# Learn Swift
#### TOPICS
* [Hello World](#hello)
* [Variables](#variables)
* [Conditionals & Logic](#condition)
* [Loops](#loops)
* [Arrays & Sets](#arrays)
* [Dictionaries](#dictionaries)
* [Functions](#functions)
* [Structures](#structures)
* [Classes](#classes)
## Hello World <a name="hello"></a>
### print()
The `print()` function outputs one or more values to the terminal.
```swift
print("Hello, world!")
 
// Prints: Hello, world!
```
### Program Structure
The program runs line by line, from top to bottom:

* Line 1 prints `Hola`
* Line 2 prints `Buenos días`
```swift
print("Hola")
print("Buenos días")
```
Single-line Comments
Single-line comments are created using two consecutive forward slashes. The compiler ignores any text after `//` on the same line.
```swift
// This line denotes a comment in Swift.
```
### Multiline Comments
Multiline comments are created using `/*` to begin the comment, and `*/` to end the comment. The compiler ignores any text in between.
```swift
/* 
This is all commented out.
None of it is going to run!
*/
```
## Variables <a name="variables"></a>
### Variables
A variable refers to a storage location in the computer’s memory that one can set aside to save, retrieve, and manipulate data.
```swift
var score = 0
```
### Constants
Constants refer to fixed values that a program may not alter during its execution. One can be declared by using the `let` keyword.
```swift
let pi = 3.14
```
### Arithmetic Operators
Swift supports arithmetic operators for:

* `+` addition
* `-` subtraction
* `*` multiplication
* `/` division
* `%` remainder
```swift
var x = 0
 
x = 4 + 2  // x is now 6
x = 4 - 2  // x is now 2
x = 4 * 2  // x is now 8
x = 4 / 2  // x is now 2
x = 4 % 2  // x is now 0
```
### Types
Type annotation can be used during declaration.

The basic data types are:

* `Int`: integer numbers
* `Double`: floating-point numbers
* `String`: a sequence of characters
* `Bool`: truth values
```swift
var age: Int = 28
 
var price: Double = 8.99
 
var message: String = "good nite"
 
var lateToWork: Bool = true
```
### String Interpolation
String interpolation can be used to construct a `String` from a mix of variables, constants, and others by including their values inside a string literal.
```swift
var apples = 6
 
print("I have \(apples) apples!")
 
// Prints: I have 6 apples!
```
### Compound Assignment Operators
Compound assignment operators provide a shorthand method for updating the value of a variable:

* `+=` add and assign the sum
* `-=` subtract and assign the difference
* `*=` multiply and assign the product
* `/=` divide and assign the quotient
* `%=` divide and assign the remainder
```swift
var numberOfDogs = 100
numberOfDogs += 1
 
print("There are \(numberOfDogs) dalmations!")
 
// Prints: There are 101 dalmations!
```
## Conditionals & Logic <a name="condition"></a>
### if Statement
An `if` statement executes a code block when its condition evaluates to `true`. If the condition is `false`, the code block does not execute.
```swift
var halloween = true 
 
if halloween {
  print("Trick or treat!")
}
 
// Prints: Trick or treat! 
```
### else Statement
An `else` statement is a partner to an `if` statement. When the condition for the `if` statement evaluates to `false`, the code within the body of the `else` will execute.
```swift
var turbulence = false 
 
if turbulence {
  print("Please stay seated.")
} else {
  print("You may freely move around.")
}
 
// Prints: You may freely move around.
```
### else if Statement
An `else if` statement provides additional conditions to check for within a standard `if`/`else` statement. `else if` statements can be chained and exist only after an `if` statement and before an `else`.
```swift
var weather = "rainy" 
 
if weather == "sunny" {
  print("Grab some sunscreen")
} else if weather == "rainy" {
  print("Grab an umbrella")
} else if weather == "snowing" {
  print("Wear your snow boots")
} else {
  print("Invalid weather")
}
 
// Prints: Grab an umbrella
```
### Comparison Operators
Comparison operators compare the values of two operands and return a Boolean result:

* `<` less than
* `>` greater than
* `<=` less than or equal to
* `>=` greater than or equal to
* `==` equal to
* `!=` not equal to
```swift
5 > 1       // true 
6 < 10      // true 
2 >= 3      // false
3 <= 5      // true
"A" == "a"  // false
"B" != "b"  // true
```
### Ternary Conditional Operator
The ternary conditional operator, denoted by a `?`, creates a shorter alternative to a standard `if`/`else` statement. It evaluates a single condition and if `true`, executes the code before the `:`. If the condition is `false`, the code following the `:` is executed.
```swift
var driverLicense = true
 
driverLicense ? print("Driver's Seat") : print("Passenger's Seat") 
 
// Prints: Driver's Seat
```
### switch Statement
The `switch` statement is a type of conditional used to check the value of an expression against multiple cases. A `case` executes when it matches the value of the expression. When there are no matches between the `case` statements and the expression, the `default` statement executes.
```swift
var secondaryColor = "green"
 
switch secondaryColor {
  case "orange":
    print("Mix of red and yellow")
  case "green":
    print("Mix of blue and yellow")
  case "purple":
    print("Mix of red and blue") 
  default: 
    print("This might not be a secondary color.") 
}
 
// Prints: Mix of blue and yellow
```
### switch Statement: Interval Matching
Intervals within a `switch` statement’s `case` provide a range of values that are checked against an expression.
```swift
let year = 1905
var artPeriod: String
 
switch year {
  case 1860...1885:
    artPeriod = "Impressionism"
  case 1886...1910:
    artPeriod = "Post Impressionism"
  case 1912...1935: 
    artPeriod = "Expressionism"
  default:  
    artPeriod = "Unknown"
}
 
// Prints: Post Impressionism
```
### switch Statement: Compound Cases
A compound case within a `switch` statement is a single `case` that contains multiple values. These values are all checked against the `switch` statement’s expression and are separated by commas.
```swift
let service = "Seamless"
 
switch service {
  case "Uber", "Lyft":
    print("Travel")
  case "DoorDash", "Seamless", "GrubHub":
    print("Restaurant delivery")
  case "Instacart", "FreshDirect":
    print("Grocery delivery")
  default: 
    print("Unknown service")
}
 
// Prints: Restaurant delivery
```
### switch Statement: where Clause
Within a `switch` statement, a `where` clause is used to test additional conditions against an expression.
```swift
let num = 7
 
switch num {
  case let x where x % 2 == 0:
    print("\(num) is even")
  case let x where x % 2 == 1:
    print("\(num) is odd")
  default:
    print("\(num) is invalid")
}
 
// Prints: 7 is odd
```
### Logical Operator !
The logical NOT operator, denoted by a `!`, is a prefix operator that negates the value on which it is prepended. It returns `false` when the original value is `true` and returns `true` when the original value is `false`.
```swift
!true          // false
!false         // true
```
### Logical Operator &&
The logical AND operator, denoted by an `&&`, evaluates two operands and returns a Boolean result. It returns `true` when both operands are `true` and returns `false` when at least one operand is `false`.
```swift
true && true    // true
true && false   // false 
false && true   // false 
false && false  // false
```
### Logical Operator ||
The logical OR operator, denoted by `||`, evaluates two operands and returns a Boolean result. It returns `false` when both operands are `false` and returns `true` when at least one operand is `true`.
```swift
true || true    // true
true || false   // true
false || true   // true 
false || false  // false
```
### Combining Logical Operators
Logical operators can be chained in order to create more complex logical expressions. When logical operators are chained, it’s important to note that the `&&` operator has a higher precedence over the `||` operator and will get evaluated first.
```swift
!false && true || false  // true
 
/* 
!false && true evaluates first and returns true. Then, the expression, true || false evaluates and returns the final result, true. 
*/ 
 
false || true && false   // false
 
/* 
true && false evaluates first which returns false. Then, the expression, false || false evaluates and returns the final result, false. 
*/
```
### Controlling Order of Execution
Within a Swift logical expression, parentheses, `()`, can be used to organize and control the flow of operations. The usage of parentheses within a logical expression overrides operator precedence rules and improves code readability.
```swift
// Without parentheses:
 
true || true && false || false      // true 
 
// With parentheses:
 
(true || true) && (false || false)  // false
```
## Loops <a name="loops"></a>
### Ranges
Ranges created by the `...` operator will include the numbers from the lower bound to (and includes) the upper bound.
```swift
let zeroToThree = 0...3
 
// zeroToThree: 0, 1, 2, 3
```
### stride() Function
Calling `stride()` with the 3 necessary arguments creates a collection of numbers; the arguments decide the starting number to, the (excluded) ending number, and how to increment/decrement from the start to the end.
```swift
for oddNum in stride(from: 1, to: 5, by: 2) {
  print(oddNum)
}
 
// Prints: 1
// Prints: 3
```
### for-in Loop
The `for`-`in` loop is used to iterate over collections, including strings and ranges.
```swift
for char in "hehe" {
  print(char)
}
 
// Prints: h
// Prints: e
// Prints: h
// Prints: e
```
### continue Keyword
The `continue` keyword will force the loop to move on to the next iteration.
```swift
for num in 0...5 {
  if num % 2 == 0 {
    continue
  }
  print(num)
}
 
// Prints: 1
// Prints: 3
// Prints: 5
```
### break Keyword
To terminate a loop before its completion, use the `break` keyword.
```swift
for char in "supercalifragilisticexpialidocious" {
  if char == "c" {
    break
  }
  print(char)
}
 
// Prints: s
// Prints: u
// Prints: p
// Prints: e
// Prints: r
```
### Using Underscore
Use `_` instead of a placeholder variable if the variable is not referenced in the `for`-`in` loop body.
```swift
for _ in 1...3 {
  print("Olé")
}
 
// Prints: Olé
// Prints: Olé
// Prints: Olé
```
### while Loop
A `while` loop accepts a condition and continually executes its body’s code for as long as the provided condition is `true`.

If the condition is never `false` then the loop continues to run and the program is stuck in an infinite loop.
```swift
var counter = 1
var stopNum = Int.random(in: 1...10)
 
while counter < stopNum {
  print(counter)
  counter += 1
}
 
// The loop prints until the stop condition is met
```
## Arrays & Sets <a name="arrays"></a>

## Dictionaries <a name="dictionaries"></a>

## Functions <a name="functions"></a>

## Structures <a name="structures"></a>

## Classes <a name="classes"></a>
