+++
title = "splitStrings"
+++
**Source:** [Codewars](https://www.codewars.com/kata/515de9ae9dcfc28eb6000001)

**The Challenge:** Complete the solution so that it splits the string into pairs of two characters. If the string contains an odd number of characters then it should replace the missing second character of the final pair with an underscore ('_').

```js
function solution(str) {
  let result = [];
  for (let x = 0; x < str.length; x++) {
    if (x + 2 < str.length + 1) {
      result.push(str.substring(x, x + 2));
      x += 1;
    } else {
      result.push(str.charAt(x) + "_");
    }
  }
  return result;
}
```
