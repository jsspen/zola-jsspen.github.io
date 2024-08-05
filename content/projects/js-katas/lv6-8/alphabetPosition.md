+++
title = "alphabetPosition"
+++

**Source:** [Codewars](https://www.codewars.com/kata/546f922b54af40e1e90001da/)

**The Challenge:** In this kata you are required to, given a string, replace every letter with its position in the alphabet. If anything in the text isn't a letter, ignore it and don't return it. ex. "a" = 1, "b" = 2, etc.

```js
function alphabetPosition(text) {
  let alphabet = "abcdefghijklmnopqrstuvwxyz";
  let alph = alphabet.split("");
  let positions = "";
  for (let x = 0; x < text.length; x++) {
    if (alph.indexOf(text.charAt(x).toLowerCase()) !== -1) {
      positions =
        positions + (alph.indexOf(text.charAt(x).toLowerCase()) + 1) + " ";
    }
  }
  return positions.substring(0, positions.length - 1);
}
```