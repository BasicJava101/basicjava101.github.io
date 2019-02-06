---
layout: page
title: For Loop
---


When you need to do something over and over again, you can often use a loop for it. For example, here's the code to print out from 1 to 5

```java
System.out.println(1);
System.out.println(2);
System.out.println(3);
System.out.println(4);
System.out.println(5);

```

Note the only thing that change is the number. Let's try to extract the thing that change and format the code so every print statement look the same.

```java
//extract the thing that change
int i = 1; // 1

//make the code so the print statement look the same
System.out.println(i);
i = i + 1; // 2

System.out.println(i);
i = i + 1; // 3

System.out.println(i);
i = i + 1; // 4

System.out.println(i);
i = i + 1; // 5

System.out.println(i);
```

You can use a while loop to do this, but we're trying to learn how to use a for loop, so let's do that. A for loop needs three parts:

1. initialization - where do you want to start. For us, we want to start at 1.
2. condition - this condition should say do this loop as long as this condition is true. The loop will stop as soon as it's false.
3. update statement - what to do after every iteration

```java
for(initialization; condition; update statement) {

}

```

For our code, here are our three parts:

1. initialization - we need to start at 1, so our initialize statement is `int i = 1;`
2. condition - we need to run the loop as long as i is less than or equal to 5 `i <= 5`
3. update statement - after every iteration, add one to i `i = i + 1`

```java
int number = 5;

for(int i = 1; i <= 5; i = i + 1) {
  System.out.println(i);
}
```

Note how nice and clean it is. The code that needs to repeat is in the `{}` of the for loop.

**Pro tip:** `i = i + 1` can be written as `i++`

This is what the condense update statement loops like in the for loop.

Let's go through a few example

## Nested for loop

Let's say if you want to print `*` 10 times. Here's the code for it.

```java
for(int i = 0; i < 10; i++) {
  System.out.print("*");
}
```

This is the result.

```
**********
```

Notice I wanted to repeat the code 10 times. I started with i as 0. This is the common practice because it makes it easier to deal with array. Because I started with 0, instead of saying i is less than or equal to 10, I say do this as long as i is less than 10 `i < 10`. This means it will 0, 1, 2, 3, 4, 5, 6, 7, 8, and 9 which is ten times.

Let's build a rectangle of stars. For example, if the size is 2, then this is the result:

```
**
**
```

Note that if it is size 2, then I have to two rows and each rows has two stars. If the size is 3, then this is the result:

```
***
***
***
```

Ok, now we know what it looks like. Let's make a method for it.

```java
public static void printRectangle(int size) {

}

```

Remember we know how to make one line of star. Let's do that first.

```java
public static void printOneRowOfStars(int size) {
  for(int i = 0; i < size; i++) {
    System.out.print("*");
  }
}
```

Note we need to make n rows of stars for a rectangle of size n. So we need another for loop to make the row.

```java
public static void printRectangle(int size) {
  //loop to make the row
  for(int i = 0; i < size; i++) {

    //call method to print stars
    printOneRowOfStars(size);

    //print new line after every row of stars
    System.out.print('\n');
  }
}
```

Let's put it together:

```java
public static void printRectangle(int size) {
  //loop to make the row
  for(int i = 0; i < size; i++) {

    //loop to print the stars
    for(int j = 0; j < size; j++) {
      System.out.print("*");
    }

    //print new line after every row of stars
    System.out.print('\n');
  }
}
```

This code is the same code as the above. Instead of calling another to print the star, we pulled the code together so it's done in one method. Both code will do the same thing. It is up to you which method you prefer. I prefer the first method because I find the first method easier to read.

## Collecting result

Let's say we want to calculate the factorial of a number. A factorial is a the product of all positive integers less than or equal to the number. For example, the factorial of 5 is `1 x 2 x 3 x 4 x 5`. Here's the code to calculate the factorial of 5.

```java
int factorial = 1 * 2 * 3 * 4 * 5;
```

Let's say you want to calculate the factorial from a user input instead of a specific number. First, you need to create a method that have one parameter. The parameter is the number you want to find the factorial for.

```java
public int factorial(int number) {
//code for factorial  
}
```

Now, how do we translate this code into something more flexible?

```java
int factorial = 1 * 2 * 3 * 4 * 5;
```

This is a common pattern. When you need to do an operation for an unknown number of times, you need to have an accumulator (which is something to collect the result). Let's rewrite the code to something that is repeatable.

```java
// first initialize an accumulator, because this is multiplication you need to initialize it to 1
int result = 1;

// notice we take result and multiply by the number
result = result * 1; // 1 * 1 = 1
result = result * 2; // 1 * 2 = 2
result = result * 3; // 2 * 3 = 6
result = result * 4; // 6 * 4 = 24
result = result * 5; // 24 * 5 = 120

// result is now 120
```

Again, let's rewrite this to make it look the same. First, extract out the thing that change. Then increment it after every loop.

```java
// first initialize an accumulator
int result = 1;

// starts at 1
int i = 1;

//
result = result * i; // 1 * 1 = 1
i++;

result = result * i; // 1 * 2 = 2
i++;

result = result * i; // 2 * 3 = 6
i++;

result = result * i; // 6 * 4 = 24
i++;

result = result * i; // 24 * 5 = 120
i++;


// result is now 120
```
Now we see the thing that repeat, let's rewrite it in a loop. Here are our loop statements:

1. initialization - int i = 1;
2. condition - i <= number
3. update statement - i++ (which is the same as i = i = 1)

```java
public int factorial(int number) {
  // first initialize an accumulator
  int result = 1;

  for (int i = 1; i <= number; i++) {
    result = result * i;
  }
}
```

## Resources
1. [Programiz's tutorial](https://www.programiz.com/java-programming/for-loop)
2. [Oracle's tutorial](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/for.html)
