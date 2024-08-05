+++
title = "directionsReduction"
+++
**Source:** [Codewars](https://www.codewars.com/kata/550f22f4d758534c1100025a)

**The Challenge:** Write a function dirReduc which will take an array of strings and returns an array of strings with the needless
directions removed (`W<->E` or `S<->N` side by side).

In `["NORTH", "SOUTH", "EAST", "WEST"]`, the direction `"NORTH" + "SOUTH"` is going north and coming back right away. The path becomes `["EAST", "WEST"]`, now `"EAST"` and `"WEST"` annihilate each other, therefore, the final result is `[]`. In `["NORTH", "EAST", "WEST", "SOUTH", "WEST", "WEST"]`, `"NORTH"` and `"SOUTH"` are not directly opposite but they become directly opposite after the reduction of `"EAST"` and `"WEST"` so the whole path is reducible to `["WEST", "WEST"]`.

Not all paths can be made simpler. The path `["NORTH", "WEST", "SOUTH", "EAST"]` is not reducible. `"NORTH"` and `"WEST"`, `"WEST"` and `"SOUTH"`, `"SOUTH"` and `"EAST"` are not directly opposite of each other and can't become such. Hence the result path is itself: `["NORTH", "WEST", "SOUTH", "EAST"]`.

```js
function dirReduc(arr) {
  let x = 0;
  while (x < arr.length && arr.length > 1) {
    if (
      (arr[x] === "NORTH" && arr[x + 1] === "SOUTH") ||
      (arr[x] === "SOUTH" && arr[x + 1] === "NORTH") ||
      (arr[x] === "WEST" && arr[x + 1] === "EAST") ||
      (arr[x] === "EAST" && arr[x + 1] === "WEST")
    ) {
      arr.splice(x, 2);
      x = 0;
    } else {
      x++;
    }
  }
  return arr;
}
```
