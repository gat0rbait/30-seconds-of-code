---
title: toBinary
tags: math,string
expertise: beginner
firstSeen: 2022-09-24T05:00:00-04:00
---

Converts an integer to its binary representation. Returns a string.

- Default bitLength is 8, but this can be modified for additional padding, OR to convert numbers larger than 255.

```js
const toBinary = (input, bitLength = 8) => {
  if (typeof input != "number") return undefined;
  let result = "";

  let max = 0;
  for (let i = bitLength - 1; i >= 0; i--) {
    max += (2 ** i);
  }
  if (input > max) return undefined;

  for (let i = bitLength - 1; i >= 0; i--) {
    let b = 2 ** i;
    if (b > input) {
      result += "0";
    } else {
      result += "1";
      input -= b;
    }
  }

  return result;
}
```

```js
toBinary(12); // "00001100"
toBinary(120, 16); // "0000000001111000"
```
