# Skore's Javascript Style Guide

# contents

- [General](#general)
  - [Variables](#general-variables)
- [Code](#code)
  - [Strings](#code-strings)
  - [Functions](#code-functions)
  - [Classes](#code-classes)

<a name='general'></a>
## General

- use soft-tabs with a 2 spaces for indentation
- never use `;`
- use spaces between `{}` or `[]`. Ex: `{ a: 1 }` `[ 0, 1, 2 ]`
- prefer early return instead of giant `if` or ternary inside functions/methods
- prefer ternary for string concatenation

<a name='general-variables'></a>
### Variables

- always use const
- `camelCased` for regular const vars
- `UPPER_CASE` for primitive hard-coded values

<a name='code'></a>
## Code

<a name='code-strings'></a>
### Strings

- use single quotes for strings
- use template string for variable concatenation
```js
const bad = 'hello, ' + name
const awesome = `hello, ${ name }`
```

<a name='code-functions'></a>
### Functions

- always wrap the parameters of an arrow function with parentesis, even if it's a single parameter
```js
const badFn = n => n + 1
const awesomeFn = (n) => n + 1
```
- always use single line arrow functions for simple calls
```js
const bad = () => { something() }
const awesome = () => something()
```
- always use single line arrow functions when only returning a value
```js
const bad = (a) => { return { a } }
const awesome = (a) => ({ a })
```
- space between the `)` and the `{`. Ex: `function awesomeFn(args) {`
- pass functions arguments as object, so you don't have to worry about parameter order
```js
function awesome({ a, b, c }) {
  return [ a, b, c ]
}
awesome({ a: 1, c: 3, b: 2})
```

<a name='code-classes'></a>
### Classes

- put the getter in the end of the class
