# QC-syntax
New Quantum Computing Language Syntax Proposal

## Common language features I would like to add:
### Comments
* **Inline comments**: use `#`. Compiler should be able to differentiate from `'#'` inside string.
* **Block comments**: use `###`

### Variables
* **Names can have @, !, ? (except at front)**: example: `_abCAde?!`
* **All caps for constants**: PI = 3.14159
* **Assingnment multiple**: `a,b = 1,2`
* **Variables can have specific types**: `s : String = "Hello World"`. This also applies to functions, `def f(x: Int32) : Bool ...`
* **There can be multiple datatypes**: `s : Float32|Int32|Student = 21`. We should also be able to create alias like, `Number = Float32 or Int32` and `s : Number = 21`
* 

### Functions
* **Function block definition**: Block functions should be defined as,
```
def square(x : Int32) : Int32 :
  return x*x
```
* **Inline function (Lambda) defintion**: This should be defined like variablesm `sqr(x : Int32) = x*x`
* **Same function for array of inputs with `$`:** The same integer squaring function `sqr(x : Int32) = x*x` should that allows can be defined using `$`. Pronounced like "s" and gives a chance to define functions in terms of their array entries. Should be used like,
```
sqr(n$ : Int32) = n*n # notice the $
sqr(9) # returns 81
sqr([1,2,3]) # returns [1,4,9]
```

### List and Array
* **Exclusive Range and Slicing should be done with `..`**: 

### Dictionary
* **Keys don't need quotatoins. Can be refrenced with `"..."`**: Here's what I mean
```
student = {name: "Shadman", id: 123}
student["name"] = "Shahriar"
qurey = "id"
student[qurey]
```

### Printing
* **`puts()` vs `print()`**: `puts()` will inherently have "\n"
* **`pretty()`**: pretty printing variables
