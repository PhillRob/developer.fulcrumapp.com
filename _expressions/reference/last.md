---
layout: default
section: expressions
title: "LAST"
description: "Returns the last N items from an array or string"
category: section
permalink: /expressions/reference/last/
---

### Parameters

`array` Array (__required__) - an array object

`count` Number (optional)  [default = 1] - The number of items to return

### Returns

Object

### Examples

```js
LAST([1, 2, 3])

// returns 3
```


```js
LAST(['a', 'b', 'c'], 2)

// returns ["b","c"]
```


```js
LAST('abc')

// returns "c"
```


```js
LAST('abc', 2)

// returns ["b","c"]
```