---
title: toHexadecimal
tags: math,string
expertise: beginner
firstSeen: 2022-09-24T05:00:00-04:00
---

Converts an integer to its hexadecimal representation. Returns a string.

```js
const toHexadecimal = (quotient) => {
  if (typeof quotient != "number") return undefined;
let remainder;
let stack = [];
let result = "";

const hexKey = {
    1: "1",
    2: "2",
    3: "3",
    4: "4",
    5: "5",
    6: "6",
    7: "7",
    8: "8",
    9: "9",
    10: "A",
    11: "B",
    12: "C",
    13: "D",
    14: "E",
    15: "F"
}

  while (quotient > 0) {
    remainder = quotient%16;
    quotient = Math.floor(quotient/16);
    stack.push(hexKey[remainder]);
    input = quotient;
  }
  
 while (stack.length) {
     result += stack.pop()
 }

console.log(result);
  return result;
}
```

```js
toHexadecimal(12); // "C"
toHexadecimal(74); // "4A"
```
