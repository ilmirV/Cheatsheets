# Learn Kotlin
#### TOPICS
* [Introduction to Kotlin](#intro)
* [Data Types & Variables](#variables)
* [Conditional Expressions](#condition)
* [Collections](#collections)
* [Loops](#loops)
* [Functions](#functions)
* [Classes](#classes)
## Introduction to Kotlin <a name="intro"></a>
### The main() Function
The `main()` function is the starting off point of every Kotlin program and must be included in the code before execution.
```kotlin
fun main() {
  // Code goes here
}
```
### Print Statements
A print statement outputs values to the output terminal.

Using a `println()` statement will create a new line in the output terminal after printing values, while a `print()` statement will not.
```kotlin
println("Greetings, earthling!")
print("Take me to ")
print("your leader.")
 
/* 
Prints:
Greetings, earthling!
Take me to your leader.
*/
```
### Comments
Comments are used to document what is happening inside of a program and are ignored by the compiler.

A single-line comment is used to write a comment on one line, while a multiline comment is used to write longer comments that span over multiple lines.
```kotlin
// This is a single-line comment
 
/*
This
comment
uses
multiple
lines
*/
```
### Order of Execution
Code is read, compiled, and executed in top-down order.
```kotlin
fun main() {
  println("I will be printed first.")
  println("I will be printed second.")
  println("I will be printed third.")
}
```
