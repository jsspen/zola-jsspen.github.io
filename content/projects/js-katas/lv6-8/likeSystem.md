+++
title = "likeSystem"
+++
**Source:** [Codewars](https://www.codewars.com/kata/5266876b8f4bf2da9b000362)

**The Challenge:** You probably know the "like" system from Facebook and other pages. People can "like" blog posts, pictures or other items. We want to create the text that should be displayed next to such an item. Implement the function which takes an array containing the names of people that like an item. It must return the display text as shown in the examples:

```js
[]                                -->  "no one likes this"
["Peter"]                         -->  "Peter likes this"
["Jacob", "Alex"]                 -->  "Jacob and Alex like this"
["Max", "John", "Mark"]           -->  "Max, John and Mark like this"
["Alex", "Jacob", "Max", "Mark"]  -->  "Alex, Jacob and 2 others like this"
```

Note: For 4 or more names, the number in "and 2 others" simply increases.

```js
function likes(names) {
  let message = "no one likes this";
  switch (names.length) {
    case 1:
      message = names[0] + " likes this";
      break;
    case 2:
      message = names[0] + " and " + names[1] + " like this";
      break;
    case 3:
      message = names[0] + ", " + names[1] + " and " + names[2] + " like this";
      break;
  }
  if (names.length > 3) {
    message =
      names[0] +
      ", " +
      names[1] +
      " and " +
      (names.length - 2) +
      " others like this";
  }
  return message;
}
```
