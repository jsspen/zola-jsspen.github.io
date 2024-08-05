+++
title = "numberTriangle"
+++
**Source:** [Codewars](https://www.codewars.com/kata/5a906c895084d7ed740000c2/)

**The Challenge:** Consider the number triangle below, in which each number is equal to the number above plus the number to the left. If there is no number above, assume it's a 0.

```
1
1 1
1 2 2
1 3 5 5
1 4 9 14 14
```

The triangle has 5 rows and the sum of the last row is sum([1,4,9,14,14]) = 42. You will be given an integer n and your task will be to return the sum of the last row of a triangle of n rows.

```js
function solve(n) {
  n = BigInt(n);

  let triangle = [[1n], [1n, 1n]];
  let sum = 0n;
  for (let x = 2n; x <= n; x++) {
    let row = [1n];
    for (let y = 1n; y <= x; y++) {
      row.push((row[y - 1n] || 0n) + (triangle[x - 1n][y] || 0n));
    }
    triangle.push(row);
  }

  for (let x = 0n; x < triangle[n - 1n].length; x++) {
    sum += triangle[n - 1n][x];
  }
  return sum;
}
```
