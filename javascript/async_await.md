# Async and Await

JavaScript functions are synchronous by default, but when they are prepended with `async` they then become asynchronous. Asynchronous functions, including ones prepended with `async` will return a `Promise` that can then be used to chain on `.then()` and `.catch()` functions.

`await` can be used only within an asynchronous function. If it prepends a `Promise` within that function it will cause the function to wait until that `Promise` has been resolved before continuing on with it's operations.