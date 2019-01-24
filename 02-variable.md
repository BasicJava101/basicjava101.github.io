---
layout: page
title: Variable
---

A variable is a name you give to a value. Variable is useful especially when you have to use the value multiple times. For example, let's say you want to find a cube of a number. You multiple the number 3 times.

```
4 * 4 * 4
```

Now if you want to find the cube of 10 instead of 4, then you have to change all the 4 to 10 so it will look like this:

```
10 * 10 * 10
```

This is could lead to mistakes. When your code gets complex, what if you forgot to change a number? It also doesn't say much about the number. However, if you named that number, it will ensure that everywhere you used the number, the value will change. You can also give it a more descriptive name so you can understand what the code is doing.

```
int numberToCube = 4;

numberToCube * numberToCube * numberToCube;
```

## Declaring a variable

To declare a variable, you need to say what type it is and a value. You can use primitive data types or object types. We will talk more about object later.

```
int x = 16;
```

If you don't know what value it is, then you can declare a type and assign it a value later.

```
int x;
x = 16;
```

Personally, I recommend assigning the value when you declare the variable. This is easier to read.

### Redeclaring a variable

You can't! Once you declare a variable, you can't change the type. Nor can you redeclare the variable with the same name.

```
int x = 16;
int x = 100; // ERROR!
double x = 1.1; // ERROR!
```

If you need it to be a different type, then use a different variable.

```
int x = 16;
double y = 1.1;
```

If you need to update the value, then don't put the type at the beginning.

```
int x = 16;
x = 17;
```