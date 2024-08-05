+++
title = "multiplesThreeAndFive"
+++
**Source:** [Codewars](https://www.codewars.com/kata/514b92a657cdc65150000006)

**The Challenge:** If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23. Finish the solution so that it returns the sum of all the multiples of 3 or 5 below the number passed in. Additionally, if the number is negative, return 0. Note: If the number is a multiple of both 3 and 5, only count it once.

```js
function solution(number) {
  let total = 0;
  for (x = number - 1; x > 0; x--) {
    if (x % 3 === 0 || x % 5 === 0) {
      total += x;
    }
  }
  return total;
}
```
