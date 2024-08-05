+++
title = "firstNonRepeatingLetter"
+++
**Source:** [Codewars](https://www.codewars.com/kata/52bc74d4ac05d0945d00054e/)

**The Challenge:** Write a function that takes a string input, and returns the first character
that is not repeated anywhere in the string. As an added challenge, upper- and lowercase letters are considered the same character but the function should return the correct case for the initial letter. If a string contains all repeating characters, it should return an empty string ("");

```js
function firstNonRepeatingLetter(s) {
  let contender = "";
  let disregard = [];
  for (let x = 0; x < s.length; x++) {
    if (contender === "" && !disregard.includes(s.charAt(x))) {
      contender = s.charAt(x);
    }
    for (let y = x + 1; y < s.length; y++) {
      if (s.charAt(x).toLowerCase() === s.charAt(y).toLowerCase()) {
        contender = "";
        disregard.push(s.charAt(y));
        y = s.length;
      }
    }
    if (contender.length > 0) {
      return contender;
    }
  }
  return contender;
}
```
