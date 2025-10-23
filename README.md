# Introduction to Dart & Setting Up Environment

![Dart](https://img.shields.io/badge/Dart-Language-blue?logo=dart&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-Compatible-02569B?logo=flutter)
![License](https://img.shields.io/badge/License-Free-brightgreen)
![Author](https://img.shields.io/badge/Author-Shahrier%20Jaman-orange)

---

## What is Dart?

Dart is a programming language created by **Google**.  
It’s mostly used for building mobile apps (with **Flutter**), web apps, and server-side programs.

---

## Why Dart?

It’s easy to read, fast, and supports both **object-oriented** and **functional programming** styles.

---

## Setup

You can write Dart code online using [**DartPad**](https://dartpad.dev) — no installation needed!  

Or install the **Dart SDK** or **Flutter SDK** on your computer.  

Use an editor like **VS Code** or **Android Studio** to write and run your code.

---

## Basic Syntax & Structure

A simple Dart program looks like this:

```dart
void main() {
  print('Hello, Sabit!');
}
```

### Explanation

| Symbol / Keyword | Meaning |
|-------------------|----------|
| `void main()` | Starting point of every Dart program |
| `{ }` | Curly braces hold the block of code to run |
| `print()` | Displays text or data on the screen |

---

## Variables & Data Types

Variables are containers that store information (like boxes with labels).

### Example

```dart
int age = 20;         // integer
double price = 9.99;  // decimal
String name = 'Ali';  // text
bool isActive = true; // true/false
```

### Data Types Overview

| Type | Description |
|-------|--------------|
| `int` | Whole numbers |
| `double` | Decimal numbers |
| `String` | Text values |
| `bool` | True/False values |
| `var` | Dart guesses the type automatically |

---

## Constants & Final

### Final Keyword

You can assign the value only once, but the value can be decided while the program is running (runtime).

```dart
final name = 'Ali';
print(name);
```

### Const Keyword

The value must be known before the program runs — at compile-time.

```dart
const pi = 3.14159;
const gravity = 9.8;
print(pi * gravity);

final currentTime = DateTime.now();
print(currentTime);
```

✅ Works fine.

```dart
const currentTime = DateTime.now(); // ❌ ERROR!
```

❌ This won’t work — because `DateTime.now()` is not known until the program runs.  
💡 Use `final` instead for such values.

---

## Operators

Operators help you perform actions on values.

### Mathematical Operators

```dart
var a = 10, b = 3;
print(a + b); // 13
print(a - b); // 7
print(a * b); // 30
print(a / b); // 3.333...
print(a % b); // 1 (remainder)
```

### Comparison Operators

```dart
print(a == b); // false
print(a != b); // true
print(a > b);  // true
print(a < b);  // false
```

### Logical Operators

```dart
bool x = true, y = false;
print(x && y); // false (AND)
print(x || y); // true  (OR)
print(!x);     // false (NOT)
```

---

## Control Flow in Dart

Control flow means deciding what your program should do next — based on conditions or repetition.  
Think of it like giving your code directions:  
“If this happens → do that.”

---

### 1. if Statement

Used to check a condition and run code only if it’s true.

**Structure:**
```dart
if (condition) {
  // code runs if condition is true
}
```

**Example:**
```dart
int age = 20;
if (age >= 18) {
  print('You are an adult.');
}
```

---

### 2. if...else Statement

Used when you want to do one thing if true, and another if false.

**Structure:**
```dart
if (condition) {
  // code runs if condition is true
} else {
  // code runs if condition is false
}
```

**Example:**
```dart
int age = 16;
if (age >= 18) {
  print('You can vote.');
} else {
  print('You are too young to vote.');
}
```

✅ **Output:**
```
You are too young to vote.
```

---

### 3. if...else if...else Statement

Used when there are multiple conditions to check.

**Structure:**
```dart
if (condition1) {
  // runs if condition1 is true
} else if (condition2) {
  // runs if condition2 is true
} else {
  // runs if all above are false
}
```

**Example:**
```dart
int marks = 75;
if (marks >= 90) {
  print('Grade: A+');
} else if (marks >= 75) {
  print('Grade: A');
} else if (marks >= 60) {
  print('Grade: B');
} else {
  print('Grade: C');
}
```

✅ **Output:**
```
Grade: A
```

💡 Dart checks conditions from top to bottom — once one is true, it stops checking the rest.

---

### 4. switch Statement

Used to check one variable against many fixed values — a cleaner alternative to multiple if-else statements.

**Structure:**
```dart
switch (variable) {
  case value1:
    // code for value1
    break;

  case value2:
    // code for value2
    break;

  default:
    // code if no case matches
}
```

**Example:**
```dart
String day = 'Tuesday';
switch (day) {
  case 'Monday':
    print('Start of the week.');
    break;
  case 'Tuesday':
    print('Second day of the week.');
    break;
  case 'Friday':
    print('Almost weekend!');
    break;
  default:
    print('Just another day.');
}
```

✅ **Output:**
```
Second day of the week.
```

💡 The `break` keyword stops the switch after a match is found.  
If no case matches, the `default` block runs.

---

## Functions in Dart (Structure + Explanation)

A function is a block of code that performs a specific task.  
You write it once and use it anywhere in your program.  
It helps to make code reusable, organized, and easy to read.

---

### 1. Basic Function (No Parameters, No Return)

**Structure:**
```dart
void functionName() {
  // code to execute
}
```

**Example:**
```dart
void greet() {
  print('Hello Dart!');
}
greet();
```

You define a function with a name (`greet`) and call it later.  
`void` means the function does not return any value.

---

### 2. Function with Parameters

**Structure:**
```dart
void functionName(datatype parameter1, datatype parameter2) {
  // code using parameters
}
```

**Example:**
```dart
void greetUser(String name) {
  print('Hello $name!');
}
greetUser('Sabit');
```

Parameters let you pass information into a function so it can use it inside.

---

### 3. Function with Return Value

**Structure:**
```dart
datatype functionName() {
  // code
  return value;
}
```

**Example:**
```dart
int addNumbers() {
  int a = 5;
  int b = 3;
  return a + b;
}
print(addNumbers());
```

---

### 4. Arrow Function (Short Function)

**Structure:**
```dart
datatype functionName(parameters) => expression;
```

`=>` is a shortcut for one-line functions.

**Example:**
```dart
int square(int x) => x * x;
print(square(5));
```

---

### 5. Function with Optional Parameters

You can make parameters optional by putting them in `[]` or `{}`.

#### (a) Optional Positional Parameters → [ ]

**Structure:**
```dart
void functionName([datatype parameter]) { ... }
```

**Example:**
```dart
void greet([String name = 'Guest']) {
  print('Hello $name!');
}
greet();        // uses default
greet('Sabit'); // uses given value
```

#### (b) Optional Named Parameters → { }

**Structure:**
```dart
void functionName({datatype parameter1, datatype parameter2}) { ... }
```

**Example:**
```dart
void userInfo({String name = 'Unknown', int age = 0}) {
  print('Name: $name, Age: $age');
}
userInfo(name: 'Sabit', age: 21);
```

Named parameters make your function calls more readable.

---

### 6. Anonymous Function (No Name)

**Structure:**
```dart
() {
  // code
};
```

**Example:**
```dart
var greet = () {
  print('Hello from anonymous function!');
};
greet(); // Hello from anonymous function!
```
