+++
title = "moveZeros"
+++
**Source:** [Codewars](https://www.codewars.com/kata/52597aa56021e91c93000cb0)

**The Challenge:** Write an algorithm that takes an array and moves all of the zeros to the end, preserving the order of the other elements.

```js
function moveZeros(arr) {
  let size = arr.length;
  let noZeros = arr.filter((x) => x !== 0);
  noZeros.push(...new Array(size - noZeros.length).fill(0));
  return noZeros;
}
```
