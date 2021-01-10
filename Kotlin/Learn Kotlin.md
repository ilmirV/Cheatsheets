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
### Immutable Lists
An immutable list represents a group of elements with read-only operations.

It can be declared with the term `listOf`, followed by a pair of parentheses containing elements that are separated by commas.
```kotlin
var programmingLanguages = listOf("C#", "Java", "Kotlin", "Ruby")
```
### Mutable Lists
A mutable list represents a collection of ordered elements that possess read and write functionalities.

It can be declared with the term, `mutableListOf` followed by a pair of parentheses containing elements that are separated by commas.
```kotlin
var fruits = mutableListOf("Orange", "Apple", "Banana", "Mango")
```
### Accessing List Elements
In order to retrieve an element from a list, we can reference its numerical position or index using square bracket notation.

**Note:** Remember that the first element of a list starts at `0`.
```kotlin
var cars = listOf("BMW", "Ferrari", "Volvo", "Tesla")
 
println(cars[2]) // Prints: Volvo
```
### The Size Property
The `size` property is used to determine the number of elements that exist in a collection.
```kotlin
var worldContinents = listOf("Asia", "Africa", "North America", "South America", "Antarctica", "Europe", "Australia")
 
println(worldContinents.size) // Prints: 7
```
### List Operations
The list collection supports various operations in the form of built-in functions that can be performed on its elements.

Some functions perform read and write operations, whereas others perform read-only operations.

The functions that perform read and write operations can only be used on mutable lists while read-only operations can be performed on both mutable and immutable lists.
```kotlin
var seas = listOf("Black Sea", "Caribbean Sea", "North Sea") 
println(seas.contains("North Sea")) // Prints: true
 
// The contains() function performs a read operation on any list and determines if an element exists.  
 
seas.add("Baltic Sea") // Error: Can't perform write operation on immutable list
 
// The add() function can only be called on a mutable list thus the code above throws an error.
```
### Immutable Sets
An immutable set represents a collection of unique elements in an unordered fashion whose contents cannot be altered throughout a program.

It is declared with the term, `setOf`, followed by a pair of parentheses holding unique values.
```kotlin
var primaryColors = setOf("Red", "Blue", "Yellow")
```
### Mutable Sets
A mutable set represents a collection of ordered elements that possess both read and write functionalities.

It is declared with the term, `mutableSetOf`, followed by a pair of parentheses holding unique values.
```kotlin
var womenInTech = mutableSetOf("Ada Lovelace",  "Grace Hopper",  "Radia Perlman",  "Sister Mary Kenneth Keller")
```
### Accessing Set Elements
Elements in a set can be accessed using the `elementAt()` or `elementAtOrNull()` functions.

The `elementAt()` function gets appended onto a set name and returns the element at the specified position within the parentheses.

The `elementAtOrNull()` function is a safer variation of the `elementAt()` function and returns `null` if the position is out of bounds as opposed to throwing an error.
```kotlin
var companies = setOf("Facebook", "Apple", "Netflix", "Google")
 
println(companies.elementAt(3)) // Prints: Google
 
println(companies.elementAt(4)) // Returns and Error
 
println(companies.elementAtOrNull(4)) // Prints: null
```
### Immutable Maps
An immutable Map represents a collection of entries that cannot be altered throughout a program.

It is declared with the term, `mapOf`, followed by a pair of parentheses. Within the parentheses, each key should be linked to its corresponding value with the to keyword, and each entry should be separated by a comma.
```kotlin
var averageTemp = mapOf("winter" to 35,  "spring" to 60,  "summer" to 85, "fall" to 55)
```
### Mutable Maps
A mutable map represents a collection of entries that possess read and write functionalities. Entries can be added, removed, or updated in a mutable map.

A mutable map can be declared with the term, `mutableMapOf`, followed by a pair of parentheses holding key-value pairs.
```kotlin
var europeanDomains = mutableMapOf("Germany" to "de", "Slovakia" to "sk", "Hungary" to "hu", "Norway" to "no")
```
### Retrieving Map Keys and Values
Keys and values within a map can be retrieved using the `.keys` and `.values` properties.

The `.keys` property returns a list of key elements, whereas the `.values` property returns a list of value elements.

To retrieve a single value associated with a key, the shorthand, `[key]`, syntax can be used.
```kotlin
var oscarWinners = mutableMapOf("Parasite" to "Bong Joon-ho", "Green Book" to "Jim Burke", "The Shape Of Water" to "Guillermo del Toro")
 
println(oscarWinners.keys)
// Prints: [Parasite, Green Book, The Shape Of Water]
 
println(oscarWinners.values)
// Prints: [Bong Joon-ho, Jim Burke, Guillermo del Toro]
 
println(oscarWinners["Parasite"])
// Prints: Bong Joon-ho
```
### Adding and Removing Map Entries
An entry can be added to a mutable map using the `put()` function. Oppositely, an entry can be removed from a mutable map using the `remove()` function.

The `put()` function accepts a key and a value separated by a comma.

The `remove()` function accepts a key and removes the entry associated with that key.
```kotlin
var worldCapitals = mutableMapOf("United States" to "Washington D.C.", "Germany" to "Berlin", "Mexico" to "Mexico City", "France" to "Paris")
 
worldCapitals.put("Brazil", "Brasilia")
println(worldCapitals)
// Prints: {United States=Washington D.C., Germany=Berlin, Mexico=Mexico City, France=Paris, Brazil=Brasilia}
 
worldCapitals.remove("Germany")
println(worldCapitals)
// Prints: {United States=Washington D.C., Mexico=Mexico City, France=Paris, Brazil=Brasilia}
```
## Loops <a name="loops"></a>
Sorry! Looks like this cheatsheet isn't available yet.
## Functions <a name="functions"></a>
### Functions
A function is a named, reusable block of code that can be called and executed throughout a program.

A function is declared with the `fun` keyword, a function name, parentheses containing (optional) arguments, as well as an (optional) return type.

To call/invoke a function, write the name of the function followed by parentheses.
```kotlin
fun greet() {
  println("Hey there!")
}
 
fun main() {
  // Function call
  greet() // Prints: Hey, there!
}
```
### Function Arguments
In Kotlin, an argument is a piece of data we can pass into a function when invoking it.

To pass data into a function, the function’s header must include parameters that describe the name and data type of the incoming data. If a function is declared with parameters, then data must be passed when the function is invoked. We can include as many parameters as needed.
```kotlin
fun birthday(name: String, age: Int) {
   println("Happy birthday $name! You turn $age today!")
}
 
fun main() {
  birthday("Oscar", 26) // Prints: Happy birthday Oscar! You turn 25 today!
  birthday("Amarah", 30) // Prints: Happy birthday Amarah! You turn 30 today!
}
```
### Default Arguements
We can give arguments a default value which provides an argument an automatic value if no value is passed into the function when it’s invoked.
```kotlin
fun favoriteLanguage(name, language = "Kotlin") {
  println("Hello, $name. Your favorite programming language is $language")  
}
 
 
fun main() {
  favoriteLanguage("Manon") // Prints: Hello, Manon. Your favorite programming language is Kotlin
  
  favoriteLanguage("Lee", "Java") // Prints: Hello, Lee. Your favorite programming language is Java
}
```
### Named Arguments
We can name our arguments when invoking a function to provide additional readability.

To name an argument, write the argument name followed by the assignment operator (`=`) and the argument value. The argument’s name must have the same name as the parameter in the function being called.

By naming our arguments, we can place arguments in any order when the function is being invoked.
```kotlin
fun findMyAge(currentYear: Int, birthYear: Int) {
   var myAge = currentYear - birthYear
   println("I am $myAge years old.")
}
 
fun main() {
  findMyAge(currentYear = 2020, birthYear = 1995)
  // Prints: I am 25 years old.
  findMyAge(birthYear = 1920, currentYear = 2020)
  // Prints: I am 100 years old.
}
```
### Return Statement
In Kotlin, in order to return a value from a function, we must add a return statement to our function using the `return` keyword. This value is then passed to where the function was invoked.

If we plan to return a value from a function, we must declare the return type in the function header.
```kotlin
// Return type is declared outside the parentheses
fun getArea(length: Int, width: Int): Int {
  var area = length * width
 
  // return statement
  return area
}
 
fun main() {
  var myArea = getArea(10, 8)
  println("The area is $myArea.") // Prints: The area is 80.
}
```
### Single Expression Functions
If a function contains only a single expression, we can use a shorthand syntax to create our function.

Instead of placing curly brackets after the function header to contain the function’s code block, we can use an assignment operator `=` followed by the expression being returned.
```kotlin
fun fullName(firstName: String, lastName: String) = "$firstName $lastName"
 
fun main() {
  println(fullName("Ariana", "Ortega")) // Prints: Ariana Ortega
  println(fullName("Kai", "Gittens")) // Prints: Kai Gittens
}
```
### Function Literals
Function literals are unnamed functions that can be treated as expressions: we can assign them to variables, call them, pass them as arguments, and return them from a function as we could with any other value.

Two types of function literals are anonymous functions and lambda expressions.
```kotlin
 
fun main() {
  // Anonymous Function:
  var getProduct = fun(num1: Int, num2: Int): Int {
     return num1 * num2
  }
  println(getProduct(8, 3)) // Prints: 24
 
  // Lambda Expression
  var getDifference = { num1: Int, num2: Int -> num1 - num2 }
  println(getDifference(10, 3)) // Prints: 7
}
```
## Classes <a name="classes"></a>
### Classes
A class is an object-oriented concept which resembles a blueprint for individual objects. A class can contain properties and functions and is defined using the `class` keyword followed by a name and optional body.

If the class does not have a body, its curly braces can be omitted.
```kotlin
// A class with properties that contain default values
class Student {
  var name = "Lucia"
  var semester = "Fall"
  var gpa = 3.95
}
 
// Shorthand syntax with no class body 
class Student 
```
### Class Instances
A new instance of a class is created by calling the class name followed by a pair of parentheses `()` and any necessary arguments.

When creating an instance of a class, we must declare a variable in which we intend to store our instance and assign it equal to the class call. Once the instance has been created, we can use dot syntax to access and retrieve the value of each property.
```kotlin
// Class
class Student {
  var name = "Lucia"
  var semester = "Fall"
  var gpa = 3.95
}
 
fun main() {
  var student = Student()   // Instance
  println(student.name)     // Prints: Lucia
  println(student.semester) // Prints: Fall
  println(student.gpa)      // Prints: 3.95  
}
```
### Primary Constructor
A primary constructor defines each property value within a class header and allows us to then set unique values when the object is instantiated.

To create a primary constructor using the shorthand syntax, we can follow the name of the class with a pair of parentheses `()` inside of which each property is defined and assigned a data type.
```kotlin
class Student(val name: String, val gpa: Double, val semester: String, val estimatedGraduationYear: Int) 
 
fun main() {
    var student = Student("Lucia", 3.95, "Fall", 2022) 
  println(student.name)     // Prints: Lucia
  println(student.gpa)      // Prints: 3.95
  println(student.semester) // Prints: Fall
  println(student.estimatedGraduationYear) // Prints: 2022
}
```
### Init Blocks
The `init` block gets invoked with every instance that’s created and is used to add logic to the class. The `init` keyword precedes any member functions and is followed by a pair of curly braces.
```kotlin
class Student(val name: String, val gpa: Double, val semester: String, val estimatedGraduationYear: Int) {
 
  init {
    println("$name has ${estimatedGraduationYear - 2020} years left in college.")
  }
}
 
fun main() {
  var student = Student("Lucia", 3.95, "Fall", 2022) // Prints: Lucia has 2 years left in college. 
}
```
### Member Functions
A function declared within a class is known as a member function of that class. In order to invoke a member function, we must call the function on an instance of the class.
```kotlin
class Student(val name: String, val gpa: Double, val semester: String, val estimatedGraduationYear: Int) {
 
  init {
    println("$name has ${estimatedGraduationYear - 2020} years left in college.")
  }
 
  // Member Function
  fun calculateLetterGrade(): String {
    return when {
      gpa >= 3.0 -> "A"
      gpa >= 2.7 -> "B"
      gpa >= 1.7 -> "C"
      gpa >= 1.0 -> "D"
      else -> "E"
    }
  }
}
 
// When an instance is created and the function is called, the when expression will execute and return a letter grade
 
fun main() {
  var student = Student("Lucia", 3.95, "Fall", 2022) // Prints: Lucia has 2 years left in college. 
  println("${student.name}'s letter grade is ${student.calculateLetterGrade()}.") // Prints: Lucia's letter grade is A. 
}
```
