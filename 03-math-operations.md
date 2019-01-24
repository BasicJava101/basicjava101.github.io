---
layout: page
title: Math operations
---

You can do mathematical operations on Java numbers and char. Java numbers are byte, short, int, long, float, and decimal.


| Operation | Sign | Example | Result |
|---------- | ---- | ------- | ------ |
| Addition | + | 7 + 8 | 15 |
| Subtraction | - | 7 - 8 | -1 |
| Multiplication | * | 7 * 8 | 56 |
| Division | / | 8/2 | 4 |
| Modulus(/Remainder) | % | 1 % 2 | 1 |

Everything should be easy to understand. Two tricky part are division and modulus. Let's go over them in details.

### Division

When you divide an integer with an integer, then you will get an integer back which means it won't have any decimal.

```
int x = 11;
int y = 2;

int result = 11/2; //result is 5 instead of 5.5

```

What you need to do is turn one of the number into a double.

```
int x = 11;
double y = 2;

int result = 11/2;

```

Or you can cast one of the number into a double.

```
int x = 11;
int y = 2;

int result = (double)11/2;
```

### Modulus

The `%` sign is used to calculate the remainder of a number.

```
4 % 3 // returns 1 because 4 divides by 3 will yields a reminder of 1
5 % 3 // returns 2 because 5 divides by 3 will yields a reminder of 2
6 % 3 // returns 0 because 6 divides evenly into 3, therefore the remainder is 0

```

To check a number is divisible by another number, you check if the remainder is 0.

```
9 % 3 == 0; // 9 is divisible by 0
```

A number is even if it divides evenly into 2. Therefore, to check if it's even, check if the remainder is 0.

```
number % 2 == 0; //number is even
```

A number is odd if it divides by 2 and the remainder is 1.

```
number % 2 == 1; //number is odd
```

## Comparison Operators

<table>
    <thead>
      <tr>
        <th>Example&nbsp;&nbsp;&nbsp;</th>
        <th>Name</th>
        <th>Result</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><code>a == b</code></td>
        <td>Equal</td>
        <td><strong><code>TRUE</code></strong> if <code>a</code> is equal to <code>b</code> (can be different types).</td>
      </tr>
      <tr>
        <td><code>a != b</code></td>
        <td>Not equal</td>
        <td><strong><code>TRUE</code></strong> if <code>a</code> is not equal to <code>b</code> (can be different types).</td>
      </tr>
      <tr>
        <td><code>a &lt; b</code></td>
        <td>Less than</td>
        <td><strong><code>TRUE</code></strong> if <code>a</code> is strictly less than <code>b</code>.</td>
      </tr>
      <tr>
        <td><code>a &gt; b</code></td>
        <td>Greater than</td>
        <td><strong><code>TRUE</code></strong> if <code>a</code> is strictly greater than <code>b</code>.</td>
      </tr>
      <tr>
        <td><code>a &lt;= b</code></td>
        <td>Less than or equal to </td>
        <td><strong><code>TRUE</code></strong> if <code>a</code> is less than or equal to <code>b</code>.</td>
      </tr>
      <tr>
        <td><code>a &gt;= b</code></td>
        <td>Greater than or equal to </td>
        <td><strong><code>TRUE</code></strong> if <code>a</code> is greater than or equal to <code>b</code>.</td>
      </tr>
    </tbody>
  </table>
