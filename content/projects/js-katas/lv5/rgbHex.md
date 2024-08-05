+++
title = "rgbHex"
+++
**Source:** [Codewars](https://www.codewars.com/kata/513e08acc600c94f01000001/)

**The Challenge:** The rgb function is incomplete. Complete it so that passing in RGB decimal values will result in a hexadecimal representation being returned. Valid decimal values for RGB are 0 - 255. Any values that fall out of that range must be rounded to the closest valid value. Note: Your answer should always be 6 characters long.

```js
255, 255, 255 --> "FFFFFF"
255, 255, 300 --> "FFFFFF"
0, 0, 0       --> "000000"
148, 0, 211   --> "9400D3"
```

```js
function rgb(r, g, b) {
  let input = [r, g, b];
  let hex = "";
  for (let x = 0; x < input.length; x++) {
    input[x] = input[x] > 255 ? 255 : input[x];
    input[x] = input[x] < 0 ? 0 : input[x];
    let current = [Math.floor(Math.floor(input[x] / 16) % 16), input[x] % 16];
    for (let y = 0; y < current.length; y++) {
      if (current[y] > 9) {
        switch (current[y]) {
          case 15:
            current[y] = "F";
            break;
          case 14:
            current[y] = "E";
            break;
          case 13:
            current[y] = "D";
            break;
          case 12:
            current[y] = "C";
            break;
          case 11:
            current[y] = "B";
            break;
          case 10:
            current[y] = "A";
            break;
        }
      }
    }
    hex = hex + current[0] + current[1];
  }
  return hex;
}
```
