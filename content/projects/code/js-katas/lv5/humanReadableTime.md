+++
title = "humanReadableTime"
+++
**Source:** [Codewars](https://www.codewars.com/kata/52685f7382004e774f0001f7/train/javascript)

**The Challenge:** Write a function, which takes a non-negative integer (seconds) as input and returns the time
in a human-readable format (`HH:MM:SS`). The maximum time never exceeds 359999 (`99:59:59`)

- HH = hours, padded to 2 digits, range: 00 - 99
- MM = minutes, padded to 2 digits, range: 00 - 59
- SS = seconds, padded to 2 digits, range: 00 - 59

```js
function humanReadable(seconds) {
  let actualSeconds = seconds % 60 < 10 ? "0" +
   (seconds % 60) : seconds % 60;
  let minutes = Math.floor(seconds / 60);
  let actualMinutes = minutes % 60 < 10 ? "0" +
   (minutes % 60) : minutes % 60;
  let hours =
    Math.floor(minutes / 60) < 10
      ? "0" + Math.floor(minutes / 60)
      : Math.floor(minutes / 60);
  return hours + ":" + actualMinutes + ":" + actualSeconds;
}
```
