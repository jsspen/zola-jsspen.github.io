+++
title = "spinWords"
+++
**Source:** [Codewars](https://www.codewars.com/kata/5264d2b162488dc400000001)

**The Challenge:** Write a function that takes in a string of one or more words, and returns the same string, but with all words that have five or more letters reversed. Strings passed in will consist of only letters and spaces. Spaces will be included only when more than one word is present.

```js
function spinWords(string) {
  let words = string.split(" ");
  let result = [];
  for (let x = 0; x < words.length; x++) {
    let word = words[x].split("");
    if (word.length > 4) {
      word = word.reverse();
    }
    result.push(word.join(""));
  }
  return result.join(" ");
}
```
