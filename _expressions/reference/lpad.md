---
layout: default
section: expressions
title: "LPAD"
description: "Pads a string on the left side"
category: section
permalink: /expressions/reference/lpad/
---

### Parameters

`value` String (__required__) - The string to pad

`count` Number (__required__) - The number of characters to pad

`character` String (optional)  [default = ' '] - The character to use for padding

### Returns

String

### Examples

```js
LPAD('2', 4, '0')

// returns "0002"
```


```js
LPAD('2', 6, '0')

// returns "000002"
```