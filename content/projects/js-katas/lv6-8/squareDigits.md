+++
title = "squareDigits"
+++
**Source:** [Codewars](https://www.codewars.com/kata/546e2562b03326a88e000020)

**The Challenge:** In this kata, you are asked to square every digit of a number and concatenate them. For example, if we run 9119 through the function, 811181 will come out, because 92 is 81 and 12 is 1. (81-1-1-81) Note: The function accepts an integer and returns an integer.

```js
function squareDigits(num) {
  let digits = num.toString().split("");
  let results = [];
  digits.forEach((x) => results.push(x * x));
  return Number(results.join(""));
}
```
