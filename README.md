# QC-syntax
New Quantum Computing Language Syntax Proposal

## Common language features I would like to add:
### Variables
* **Names can have @, !, ? (except at front)**: example: `_abCAde?!`
* **All caps for constants**: PI = 3.14159
* **Assingnment multiple**: `a,b = 1,2`
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
