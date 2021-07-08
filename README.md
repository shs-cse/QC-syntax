# QC-syntax
New Quantum Computing Language Syntax Proposal

## Common language features I would like to add:
### Comments
* **Inline comments**: use `#`. Compiler should be able to differentiate from `'#'` inside string.
* **Block comments**: use `###`

### Variables
* **Names can have @, !, ? (except at front)**: example: `_abCAde?!`
* **All caps for constants**: `PI = 3.14159`
* **Assingnment multiple**: `a,b = 1,2`
* **Variables can have specific types**: `s : String = "Hello World"`. This also applies to functions, `def f(x: Int32) : Bool ...`
* **There can be multiple datatypes**: `s : Float32|Int32|Student = 21`. We should also be able to create alias like, `Number = Float32 or Int32` and `s : Number = 21`
* 

### Functions
* **Multiple Parameters**: functions with multiple parameters should be thought of as **tuple** of inputs. 
* **Function block definition**: Block functions should be defined as,
```
def square(x : Int32) : Int32 :=
  return x*x
```
* **Inline function (Lambda) defintion**: This should be defined like variablesm `sqr(x : Int32) = x*x`
* **Same function for array of inputs with `$`:** The same integer squaring function `sqr(x : Int32) = x*x` should that allows can be defined using `$`. Pronounced like "s" and gives a chance to define functions in terms of their **list** entries. Should be used like,
```
# example 1
sqr(n$ : Int32) = n*n # notice the $ allows for list of n as input
sqr(9) # returns 81
sqr([1,2,3]) # returns [1,4,9]

# example 2
area(w$: Int32, h$: Int32) = w*h # this means there can be multiple (w,h) as inputs.
area(2, [2,3]) # returns [4,6]
area([2,3], 2) # returns [4,6]
area([2,3], [4,5]) # returns [8,15]
area([1,2,3], [4,5]) # error
```

### Tuple
* **Immutable**: Like python tuples
* **Comprehension**: 

### List
* **Indexing**: 1D lists are indexed like `nums[0]` and n-D lists are indexed like `nums[0][0]` etc.
* **Logical Indexing (Mask)**: For example, `nums[x: x > 0]` and `nums[list_with_same_size_as_nums > 0]` should be able to return only positive numbers.
* **Exclusive Range `..`**: `[0..3]` is equivalent to `[0,1,2]`. 
* **List Slicing**: Range can be used for slicing: `nums2d[0..3][1..2]`. Also `,` can be used to skip through elements: `nums[1,3] # returns [nums[1], nums[3]]`. Both of these can be used together: `nums[0..2,3] # returns [nums[0], nums[1], nums[3]]

### Dictionary
* **Keys don't need quotatoins. Can be refrenced with `"..."`**: Here's what I mean,
```
student = {name: "Shadman", id: 123}
student["name"] = "Shahriar"
qurey = "id"
student[qurey]
```

### Set

### Generator

### Data-Types
* **String**: format string with `#{}`. For example, `"#{PI}` should return "3.14159"

### Printing
* **`puts()` vs `print()`**: `puts()` will inherently have "\n"
* **`pretty()`**: pretty printing variables
