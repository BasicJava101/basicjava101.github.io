---
layout: page
title: String & Loop
---


## Building Strings

Using the StringBuilder class allows you to build a string from many small pieces.

```
StringBuilder builder = new StringBuilder("ap");

builder.append('p'); // appends a single character
builder.append("le"); // appends a string

String completedString = builder.toString(); // "apple"
```
[StringBuilder API](https://docs.oracle.com/javase/7/docs/api/java/lang/StringBuilder.html)

-
## Building Strings

- Use `+` to concatenate a small set of string.
- Use StringBuilder for large or unknown number of string
  - Ex: for loop, or reading a file

-
## Building Strings

### DEMO!!!
Remove vowel from words

-
## Lab

[Leon's Loopy Lab](https://git.zipcode.rocks/ZipCodeWilmington/CR-MicroLabs-Loops-NumbersTrianglesTables)
-
