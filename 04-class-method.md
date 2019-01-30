---
layout: page
title: Anatomy of a method
---

Let's write our first program. Create a new file and copy this code into the file.

```java
public class FirstClass {

    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

This code will prints out `Hello, World!`. Let's dissect this code.

## Class
First, let's talk about the class. Here we have a class named `FirstClass`.

```java
public class FirstClass {

}
```

In Java, you have to write your code inside a class. Think of a class as a container for your actual code. To create a class you need to specify three things:

- **Access modifier** `public` - also call accessor. This defines the visibility of the class. It could be public, protected, or default. We will go more into this later.
- **`class`** - this is a keyword. In Java, keywords have special meanings. You can't use it for variable name or class name.
- **class name** `FirstClass` - this is the name of the class. You can name it anything you want. By convention, each word in the name is capitalized. This naming convention is called camel case.
- `{}` - open and close curly braces. Place your actual code inside these curly braces.   

To iterate, a class signature looks like this:

```
[access modifier] class [class name] {

}
```

## Method

Now, let's talk about the method.

```java
public static void main(String[] args) {

}
```

In general, you need to put your code inside a method. A class can have multiple methods. A method needs the following:

- **access modifier** `public` - defines the visibility of the class.
- **static** - this is a keyword. This is optional. We'll go over this keyword more when we talk about object.
- **return type** `void` - what type of data this method returns. `void` means this method doesn't return anything.
- **method name** `main` - similar to variable, you can name the method anything you want. By convention, it should starts with lower case. Each word after is capitalized. For example `public static void printGreeting`.
- **arguments/inputs** `String[] args`- each method can have zero, one, or more input. Our main method has one input. It is an array of String. We will go over this type later. Don't worry about this right now.

To iterate, a class method signature looks like this:

```
[access modifier] static [return type] [method name]([inputs]) {

}
```

### Multiple arguments/inputs
If we want a method to multiple two numbers and return a number, this is the signature:

```
public static double multiply(double x, double y) {

}
```

### Different arguments/inputs and return type
If we want to take in a number and check to see if it's even by returning true or false, then this is the signature:

```
public static boolean isEven(int number) {

}
```

### No arguments/inputs or return type

If we want a method that doesn't have any input or return any input, then this is the method signature:

```
public static void printGreeting() {

}
```

## The main method

The main method is a special method. This is where your program begins executing your code. The method signature should always be like this:
```java
public static void main(String[] args) {

}
```

`String[] args` Used for command line arguments that are passed as strings. We will cover that in a separate post.

## The code

This method prints the contents inside the double quotes into the console and inserts a newline after.

```java
System.out.println("This is my first program in java");
```

## Naming

Remember Java is case sensitive. If you named your method `addNumbers`, then


## Task

Now, edit the code to prints out `Hello, [your name]!`. For example, my name is Nhu. My code will look like this.

```java
public class FirstClass {

    public static void main(String[] args) {
        System.out.println("Hello, Nhu!");
    }
}
```
