# Notes for JavaScript

## Data Types
- Data types:
  - String
  - Number
  - Boolean
  - undefine
  - null
  - object

- String
  - concatenation
    - `str1 + str2`
  - length
    - `str.length()`
  - slice
    - `str.slice(start, end)`
    - substring [start, end)
  - change case:
    - `str.toUpperCase()`
    - `str.toLowerCase()`

- Number
  - increment statement
  - `num++`
  - `num+=1`

## Function
- define function
    - `function functionName(arguments) {...}`
- some functions:
  - `console.log()`
  - `alert()`
  - `prompt()`

## Operators

### Comparators:
- Equal
  - `===` also check data type equality
  - `==`
- Not equal
  - `!==`
  - `!=`
- greater, less than
  - `>`
  - `<`
  - `>=`
  - `<=`

### Logical operators:
- AND: `&&`
- OR: `||`
- NOT: `!`

## Control Flow
- if statement
  - `if () {} else if () {} else {}`
- switch statement
  - `switch(expression): case (x): ... break; case(y): ... break; default: ... break;`
- while loop
  - `while () {}`
- for loop 
  - `for (var i = 0; i < 10; i++) {}`

## Array
- `array = [...]`
- `array.push()`
- `array.pop()`

## Object
- create a object
  - `obj = {name: "Jack", age: 24, gender: "male"}`
- access object properties
  - `obj.name`
  - `obj["name"]`
- add or change properties:
  - `obj.job = "SDE"`
- add or change methods
  - `obj.work = function () {...}`
- constructor
  - constructor function should start with a upper-case letter
  - `function Person(name, age, gender) {this.name = name; this.age= age; this.gender= gender; this.work = function () {...}}`
  - `let person1 = new Person("Jack", 24, "male")`