---
layout: page
title: Error & Exception Handling
---

An exception or error is an event that occurs during the execution of a program which disrupts the 
normal flow of the appliction.

Testing your application is very important but, when it comes to large scale programs, you cannot account
for all the ways a user will interact with the application which may result in errors and exceptions.

Therefore, Error and Exception handling is crucial to maintaining a healthy application.

The #1 thing you should focus on is handling your errors and exceptions **GRACEFULLY**. Resources are being utilized within the application and you will want to make sure that you allow the user
to exit and recover these resources properly without your appliction entering an error state.

**“It is an error to not handle an exception.”
Henning Thielemann**

## Errors

```
When there is no way to recover/continue gracefully and usually the programmer 
needs to change code/fix bug in order to get the program to start performing properly.
```

If written correctly, an error can sometimes be turned into and handled as an Exception. 

## Exceptions

```
Exceptions are thrown and caught so that an appliction can recover and handle the 
situation without entering an error state. An exceptional situation should not break your 
appliction!
```

**An unhandled exception is known as an ERROR. Therefore, handle your exceptions gracefully to avoid
errors.**

Java exception handling is managed via five keywords: 
- **Try :** If an exception occurs within the try block, that exception is handled by the exception handler associated with it.

- **Catch :** : To associate an exception handler put catch block after it.

- **Throw :** The throw keyword in Java is used to explicitly throw an exception from a method or any block of code. 
We can throw either checked or unchecked exception. 
*The throw keyword is mainly used to throw custom exceptions.*

**The flow of execution of the program stops immediately after the throw statement is executed 
and the nearest enclosing try block is checked to see if it has a catch statement that matches 
the type of exception. If it finds a match, controlled is transferred to that statement 
otherwise next enclosing try block is checked and so on.**

*If no matching catch is found then 
the default exception handler will halt the program.*


- **Throws :** throws is a keyword in Java which is used in the signature of method to 
indicate that this method might throw one of the listed type exceptions.

```
class Example  
{ 
    public static void main(String[] args)throws InterruptedException 
    { 
        System.out.println("This method could raise an exception"); 
    } 
} 
```
- **Finally :** The finally block *always* gets executed whether an exception occurred in the try block or not. 
If an exception occurs, then it will be executed after the try and catch blocks. 
If an exception does not occur then it will be executed after the try block. 
*The finally block is used 
to put important codes such as clean up code (Closing the file or closing the connection.)*

**The finally block is optional and there can only be one.**

```
try {
// block of code to monitor for errors
// the code you think can raise an exception
}
catch (ExceptionType1 e) {
// exception handler for ExceptionType1
}
catch (ExceptionType2 e) {
// exception handler for ExceptionType2
}
// optional
finally {
// block of code to be executed after try block ends
}
```



Default Exception Handling

- **Default Exception Handling:** Whenever inside a method, if an exception has occurred, the method creates an Object known as 
Exception Object and hands it off to the run-time system (JVM). The exception object contains name and description of the exception, and current state of the program where exception has occurred. Creating the Exception Object and handling it to the run-time system is called throwing an Exception.

- **Call Stack:** There might be the list of the methods that had been called to get to the method where exception was occurred.

- **Exception Handler:** The block of code in a method that can handle the occurred exception.

- If run-time system searches all the methods on call stack and doesnt find an Exception Handler 
 that can appropriately handle the given exception then the run-time system defaults.
 The default exception handler thenn prints the exception information in the following format and terminates program **abnormally**.

```
Exception in thread "xxx" Name of Exception : Description
... ...... ..  // Call Stack
```


## Logging
Errors should be logged so that they can be looked at by a developer. 
Logs help give further insight into 
how to fix the error.

Logging your error takes frustrated users out of the mix and allows your team to be 
proactive when something goes wrong.

**Only 1% of users report errors**

So, dont wait for people to report your errors or to stop using your application - be proactive and check 
your logs!