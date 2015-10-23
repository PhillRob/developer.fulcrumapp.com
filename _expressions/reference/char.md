---
layout: default
section: expressions
title: "CHAR"
description: "Convert a number into a character according to the current Unicode table."
category: section
permalink: /expressions/reference/char/
---

## CHAR

Convert a number into a character according to the current Unicode table.

### Parameters

`number` Number (__required__) - The number of the character to look up from the current Unicode table in decimal format.

### Returns

String

### Examples

~~~
CHAR(65)

// returns A
~~~
{: .language-js}


~~~
CHAR(1337)

// returns Թ
~~~
{: .language-js}