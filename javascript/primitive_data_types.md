# Primitive Data Types

In Javascript, a primitive data-type is defined by being data that is not an object and has no methods.

JS has six primitive data-types: string, number, boolean, `undefined`, `null`, and symbol.

Primitives in JS are immutable, they can not be altered. It should be noted that the data-type is not the same as the value of the variable. A variable can be reassigned but unlike objects and arrays the value itself can not be changed.

The functions available to all primitives besides `null` and `undefined` are from an equivalent object that wrap around the primitive values, these can be found by calling `valueOf()` on one of those primitive values.

---

### Null and Undefined

In JacvaScript, `undefined` is when a variable has been declared but has not been assigned a value. `null` is when a variable has explicitly been given the value of `null`.

---

### Symbols

A `Symbol` can be used as an anonymous property in an object in order to create things such as private methods. Assign `Symbol()` as the value of a variable and then use that variable for the property of a value within an object. This key/value will not appear in any Enumerable function such as `Object.keys()` but can be accessed by keying into the object with the original variable or using `Object.getOwnPropertySymbols()`.

Trying to create a `Symbol` with the `new` keyword will result in an error. `Symbol()` is instead used to create a `Symbol` as it returns a `Symbol` value instead of creating a new instance of the `Symbol` class which contains functions that should not be included in the limited functionality of a `Symbol`.