+++
title = "piglatin"
+++
**Source:** [Codewars](https://www.codewars.com/kata/520b9d2ad5c005041100000f)

**The Challenge:** Move the first letter of each word to the end of it, then add "ay" to the end of the word. Leave punctuation marks untouched.

```js
function pigIt(str) {
  let results = "";
  let start = 0;
  for (let x = 0; x <= str.length; x++) {
    if (str[x] === " " || x === str.length) {
      let word = str.slice(start, x);
      start = x + 1;
      results += word.substr(1, word.length - 1) + word.charAt(0);
      if (!/[!"#$%&'()*+,-./:;<=>?@[\]^_`{|}~]/.test(word[word.length - 1])) {
        results += "ay";
      }
      if (x !== str.length) {
        results += " ";
      }
    }
  }
  return results;
}
```
