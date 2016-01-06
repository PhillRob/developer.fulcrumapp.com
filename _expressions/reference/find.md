---
layout: default
section: expressions
title: "FIND"
description: "Returns the position at which a string is first found within text, case-sensitive."
category: section
permalink: /expressions/reference/find/
---

### Parameters

`search_for` String (__required__) - String to search for within `text_to_search`.

`text_to_search` String (__required__) - Text to search for the first instance of `search_for`.

`starting_at` Number (__required__) - argument Position index to begin the search.

### Returns

Number

### Examples

~~~
FIND("needle", "the needle is in the haystack")

// returns 5
~~~
{: .language-js}