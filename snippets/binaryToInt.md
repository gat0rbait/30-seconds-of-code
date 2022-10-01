---
title: binaryToInt
tags: math,string
expertise: beginner
firstSeen: 2022-09-24T05:00:00-04:00
---

Converts a binary string to an integer.

```js
const binaryToInt = (binary) => {
 if (typeof binary != "string") return undefined;
  let result = 0;

for (let i = 1; i <= binary.length; i++) {
    result += binary[i-1] * Math.pow(2, binary.length - i);
 }

return result;
}
```

```js
binaryToInt("0001"); // "1"
binaryToInt("110010001000"); // "3208"
```
