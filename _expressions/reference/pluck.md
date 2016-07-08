---
layout: default
section: expressions
title: "PLUCK"
description: "Extract property values from an object"
category: section
permalink: /expressions/reference/pluck/
---

### Parameters

`array` Array (__required__) - An array of objects to extract properties from

`property` String (__required__) - The property name to extract

### Returns

Object

### Examples

```js
var objects = [{name: 'one',   value: 1},
               {name: 'two',   value: 2},
               {name: 'three', value: 3}];
PLUCK(objects, 'value')

// returns [1,2,3]
```