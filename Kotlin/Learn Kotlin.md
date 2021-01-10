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
## Data Types & Variables <a name="variables"></a>
### Mutable Variables
A mutable variable is declared with the `var` keyword and represents a value that is expected to change throughout a program.
```kotlin
var age = 25
age = 26
```
### Immutable Variables
An immutable variable is declared with the `val` keyword and represents a value that must remain constant throughout a program.
```kotlin
val goldenRatio = 1.618
```
### Type Inference
When a data type is not specified in a variable declaration, the variable’s data type can be inferred through type inference.
```kotlin
// The following variable is assigned a text value within double quotes, thus the inferred type is String 
 
var color = "Purple"
```
### String Concatenation
String concatenation is the process of combining Strings using the `+` operator.
```kotlin
var streetAddress = "123 Main St."
var cityState = "Brooklyn, NY" 
 
println(streetAddress + " " + cityState) 
// Prints: 123 Main St. Brooklyn, NY
```
### String Templates
String templates contain String values along with variables or expressions preceded by a `$` symbol.
```kotlin
var address = "123 Main St. Brooklyn, NY"
println("The address is $address") 
// Prints: The address is 123 Main St. Brooklyn, NY
```
### Built-in Properties and Functions
The Kotlin String and Character data types contain various built-in properties and functions. The `length` property returns the number of characters in a String, and the `capitalize()` function capitalizes the first letter of a String.
```kotlin
var monument = "the Statue of Liberty"
 
println(monument.capitalize()) // Prints: The Statue of Liberty
println(monument.length) // Prints: 21
```
### Character Escape Sequences
Character escape sequences consist of a backslash and character and are used to format text.

* `\n` Inserts a new line
* `\t` Inserts a tab
* `\r` Inserts a carriage return
* `\'` Inserts a single quote
* `\"` Inserts a double quote
* `\\` Inserts a backslash
* `\$` Inserts the dollar symbol
```kotlin
print("\"Excellent!\" I cried. \"Elementary,\" said he.") 
 
// Prints: "Excellent!" I cried. "Elementary," said he.
```
### Arithmetic Operators
The arithmetic operators supported in Kotlin include `+` addition, `-` subtraction, `*` multiplication, `/` division, and `%` modulus.
```kotlin
5 + 7  // 12
9 - 2  // 7
8 * 4  // 32
25 / 5 // 5 
31 % 2 // 1
```
### Order of Operations
The order of operations for compound arithmetic expressions is as follows:

1. Parentheses
2. Multiplication
3. Division
4. Modulus
5. Addition
6. Subtraction

When an expression contains operations such as multiplication and division or addition and subtraction side by side, the compiler will evaluate the expression in a left to right order.
```kotlin
5 + 8 * 2 / 4 - 3 // 6 
3 + (4 + 4) / 2   // 7
4 * 2 + 1 * 7     // 15
3 + 18 / 2 * 1    // 12  
6 - 3 % 2 + 2     // 7
```
### Augmented Assignment Operators
An augmented assignment operator includes a single arithmetic and assignment operator used to calculate and reassign a value in one step.
```kotlin
var batteryPercentage = 80
 
// Long Syntax 
batteryPercentage = batteryPercantage + 10 
 
// Short Syntax with an Augmented Assignment Operator 
batteryPercentage += 10
```
### Increment and Decrement Operators
Increment and decrement operators provide a shorthand syntax for adding or subtracting `1` from a value. An increment operator consists of two consecutive plus symbols, `++`, meanwhile a decrement operator consists of two consecutive minus symbols, `--`.
```kotlin
var year = 2019 
year++ // 2020
year-- // 2019
```
### The Math Library
The `Math` library, inherited from Java, contains various mathematical functions that can be used within a Kotlin program.
```kotlin
Math.pow(2.0, 3.0)  // 8.0
Math.min(6, 9)      // 6 
Math.max(10, 12)    // 12
Math.round(13.7)    // 14
```
## Conditional Expressions <a name="condition"></a>
## Collections <a name="collections"></a>
## Loops <a name="loops"></a>
## Functions <a name="functions"></a>
## Classes <a name="classes"></a>
