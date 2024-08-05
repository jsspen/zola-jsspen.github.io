+++
title = "oddInt"
+++
**Source:** [Codewars](https://www.codewars.com/kata/54da5a58ea159efa38000836)

**The Challenge:** Given an array of integers, find the one that appears an odd number of times. There will always be only one integer that appears an odd number of times.

- `[7]` should return `7`, because it occurs 1 time (which is odd).
- `[0]` should return `0`, because it occurs 1 time (which is odd).
- `[1,1,2]` should return `2`, because it occurs 1 time (which is odd).
- `[0,1,0,1,0]` should return `0`, because it occurs 3 times (which is odd).
- `[1,2,2,3,3,3,4,3,3,3,2,2,1]` should return `4`, because it appears 1 time (which is odd).

```js
function findOdd(A) {
  for (let x = 0; x < A.length; x++) {
    let contender = A[x];
    let count = 1;
    if (A.indexOf(contender) !== x) {
      continue;
    }
    for (let y = x + 1; y < A.length; y++) {
      if (A[y] === contender) {
        count++;
      }
    }
    if (count % 2 !== 0) {
      return contender;
    }
  }
}
```
