+++
title = "duplicateCount"
+++
**Source:** [Codewars](https://www.codewars.com/kata/54bf1c2cd5b56cc47f0007a1)

**The Challenge:** Write a function that will return the count of distinct case-insensitive alphabetic characters and numeric digits that occur more than once in the input string. The input string can be assumed to contain only alphabets (both uppercase and lowercase) and numeric digits.

```js
"abcde" -> 0 # no characters repeats more than once
"aabbcde" -> 2 # 'a' and 'b'
"aabBcde" -> 2 # 'a' occurs twice and 'b' twice (`b` and `B`)
"indivisibility" -> 1 # 'i' occurs six times
"Indivisibilities" -> 2 # 'i' occurs seven times and 's' occurs twice
"aA11" -> 2 # 'a' and '1'
"ABBA" -> 2 # 'A' and 'B' each occur twice
```

```js
function duplicateCount(text) {
  let count = 0;
  let counts = {};
  for (let i = 0; i < text.length; i++) {
    let char = text[i].toLowerCase();
    counts[char] = counts[char] ? counts[char] + 1 : 1;
  }
  for (let x = 0; x < text.length; x++) {
    if (counts[text[x].toLowerCase()] > 1) {
      count++;
      counts[text[x].toLowerCase()] = 0;
    }
  }

  return count;
}
```
