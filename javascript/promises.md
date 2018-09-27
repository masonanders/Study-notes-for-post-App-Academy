# Promises

Promises are JavaScript objects that represent the eventual success or failure of an asynchronous operation.

After a promise is executed, it invokes a given callback based on the success or failure of the operation executed through a `.then()` function chain. `.then()` can take a success situation callback as it's first argument, and an failure situation callback as it's second. `.then()` returns a new promise based off of the original operation as well as the success/failure callback it executed which can then be chained to another `.then()` function.

The first argument of `.then()` must always be the success callback. The failure callback may be omitted but if you wish to only execute a callback upon failure you may add a placeholder as the first argument, like so `.then(_, failureCallback)`. Alternatively you can use `.catch()` which takes one argument, the failure callback, and executes that upon failure.

You must always have a return value witin a `.then()`/`.catch()` function if you wish to chain on another `.then()`/`.catch()`.