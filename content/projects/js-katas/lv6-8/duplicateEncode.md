+++
title = "duplicateEncode"
+++
**Source:** [Codewars](https://www.codewars.com/kata/54b42f9314d9229fd6000d9c)

**The Challenge:** The goal of this exercise is to convert a string to a new string where each character in the new string is `(` if that character appears only once in the original string, or `)` if that character appears more than once in the original string. Ignore capitalization when determining if a character is a duplicate.

```js
"din"      =>  "((("
"recede"   =>  "()()()"
"Success"  =>  ")())())"
"(( @"     =>  "))(("
```

```js
function duplicateEncode(word) {
  let counts = {};
  let result = "";
  for (let i = 0; i < word.length; i++) {
    let char = word[i].toLowerCase();
    counts[char] = counts[char] ? counts[char] + 1 : 1;
  }
  for (let x = 0; x < word.length; x++) {
    result = counts[word[x].toLowerCase()] > 1 ? result +
     ")" : result + "(";
  }
  return result;
}
```