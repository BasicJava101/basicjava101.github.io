---
layout: page
title: If & Switch
---

There are times when you want to do something only when a certain condition is true. In this case, you need to use a `if` statement.

```java
int age = 18;

// only print out this statement if the person age is greater than or equal to 18
if (age >= 18) {
    System.out.println("You're an adult.");
    System.out.println("Pay the bills!😆");
}

```

The format for an if statement is this:

```java
if (condition that return a boolean) {
  //code you want to do if condition is true
}
```

It doesn't always have to be a comparison statement. As long as what is in the parenthesis is a boolean.

```java
boolean isStudent = true;

if (isStudent) {
  System.out.println("Do your labs!😆");
}
```

You can use a bang sign (exclamation point !) to test a false condition. For example, if we only have the variable `isStudent`, but we want to say, if NOT student, then we can use the `!` sign.

```java
boolean isStudent = true;

//note the ! which states if NOT student
if (!isStudent) {
  System.out.println("Take a vacation! 🌴");
}
```

## Else

There are times when you want to say, if this is true, then do this, otherwise, do this other thing. When you need an if or else situation like that, you need an `if-else` statement.

```java
int age = 17;

if (age >= 18) {
    // only print out this statement if the person age is greater than or equal to 18
    System.out.println("You're an adult.");
    System.out.println("Pay the bills!😆");
} else {
    // otherwise, print this statement
    System.out.println("Here's some allowance!🤑");
}
```

The allowance statement will only print out if the age is less than 18. If you have only two situation where it is if this, otherwise that, then use this statement. The format is this:

```java
if (condition that return a boolean) {
  //code you want to do if condition is true
} else {
  // code for when condition is false
}
```

## Else If

If you have a case when there is two condition, then you can use `else if`. For example, if the person age is 18 or greater, you want the person to pay the bills. If the person is less then 18, then you want to give them allowance. But a baby/toddler doesn't need allowance, so you want to say, if the person is >= 18, pay the bills. If the person is older than 5, then they get an allowance.

```java
int age = 17;

if (age >= 18) {
    // only print out this statement if the person age is greater than or equal to 18
    System.out.println("You're an adult.");
    System.out.println("Pay the bills!😆");
} else if(age > 5) {
    // only print this if the person age is greater than 5 but less than 18.
    System.out.println("Here's some allowance!🤑");
}
```

Notice that if age is 5 or younger, then it doesn't print out anything. Unlike the `else` statement which executes when the condition is false. The `else if` statement only execute if the second condition is true. Because the if statement executes first, thus when it gets to the `else if` statement, it will never be 18+.

We can combine the if, else if, and else statement together.

```java
int age = 3;

if (age >= 18) {
    // only print out this statement if the person age is greater than or equal to 18
    System.out.println("You're an adult.");
    System.out.println("Pay the bills!😆");
} else if(age > 5) {
    // only print this if the person age is greater than 5 but less than 18.
    System.out.println("Here's some allowance!🤑");
} else {
    // if the other two condition is false, then execute this
    System.out.println("You're a baby! Here are some candies 🍫");
}
```

You can have multiple `else if` condition, but you can only have one else statement. Here's an example:

```java
int age = 23;

if (age >= 25) {
    System.out.println("You're an adult.");
    System.out.println("Pay the bills!😆");
} else if (age > 6) {
    // only print out this statement if the person age is greater than or equal to 18
    System.out.println("Go to class! 🏫");
} else if(age > 5) {
    // only print this if the person age is greater than 5 but less than 18.
    System.out.println("Here's some allowance!🤑");
} else {
    // if the other two condition is false, then execute this
    System.out.println("You're a baby! Here are some candies 🍫");
}
```

You can read more about if statement on [Oracle's website](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/if.html).

## Switch

A switch case is similar to an if else statement. However, instead of greater than or less than, it only compare if the value is the exact value. For example, given this if statement,

```java
int year = 100;

if(year == 100) {
    //only do this if year == 100
    System.out.println("century");
} else if (year == 10){
    //only do this if year == 10
    System.out.println("decade");
} else {
    // if it doesn't match any of the other case
    System.out.println("Nothing special");
}
```

We can convert it to a switch statement.

```java
int year = 100;

 switch (year) {
     case 100:
         //only do this if year == 100
         System.out.println("century");
         //have to break else it will go down to the other cases
         break;
     case 10:
         //only do this if year == 10
         System.out.println("decade");
         //have to break else it will go down to the other cases
         break;
     default:
         // if it doesn't match any of the other case
         System.out.println("Nothing special");
         //doesn't need to break because this is the last statement
 }
 ```
