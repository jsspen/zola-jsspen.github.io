+++
title = "trailingZeros"
+++

**Source:** [Codewars](https://www.codewars.com/kata/52f787eb172a8b4ae1000a34)

**The Challenge:** Write a program that will calculate the number of trailing zeros in a factorial of a given number.

```js
function zeros(n) {
  let zeros = Math.floor(n / 5);
  for (let x = 2; 5 ** x <= n; x++) {
    zeros = zeros + Math.floor(n / 5 ** x);
  }
  return zeros;
}
```
