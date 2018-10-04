# Array Functions

### Reduce
The `.reduce()` function takes a developer provided callback that runs on each element in the array. It can take a optional second argument that acts as the starting value.

The callback will be fed four parameters, the accumulator, the current value, the index, and the source array. The return value from this function becomes the new accumulator for the next callback call on the next element in the array or is returned by `.reduce()` when the iteration is complete.

```
const arr = [1, 2, 3, 4, 5];
const reducer = (accum, curval) => accum + curVal;

arr.reduce(reducer); // 15
arr.reduce(reducer, 5); // 20
```