# Readings: React 1

## Legend
I'm not a fan of `foo` `bar` `baz`. Here is a key of most identifier names used throughout this reference.

* Variable: `x`
* Object: `obj`
* Array: `arr`
* Function: `func`
* Parameter, method: `a`, `b`, `c`
* String: `str`

## Variable declaration

ES6 introduced the let keyword, which allows for block-scoped variables which cannot be hoisted or redeclared.

```
var x = 0
```
```
let x = 0
```

> MDN Reference: let

## Constant declaration

 introduced the `const` keyword, which cannot be redeclared or reassigned, but is not immutable.

```
const CONST_IDENTIFIER = 0 // constants are uppercase by convention
```

> MDN Reference: const

## Arrow functions
The arrow function expression syntax is a shorter way of creating a function expression. Arrow functions do not have their own this, do not have prototypes, cannot be used for constructors, and should not be used as object methods.

```
function func(a, b, c) {} // function declaration
var func = function (a, b, c) {} // function expression
```
```
let func = (a) => {} // parentheses optional with one parameter
let func = (a, b, c) => {} // parentheses required with multiple parameters
```
> MDN Reference: Arrow functions
## Template literals
Concatenation/string interpolation
Expressions can be embedded in template literal strings.

```
var str = 'Release date: ' + date
```
```
let str = `Release Date: ${date}`
```

> MDN Reference: Expression interpolation

## Multi-line strings

Using template literal syntax, a JavaScript string can span multiple lines without the need for concatenation.

```
var str = 'This text ' + 'is on ' + 'multiple lines'
```
```
let str = `This text
            is on
            multiple lines`
```

* Note: Whitespace is preserved in multi-line template literals. See Removing leading whitespace in ES6 template strings.

> MDN Reference: Multi-line strings
## Implicit returns
The return keyword is implied and can be omitted if using arrow functions without a block body.

```
function func(a, b, c) {
  return a + b + c
}
```
```
let func = (a, b, c) => a + b + c // curly brackets must be omitted
```
> MDN Reference: Function body
