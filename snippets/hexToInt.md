---
title: hexToInt
tags: math,string
expertise: beginner
firstSeen: 2022-09-24T05:00:00-04:00
---

Converts a hexadecimal string to an integer.

```js
const hexToInt = (hexadecimal) => {
  if (typeof hexadecimal != "string") return undefined;
let result = 0;

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

for (let i = 1; i <= hexadecimal.length; i++) {
    let num = Object.keys(hexKey).find(key => hexKey[key] === hexadecimal[i-1]);
    result += num * Math.pow(16, hexadecimal.length - i);
 }

return result;
}
```

```js
hexToInt("C"); // "12"
hexToInt("4A"); // "74"
```
