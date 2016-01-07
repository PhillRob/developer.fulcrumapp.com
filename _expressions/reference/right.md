---
layout: default
section: expressions
title: "RIGHT"
description: "Returns a substring from the end of a given string."
category: section
permalink: /expressions/reference/right/
---

### Parameters

`value` String (__required__) - The string value from which the right portion will be returned.

`number_of_characters` Number (optional)  [default = 1] - The number of characters to return from the right side of the string.

### Returns

String

### Examples

{% highlight js %}
RIGHT("ABCDEFG", 4)

// returns DEFG
{% endhighlight %}


{% highlight js %}
RIGHT("000001")

// returns 1
{% endhighlight %}