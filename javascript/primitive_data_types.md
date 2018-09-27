# Primitive Data Types

In Javascript, a primitive data-type is defined by being data that is not an object and has no methods.

JS has six primitive data-types: string, number, boolean, `undefined`, `null`, and symbol.

Primitives in JS are immutable, they can not be altered. It should be noted that the data-type is not the same as the value of the variable. A variable can be reassigned but unlike objects and arrays the value itself can not be changed.

The functions available to all primitives besides `null` and `undefined` are from an equivalent object that wrap around the primitive values, these can be found by calling `valueOf()` on one of those primitive values.