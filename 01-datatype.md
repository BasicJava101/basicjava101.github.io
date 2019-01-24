---
layout: page
title: Data Types
---

In Java, there are 8 primitive data types. They are the basic building blocks for the language. You can build complex objects and applications based on these data types, similar to how you can create a skyscraper out of simple Lego pieces.

1. byte
2. short
3. int
4. long
5. float
6. double
7. char
8. boolean

-----

## Integer Types

For negative and positive numbers without fractions, you have four choices: byte, short, int, and long.

| Type  | Storage  | Range (Inclusive)                                       | Example |
| ----- |:----------- | :------------------------------------------------------ | --------- |
| byte  | 1 byte      | -128 to 127                                             | `byte b = 127;` |
| short | 2 bytes     | –32,768 to 32,767                                       | `short s = 30000;` `short s1 = -32_000;`|
| int   | 4 bytes     | –2,147,483,648 to 2,147,483, 647 (just over 2 billion)  | `int i = 20;` |
| long  | 8 bytes     | –9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 | `long l = 100;` `long l1 = 100L;` `long l2 = 100l;` |

### Byte
Note for each type, there is a storage associated with it. The storage space is called byte. Think of it like a bucket. It refers to how many bucket is needed to store the number.  This is important when memory was expensive. But now, memory is usually not a factor for most computer, so most developers use `int` for simple numbers and `long` for large numbers.

### Casting

Java automatically converts a smaller type number into a larger type because it is not losing any data.

```
byte b = 127;
int i = b;
```

However, to cast a larger type into a smaller type, you have to write the type you want to convert it to. For example, if you have an `int` (4 byte) and you want to convert it to a byte (1 byte), then there is a possibility that the number might not fit into the byte. Therefore, Java forces you to say, yes, I understand I might lose some data, convert it anyway.

```
int i = 129;
byte b = (byte)i; // casting from 4 bytes into 1 byte
// b becomes -127 because the maximum number a byte can be is 127
```

## Decimal Types

Numbers with fractions

| Type   | Storage requirements | Range (Inclusive)                                              |
| ------ |:------------------- | :------------------------------------------------------------- |
| float  | 4 bytes             | Approximately ±3.40282347E+38F (6–7 significant decimal digits) |
| double | 8 bytes             | Approximately ±1.79769313486231570E+308 (15 significant decimal digits)|


### Casting

Java can automatically cast integers into float/double.

```
int i = 2000;
float f = i;
```

Because of the loss of precision, to cast from a decimal number into an integer, you have to explicitly say so.

```
float f = 3.14f;
int i = (int)f; //i is 3
```

## char Type

The char type is a single character represented by a value enclosed in single quotes. It takes up 2 bytes.

```
char a = 'a';
char capA = 'A';
char semi = ';';
char num = '8';
```
Note `'8'` is NOT the same as the number `8` without quotes. One is a char, the other is an int.

You can use a number to represent a character. `A` is mapped to the number 65 so you can write it like this:

```
char numChar = 65; // 'A'
```

## boolean Type

The boolean type has two values: <span style="color: red">false</span> and <span style="color:green">true</span>.

```
boolean t = true;
boolean f = false;
```

You can use it to store the result of a comparison because the comparison yields `true` or `false`.

```
boolean a = 1 > 0; // true
boolean b = 1 > 5; // false
boolean c = 1 == 1; // true
boolean d = 1 >= 5; // false
boolean e = 1 <= 5; // true
boolean f = 8 == '8'; // false
```


## Is Java a true object oriented language?

No, because primitive types are not objects.

--------

## Resources
- Core Java Chapter 3.3
- [Data types - Oracle](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html)
- [Understanding Binary](https://www.youtube.com/watch?v=Xpk67YzOn5w)


<img src="https://weneedfun.com/wp-content/uploads/2015/10/Cute-puppy-Pictures-29.jpg" width="70%">
