---
layout: default
section: expressions
title: "SORT"
description: "Returns the sorted values within an array"
category: section
permalink: /expressions/reference/sort/
---

### Parameters

`values` Array (__required__) - The values to sort

`callback` function (optional) - A transform function to use when sorting objects

### Returns

Array

### Examples

```js
SORT([1, 2, 3, 3, 1])

// returns [1,1,2,3,3]
```


```js
SORT(['a', 'c', 'b', 'a', 'b'])

// returns ["a","a","b","b","c"]
```