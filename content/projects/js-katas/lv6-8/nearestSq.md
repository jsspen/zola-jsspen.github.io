+++
title = "nearestSq"
+++
**Source:** [Codewars](https://www.codewars.com/kata/5a805d8cafa10f8b930005ba)

**The Challenge:** Your task is to find the nearest square number of a positive integer n

```js
function nearestSq(n) {
  let nearest = 1;
  for (let x = 1; x <= n; x++) {
    let square = x * x;
    if (Math.abs(n - square) < Math.abs(n - nearest) || n === nearest) {
      nearest = square;
    }
  }
  return nearest;
}
```