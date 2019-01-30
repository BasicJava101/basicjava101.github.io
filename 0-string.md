---
layout: page
title: String
---

String is a sequence of characters. Remember the `char` type can only hold one character. In order to hold multiple characters, Java has a class named `String`. It is a sequence of text. The most common way to create a String is to use double quote. You need a double quote in the beginning of the text and another double quote to end the text. For example:

```java
String words = "apple is red";
```

The code is saying the text `apple is red` is stored in a variable of type String. The variable name is `words`.

Here are a few ways to create a new String:

```java
String empty = new String();
String empty = "";

String oneCharacter = "a";

String word = "apple";

//to have a double quote in the string, use \
String phrase = "I'm sorry for what \"I said\" when I was hungry!";

String paragraph = "It was the best of times, it was the worst of times, it was the age of wisdom, it was the age of foolishness, it was the epoch of belief, it was the epoch of incredulity, it was the season of Light, it was the season of Darkness, it was the spring of hope, it was the winter of despair, we had everything before us, we had nothing before us, we were all going direct to Heaven, we were all going direct the other way – in short, the period was so far like the present period, that some of its noisiest authorities insisted on its being received, for good or for evil, in the superlative degree of comparison only.";

```

## Converting other data type to strings

There are usually two ways to convert a primitive data type to a String. One way is to use the primitive wrapper class to convert it. Another way is to use `String.valueOf()`.

```java
//using Integer which is the wrapper class for int
String number = Integer.toString(55); // "55"
//using String.valueOf
String number2 = String.valueOf(55); // "55"

String decimal = Double.toString(3.14); // "3.14"
String decimal2 = String.valueOf(3.14); // "3.14"

String character = Character.toString('c'); // "c"
String character2 = String.valueOf('c'); // "c"
```

## The String methods
String is an object. It has many useful methods to make your life easier.

#### .length()
`.length()` returns the number of characters in the String

```
String fruit = "apple is red";
fruit.length(); // 12
```

Note that a space is a character.

`|a|p|p|l|e| |i|s| |r|e|d|`

Note that an empty String is different than a String with a space. An empty String has no character, therefore the length is 0.

```
String empty = "";
empty.length(); // 0

String space = " ";
space.length(); // 1
```

#### .charAt(int index)
`.charAt(int index)` - returns the character at the given index

Internally, the String class has an array to hold the character. Each character is associated with an index. The first character's index is 0. The second character's index is 1, and so on.

|a|p|p|l|e| |i|s| |r|e|d|
|-|-|-|-|-|-|-|-|-|-|-|-|
|0|1|2|3|4|5|6|7|8|9|10|11|

`charAt` will return the character at that index.

```
char firstCharacter =  fruit.charAt(0); // ‘a’
char sixthCharacter = fruit.charAt(5); // ‘ ’
char lastCharacter = fruit.charAt(fruit.length() - 1); // ‘d’
char secondToLastChar = fruit.charAt(fruit.length() - 2); // ‘e’
```

#### .substring(int beginIndex)
`.substring(int beginIndex)` - returns a part of the string starting from the given index

Remember that each character in a String is associated with an index.

|a|p|p|l|e| |i|s| |r|e|d|
|-|-|-|-|-|-|-|-|-|-|-|-|
|0|1|2|3|4|5|6|7|8|9|10|11|

Calling `.substring` will return a new String starting from the given index. For example, if we want to get all the characters starting from index 9 we can call `text.substring(9)`.

```
String fruit = "apple is red";

String color = fruit.substring(9);  // "red"
```

#### .substring(int beginIndex, int endIndex)
`.substring(int beginIndex, int endIndex)` - returns a part of the string starting and ending at the given indexes

```
String fruit = "apple is red";

String noun = fruit.substring(0, 5); // "apple"
String verb = fruit.substring(6, 8); // "is"
String adjective = fruit.substring(9, fruit.length()); // "red"

```

#### .trim()
`.trim()` - removes all spaces at the beginning and at the end of the string. It will leave the spaces in between characters.

```
String words = "  apple is   ";
String trimmedWord = words.trim(); // "apple is"

```

## String concatenation
To combine two or more strings together, we can use the `+` sign

```java
String name = "Moana";
String greeting = "Hello, "
String message = greeting + name; // "Hello, Moana"
```

Here are two other ways to concatenate string. These are not as popular because they're harder to read.

```java
String greeting2 = "Hello, ".concat(name).concat("!");
String greeting3 = String.join(" ","Hello,", name, "!");
```

To concatenate a String with a primitive data, you can also use the `+` sign.

```java
double pi = 3.14;
String message = "Pi is " + pi; // "Pi is 3.14"
String message2 = pi + " is pi"; // "3.14 is pi"
```


## Equality

To compare if the two Strings are the same, we can use `.equals`.

```
String fruit1 = "apple";
String fruit2 = "apple";
String fruit3 = "Apple";

fruit1.equals(fruit2); // true because they have the same characters

fruit1.equals(fruit3); // false because fruit3 is capitalized

fruit1.equalsIgnoreCase(fruit3); // true because this method doesn't care about capitalization
```

###  Don't use == to test for String equality

The `.equals` checks if the String have the same value. The `==` checks to see if the two objects are literally the same object, which means they will have the same memory address. Think of the memory address like a regular address. It is where the string is located. Take for example, you and I each has our own houses. They are exactly the same. However, we live on different block. The `.equals` checks to see if our houses are the same. The `==` checks to see if we have the same address. The `==` is not reliable, so DON'T USE IT TO COMPARE STRING. Only use the `==` to compare primitive data types like numbers.

Here is an example why `==` is bad.

```
String num = "3";
String num2 = Integer.toString(3); // this is also a string "3"

num == num2; //returns false because they have different locations

num.equals(num2); // return true because they have the same value
```

##TODO

## Empty vs Null

```
String name = null;
System.out.println("My name is " + name); // "My name is null"
name.length(); // ERROR!!!!!


String name2 = "";
System.out.println("My name is " + name2); // "My name is "
name2.length(); // 0
```

## Checking if there is a value

```
public static boolean hasValue(String value) {
    if (value != null && value.trim().length() > 0) {
        return true;
    } else {
        return false;
    }
}

System.out.println(hasValue(null)); //false
System.out.println(hasValue("")); //false
System.out.println(hasValue("   ")); //false
System.out.println(hasValue("a")); //true
```

## Strings are immutable

- Once created, they cannot be changed
- Methods that change a string return a new string (unless nothing was changed)

## String operations

- `+` - String concatenation
- `length()`
- `charAt()`
- `toCharArray()`
- `equals()`, `equalsIgnoreCase()`
- `compareTo()`
- `contains()`, `startsWith()`, `endsWith()`
- `indexOf()`, `lastIndexOf()`
- `toLowerCase()`, `toUpperCase()`
- `replace()`, `replaceAll()`, `replaceFirst()`
- `split()`, `trim()`, `join()`

Read [String API](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html) for more methods

## String Formatting

When we display money, we often want it to 

```
double total = 10.00 - 9.33;
System.out.println(total); //0.6699999999999999
```

-
## String Formatting

```
double total = 10.00 - 9.33;

String formattedTotal = String.format("Total is %,15.2f", total);
System.out.println(formattedTotal); //Total is            0.67
```

-
## String Formatting
```
"%[argument_index$][flags][min width][.precision]conversion"
```
The only field that is required is conversion

- `argument_index` - an integer indicating the position of the argument. The first argument is referenced by "1$", the second by "2$", etc.
- `flags` - modifies output like left justify, 0 padded
- `width` - the minimum number of characters
- `conversion` - indicates how the argument should be formatted

[How to format String](https://docs.oracle.com/javase/8/docs/api/java/util/Formatter.html#syntax)
-
## String Formatting
```
"%[argument_index$][flags][min width][.precision]conversion"
```
| Specifier |	Applies to | Output|
| --------- | -------- | ----- |
| %b | Any type | `true` if non-null, `false` if null |
| %c | character | character |
| %s | any type | String value |

-
## String Formatting
```
"%[argument number] [flags][width].[precision][type]"
```
| Specifier |	Applies to | Output|
| --------- | -------- | ----- |
| %d | integer (incl. byte, short, int, long, bigint) | Decimal Integer |
| %e | floating point | decimal number in scientific notation |
| %f | floating point | decimal number |

`String format = "Total is %,15.2f"`

Pads with space, group with comma, with minimum with of 15 and precision of 2. Conversion type is float.

-
## Ways to format

  - Formatter()
  - String.format()
  - NumberFormat
  - System.out.format()
  - System.out.printf

-
-
## Codepoint
Once upon a time, there was ASCII. It assigns codes between 0 and 127 to all English letters, the decimal digits, and many symbols.

-
## Codepoint
But what about Russian, Japanese, and Chinese characters?

-
## Codepoint
Unicode to the rescue!

It assigns each character in all of the writing systems ever devised a unique 16-bit code between 0 and 65535.

When you see this it will usually be in hexidecimal from 0x0000 to 0xFFFF but Java supports encoding up to 0x10FFFF

-
## Codepoint
Unicode in Java

```
String symbol = "\ud835\udd46"; // 𝕆
symbol.length(); // 2
symbol.codePointCount(0, symbol.length()); // 1
```
[List of Unicode character](https://en.wikipedia.org/wiki/List_of_Unicode_characters)

-
-
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
<img src="https://i.pinimg.com/736x/2c/ac/ae/2cacae63626e91d6887608bf51217907.jpg">
