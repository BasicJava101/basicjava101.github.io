---
layout: page
title: While Loop
---

When you need to do something over and over again, you can often use a loop for it. For example, here's the code to print out from 1 to 5

```java
System.out.println(1);
System.out.println(2);
System.out.println(3);
System.out.println(4);
System.out.println(5);

```

Notice that you're doing the same thing over and over again. The only thing that changed is the number. So let's  extract that number and store it in a variable to make the print statement look the same.

```java
int x = 1;
System.out.println(x);
System.out.println(x);
System.out.println(x);
System.out.println(x);
System.out.println(x);

```

This code doesn't work. This will print out 1 every single time. As you can see from above, the number need to increase by 1 after every print statement. Let's add 1 after every print statement.

```java
int x = 1; // 1

System.out.println(x);
x = x + 1; // 2

System.out.println(x);
x = x + 1; // 3

System.out.println(x);
x = x + 1; // 4

System.out.println(x);
x = x + 1; // 5

System.out.println(x);
```

Because developers are lazy, whenever we need to repeat something, we usually find a way to DRY (don't-repeat-yourself) it. One of the way to not repeat yourself is to use a while loop. This code below does the same thing as the code above. Here are the steps to turn the code into a loop:

1. Initialize a variable to control the loop
2. Tell the while loop when to stop looping
3. Add the code you need to repeat in the `{}` of the while loop

```java
// 1. initialize your variable
int x = 1;

// 2. Tell the while loop when to stop.
// This statement reads, repeat the code in the block while x is greater or equal to 5
// the system will stop executing the code in the block when x is greater than 5
while (x <= 5) {

  //repeatedly print out x
  System.out.println(x);

  //after every single print statement, increate x by 1
  x = x + 1;

}
```

If at some point you want to break out of the loop, you can use the keyword `break`. For example, instead of a condition, we use true so the loop will execute forever. But we don't want to execute the code forever, we need to stop it after a certain time. In this code below we will print `hello` and increment the count. But after count reaches 3, we want to stop. So here's the ugly code for it.

```java

int count = 0;
while(true) {
  System.out.println("hello");
  count++;

  if (count == 3) {
    break;
  }
}

```

Instead of breaking, you can also have a variable to store whether or not you should print `hello`. Then as soon as count is 3 which is when we want to stop printing, we change the variable to false.

```java

int count = 0;
boolean print = true;

while(print) {
  System.out.println("hello");
  count++;

  if (count == 3) {
    print = false;
  }
}

```

This is especially helpful when you write game. For example:

```java
Game game = new Game();

// the ! means not so the statement read while the game is not over, execute this code
while(!game.isOver()) {
  //play game
}
```
