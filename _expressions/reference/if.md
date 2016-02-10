---
layout: default
section: expressions
title: "IF"
description: "Returns one value if a logical expression is true and another if it is false."
category: section
permalink: /expressions/reference/if/
---

### Parameters

`value` * (__required__) - logical expression

`value_if_true` * (__required__) - The value to return if the expression is true

`value_if_false` * (__required__) - The value to return if the expression is false

### Returns

*

### Examples

```js
IF(1 > 3, '1 is greater than 3', '1 is less than 3')

// returns 1 is less than 3
```


```js
IF(ISSELECTED($choice_field, 'Red'), 'Red is selected', 'Red is not selected')

// returns Red is selected
```