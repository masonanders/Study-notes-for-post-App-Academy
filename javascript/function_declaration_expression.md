# Function Declaration vs Expression

## Function Declaration
A function declaration is when you precede a variable name with `function` instead of assigning it to a variable. Function declarations get hoisted along with it's code block.

Function declarations are not officially allowed inside of a non-function block (such as `if`), however, many browsers and other environments will allow such behavior, albeit in different ways.

```
function test(arg) {
  console.log(arg);
}
```

## Function Expression
A function expression is when you assign a function declaration to a variable. The function can be anonymous or named, but will be referenced and called by the variable name regardless. The variable may get hoisted but since it's value is the function declaration that will not be interpreted by JS before execution.

```
const func = function(arg) {
  console.log(arg);
}

const tion = function logMe(arg) {
  console.log(arg);
}
```

## Self Invoking Function
You can wrap a function declaration inside a pair of parentheses and then add a second pair at the end to create a self invoking function declaration.
```
(function logMe(arg) {
  console.log(arg);
})('test');
```