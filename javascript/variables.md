# Variables

In JavaScript, variable represents an arbitrary value. Js is loosely typed, meaning that a variable is not type-locked, does not need it's type specified during declaration, and in most cases can be reassigned to another type of value.

In JS, a variable must start with a letter, an underscore, or a dollar-sign. Other characters that can be use within a variable name are 0 through 9. JS variables are case-sensitive.

Once a variable has been declared, it can not then be re-declared within that local scope.

---

## Hoisting
Hoisting occurs as JS reads a block of code before it executes it. Certain variables are then recognized from the beginning of execution as declared but has a value of `undefined` until JS reaches the point in execution where that variable is given a value. It is best practice to declare and assign your variables at the top of your blocks.

`function` declarations are also hoisted, however, only the declaration is and the expression is not read or executed until JS reaches it during execution.

---

## Var
`var` declares a variable and is hoisted by JavaScript before the code is run. This can cause unexpected behavior and bugs.


## Let
`let` declares a variable scoped locally relative to where it is declared and is not hoisted. `let` can be reassigned to any type of value and must be declared before referenced.


## Const
`const` is similar to `let` expect that it is read-only. You can not reassign a value to a variable declared by `const`. It should be mentioned that while a constant is read-only and not able to be reassigned, that does not mean the value cannot be mutated, you can still add to and subtract from an array assigned to a `const`.

---

## Parent
`parent` can be used within a function to reference it's parent object and it's variables.