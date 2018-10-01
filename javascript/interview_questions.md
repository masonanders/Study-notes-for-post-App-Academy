# Interview Questions

Q: What is the pitfall of using `typeof thing === "object"` when determining whether something is an `object` and what can you do to avoid those pitfalls?

A: `typeof null` returns `"object"` so you could end up with a case where you're getting a truthy value with `null`. To avoid this you can simply throw in a check for `null`/`false` beside the check for an object.

---

Q: What will this code snippet output?
```
(function(){
  var a = b = 3;
})();

console.log("a defined? " + (typeof a !== 'undefined'));
console.log("b defined? " + (typeof b !== 'undefined'));
```

A: `var a = b = 3` is shorthand for 
```
b = 3;
var a = b;
```
In this case, if you are not using strict mode, the output will be 
```
a defined ? false
a defined ? true
```
In the function, `b` was declared as a global variable and then `a` was declared with a value of `b` but only within the local scope of the function so it will be `undefined` when referenced in the `console.log();`.

---

Q: What will this code snippet output?
```
var myObject = {
    foo: "bar",
    func: function() {
        var self = this;
        console.log("outer func:  this.foo = " + this.foo);
        console.log("outer func:  self.foo = " + self.foo);
        (function() {
            console.log("inner func:  this.foo = " + this.foo);
            console.log("inner func:  self.foo = " + self.foo);
        }());
    }
};
myObject.func();
```
A: 
```
outer func: this.foo = foo
outer func: self.foo = foo
inner func: this.foo = undefined
inner func: self.foo = foo
```
In `outer func`, `this` and `self` both refer to `myObject`. But in `inner func`, this no longer refers to `myObject` while `self` has been passed down from an upper scope and remains the same.

---

Q: What is the significance of, and reason for, wrapping the entire contents of a JavaScript file in a function block?

A: It creates a closure and a private namespace for the source code which helps avoid clashes between two different files which may share the same names for variables.  

---

Q: Will these two functions return the same thing?
```
function foo1()
{
  return {
      bar: "hello"
  };
}

function foo2()
{
  return
  {
      bar: "hello"
  };
}
```

A: They will not. `foo1()` will return the object within, but `foo2()` will return `undefined`. This is a bit unexpected considering it is not throwing any error. 

This has to do with the fact that JS will automatically add semicolons where it thinks they should be. Since there is nothing after the return statement, JS will add a semicolon there. No error is thrown because it is all valid code, albeit everything after the `return` is unreachable.

---

Q: What is `NaN`? What is it's type? How can you reliably test if something is equal to `NaN`?

A: `NaN` is a value that stands for "Not a number". It is the result when an expression cannot be performed due to two values, one of which not being a number while the other is, being paired.

Some unexpected behaviors are `NaN === NaN` returns a falsy value as well as `typeof NaN` returning `"number"`.

There is a built in `isNan()` function, but it's not reliable. ES6 has a `Number.isNan()` which is more reliable, but you can also use the comparison trick to your advantage `value !== value` since the only time it would produce true is when `value` is equal to `NaN`.

---

Q: What will this code snippet output?
```
console.log(0.1 + 0.2);
console.log(0.1 + 0.2 == 0.3);
```

A: Since numbers in JavaScript are treated with floating point precision, the educated answer is, you cannot be sure.

In this case the answer will be 
```
0.30000000000000004
false
```