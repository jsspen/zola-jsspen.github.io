+++
title = "persistence"
+++
**Source:** [Codewars](https://www.codewars.com/kata/55bf01e5a717a0d57e0000ec/)

**The Challenge:** Write a function, persistence, that takes in a positive parameter num and returns its multiplicative persistence, which is the number of times you must multiply the digits in num until you reach a single digit.

```js
function persistence(num) {
  let count = 0;
  while (num.toString().length > 1) {
    num = num
      .toString()
      .split("")
      .reduce((t, c) => t * c);
    count++;
  }
  return count;
}
```