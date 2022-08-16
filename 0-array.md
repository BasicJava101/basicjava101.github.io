---
layout: page
title: Array
---

An array is an ordered collection of the same type. Let's say you want to store the temperature for the week. Instead of making 7 variables for 7 days, you can store it in one variable of the type double array.

```
double[] temperatures = {18.1, 9.5, 13.4, 10.1, 14.2, 22.4, 17.9};
```

There are two ways to create an array. If you know the values, you can use curly braces.

```
int[] numbers = {5, 1, 30, 1};

//same as above
int[] numbers2 = new int[]{5, 1, 30, 1};
```

If you don't know the value, you can create an empty array with a specific size. You have to know the size when you create an array. An empty array is an array with no value. If it is number array, then all the values will be 0. If it is a boolean array, then all the values will be false.

```
//this will give you an array of size 3
boolean[] conditions = new boolean[3]; // {false, false, false}
```

To create an array with a given size, you need to say `new` and specify a type and the `[]`. Here's the format:

```
DataType[] variableName = new DataType[size];
```

Notice to store the array in a variable, you also need to specify a type and `[]`. In general, whenever you see `[]` you know you're dealing with an array.


### Array index
A value is called an element in an array. Each element in an array is associated with an index, which specify what position it is at. The index starts at 0 so the first element is at index 0, the second element is at index 1, and so on. For example, here's a character array.

```
char[] fruit = {'a', 'p', 'p', 'l', 'e'};
```

Here are the index associated with each character.

|a|p|p|l|e|
|-|-|-|-|-|
|0|1|2|3|4|

#### Get an element

To get a character at a certain position, you use the `[index]`.

```
char[] fruit = {'a', 'p', 'p', 'l', 'e'};

//get the first character
char first = fruit[0];

//get the second character
char second = fruit[1];

//get the fifth character
char fifth = fruit[4];
```

#### Update/set element

```
char[] animal = new char[3];

//set the first character
animal[0] = 'c';

//set the second character
animal[1] = 'a';

//set the third character
animal[1] = 't';

```

#### .length

To see how many elements there are in the array, you can use `.length`.

```
char[] fruit = {'a', 'p', 'p', 'l', 'e'};

fruit.length; // 5
```

Notice that the last index is actually one less than the size. This is because the index starts at 0. So to get the last element in an array, you can do this:

```
char[] fruit = {'a', 'p', 'p', 'l', 'e'};

char lastChar = fruit[fruit.length - 1];
```

### Length/Size

Once you create an array, you cannot change its size. For example, if you have an array of size 4. If you want to add in another element, you have to create a new array of size 5. then copy the value over.

```java
int[] numbers = {5, 1, 30, 1};

int[] newNumbers = new int[numbers.length + 1];

//code to copy array
System.arraycopy(numbers, 0, newNumbers, 0, numbers.length);

//add the new element
newNumbers[newNumbers.length - 1] = 193;
```

## Copy

This is the easiest way to create a copy of an array.

```java
int[] numbers = {5, 1, 30, 1};
int[] copiedLuckyNumbers = Arrays.copyOf(numbers, numbers.length);
```

If you need to add another number, you can change the length

```java
//copy the original array
int[] copiedLuckyNumbers = Arrays.copyOf(numbers, numbers.length + 1);

//add in the new value
copiedLuckyNumbers[numbers.length] = 19;
```

## Sort

To sort an array, use `Arrays.sort`

```java
int[] numbers = {5, 1, 30, 1};
Arrays.sort(numbers); // {1, 1, 5, 30}
```

## Printing array elements

```java
int[] numbers = {5, 1, 30, 1};
System.out.println(Arrays.toString(numbers));
```

## TODO multi dimensional array


## Resources
1. [https://docs.oracle.com/javase/7/docs/api/java/util/Arrays.html](https://docs.oracle.com/javase/7/docs/api/java/util/Arrays.html)
2. [https://docs.oracle.com/javase/tutorial/java/nutsandbolts/arrays.html](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/arrays.html)
3. [creating_your_first_project](http://yfain.github.io/Java4Kids/)
4. [Scaler Topcis - Java Array](https://www.scaler.com/topics/java/array-in-java/)
