+++
title = "findOutlier"
+++

**Source:** [Codewars](https://www.codewars.com/kata/5526fc09a1bbd946250002dc)

**The Challenge:** You are given an array (which will have a length of at least 3, but could be very large) containing integers. The array is either entirely comprised of odd integers or entirely comprised of even integers except for a single integer N. Write a method that takes the array as an argument and returns this "outlier" N.

```js
function findOutlier(integers) {
  let evens = 0;
  let odds = 0;
  let type = "";
  for (let x = 0; x < integers.length; x++) {
    if (integers[x] % 2 !== 0) {
      odds += 1;
    } else {
      evens += 1;
    }
    if (evens > 1) {
      type = "evens";
    }
    if (odds > 1) {
      type = "odds";
    }
  }
  for (let y = 0; y < integers.length; y++) {
    if (integers[y] % 2 !== 0 && type === "evens") {
      return integers[y];
    } else if (integers[y] % 2 === 0 && type === "odds") {
      return integers[y];
    }
  }
}
```
