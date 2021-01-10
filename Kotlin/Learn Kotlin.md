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
### If Expressions
An `if` expression is a conditional that runs a block of code when its condition has a `true` value.
```kotlin
var morning = true
 
if (morning) {
  println("Rise and shine!")
}
// Prints: Rise and shine!
```
### Else Expressions
An `else` expression is a conditional that runs a block of code only when the conditions contained in the previous expressions have `false` values.
```kotlin
var rained = false
 
if (rained) {
  println("No need to water the plants today.")
} else {
  println("Plants need to be watered!")
}
// Prints: Plants need to be watered!
```
### Else-If Expressions
An `else`-`if` expression allows for more conditions to be evaluated within an `if`/`else` expression.

You can use multiple `else`-`if` expressions as long as they appear after the `if` expression and before the `else` expression.
```kotlin
var age = 65
 
if (age < 18 ) {
  println("You are considered a minor.")
} else if (age < 60) {
  println("You are considered an adult.")
} else {
  println("You are considered a senior.")
}
 
// Prints: You are considered a senior.
```
### Comparison Operators
Comparison operators are symbols that are used to compare two values in order to return a result of `true` or `false`. Comparison operators include `>`, `<`, `>=`, `<=`.
```kotlin
var myAge = 19
var sisterAge = 11
var cousinAge = 11
 
myAge > sisterAge  // true
myAge < cousinAge  // false
myAge >= cousinAge // true
myAge <= sisterAge // false
```
### Logical Operators
Logical operators are symbols used to evaluate the relationship between two or more Boolean expressions in order to return a `true` or `false` value.

Logical operators include `!`, `&&`, and `||`.
```kotlin
var humid = true
var raining = true
var jacket = false
 
println(!humid)
// Prints: false
 
println(jacket && raining)
// Prints: true
 
println(humid || raining)
// Prints: true
```
### The AND Operator: &&
The logical AND operator (`&&`) is used to compare the relationship between two Boolean expressions and will only return a `true` value if both expressions are `true`.
```kotlin
var humid = true
var raining = true
var shorts = false
var sunny = false
 
// true AND true
println(humid && raining) //  true
 
// true AND false
println(humid && shorts) //  false
 
// false AND true
println(sunny && raining) //  false
 
// false AND false
println(shorts && sunny) // false
```
### The OR Operator : ||
The logical OR operator (`||`) is used to compare the relationship between two Boolean expressions and will return `true` when at least one of the expressions are `true`.
```kotlin
var late = true
var skipBreakfast = true
var underslept = false
var checkEmails = false
 
 
// true OR true
println(skipBreakfast || late) //  true
 
// true OR false
println(late || checkEmails) //  true
 
// false OR true
println(underslept || late) //  true
 
// false OR false
println(checkEmails || underslept) // false
```
### The NOT Operator: !
The logical NOT operator (`!`) evaluates the value of a Boolean expression and then returns its negated value.
```kotlin
var hungry = true
var full = false
 
println(!hungry) //  false
println(!full) //  true
```
### Order of Evaluation
The order of evaluation when using multiple logical operators in a single Boolean expression is:

Expressions placed in parentheses.
NOT(`!`) operator.
AND(`&&`) operator.
OR(`||`) operator.
```kotlin
!true && (false || true) // false
/*
(false || true) is evaluated first returning true. Then,
!true && true is evaluated returning the final result, false. 
*/
 
!false && true || false // true
/*
!false is evaluated first returning true. Then true && true are evaluated, returning true. Then, true || false is evaluated which ends up returning true.
*/
```
### Nested Conditionals
A nested conditional is a conditional that exists within another conditional.
```kotlin
var studied = true
var wellRested = true
 
if (wellRested) {
    println("Best of luck today!")  
  if (studied) {
    println("You should be prepared for your exam!")
  } else {
    println("Take a few hours to study before your exam!")
  }
}
 
// Prints: Best of luck today!
// Prints: You should be prepared for your exam!
```
### When Expressions
A `when` expression controls the flow of code by evaluating the value of a variable in order to determine what code gets executed.
```kotlin
var grade = "A"
 
when(grade) {
  "A" -> println("Excellent job!")
  "B" -> println("Very well done!")
  "C" -> println("You passed!")
  else -> println("Close! Make sure to perpare more next time!")
}
// Prints: Excellent job!
```
### The Range Operator
The range operator (`..`) is used to create a succession of number or character values.
```kotlin
var height = 46 // inches
 
if (height in 1..53) {
  println("Sorry, you must be at least 54 inches to ride the rollercoaster.")
}
// Prints: Sorry, you must be at least 54 inches to ride the rollercoaster.
```
### Equality Operators
Equality operators are symbols that are used to compare the equivalence of two values in order to return `true` or `false`. Equality operators include `==` and `!=`.
```kotlin
var myAge = 22
var sisterAge = 21
 
myAge == sisterAge // false
myAge !== sisterAge // true
```
## Collections <a name="collections"></a>
## Loops <a name="loops"></a>
## Functions <a name="functions"></a>
## Classes <a name="classes"></a>
