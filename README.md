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
---

## 7. Input (stdin – Reading from User)

To take user input, you must import **dart:io**.

### Structure
```dart
import 'dart:io';
void main() {
  var input = stdin.readLineSync(); // reads text input
  print(input);
}
```

### Example 1
```dart
import 'dart:io';
void main() {
  print('Enter your name:');
  String? name1 = stdin.readLineSync();  // ? = allows null
  String name2 = stdin.readLineSync();  // do not allow null
  print('Hello $name1!');
}
```

`stdin.readLineSync()` reads a line of text from user input and always returns a String.

### Convert Input to Number
```dart
int variable = int.parse(stdin.readLineSync()!);
double variable = double.parse(stdin.readLineSync()!);
```
**Example 2:**
```dart
import 'dart:io';
void main() {
  print('Enter your age:');
  int age = int.parse(stdin.readLineSync()!);
  print('Next year you will be ${age + 1} years old.');
}
```
💡 `int.parse()` converts string → number.

### 🧠 Why We Need `!` Here

`stdin.readLineSync()` returns a nullable string → its type is `String?`.

The question mark `?` means the value could be null (for example, if the user didn’t type anything).  
But `int.parse()` only accepts a **non-null** String (`String`, not `String?`).

So we use `!` (null assertion operator) to tell Dart:  
> “Don’t worry, I know it’s not null. Trust me!”

### ❌ Wrong Code
```dart
import 'dart:io';
void main() {
  int? myage = stdin.readByteSync();
  print(myage);
}
```

### What’s Happening Here
✅ The code is valid Dart syntax, so no compile error.  
❌ But it prints a weird or unexpected number instead of your actual input (like your age).

For example, if you type **2**, it prints something like **50**.

💡 Why This Happens  
`stdin.readByteSync()` reads only a single byte from input, and that byte is the **ASCII code** of the character you typed — not the number itself.

| What You Type | What Dart Reads (ASCII Code) | Output |
|----------------|-------------------------------|---------|
| 1 | 49 | 49 |
| 2 | 50 | 50 |
| 3 | 51 | 51 |
| 4 | 52 | 52 |

---

## 8. Comments

### ✅ A. Single-line Comment
```dart
// This is a single-line comment
```
**Example:**
```dart
void main() {
  // This prints a message
  print('Hello Dart!');
}
```
Used for short explanations or notes. Dart ignores it while running.

### ✅ B. Multi-line Comment
```dart
/*
This is a multi-line comment
You can write multiple lines here
*/
```
**Example:**
```dart
void main() {
  /* This section prints
     a greeting message */
  print('Welcome!');
}
```
🧠 **Tip:** In VS Code, press **Shift + Alt + F** (Windows) or **Option + Shift + F** (Mac) to auto-format your Dart code.

---

## 9. Collections (Lists, Sets, Maps)

### 🧱 1️⃣ LIST — Ordered Collection

**Structure**
```dart
List<datatype> listName = [value1, value2, value3];
```

**Example**
```dart
List<String> names = ["Jaman", "Sabit", "Shahrier"];
print(names);
print(names[0]);
print(names.length);
```
✅ **Output:**
```
[Jaman, Sabit, Shahrier]
Jaman
3
```

### Common List Operations

| Operation | Example | Meaning |
|------------|----------|----------|
| Add item | `names.add("Rafi")` | Adds element at end |
| Insert item | `names.insert(1, "Arif")` | Adds element at position |
| Remove item | `names.remove("Sabit")` | Removes specific element |
| Remove by index | `names.removeAt(0)` | Removes element at index |
| Sort | `names.sort()` | Sorts list alphabetically |
| Reverse | `names.reversed.toList()` | Returns reversed list |
| Contains | `names.contains("Ali")` | Checks if value exists |
| Length | `names.length` | Returns total elements |
| Clear | `names.clear()` | Removes all elements |
| Join | `names.join(", ")` | Converts list to string |

**Loops with Lists**
```dart
for (int i = 0; i < names.length; i++) {
  print(names[i]);
}
for (var name in names) {
  print(name);
}
names.forEach((name) {
  print(name);
});
```

✅ All 3 print each element one by one.

---

### 🧱 2️⃣ SET — Unordered Collection (Unique Values)

**Structure**
```dart
Set<int> numbers = {1, 2, 3, 3, 2};
print(numbers);
```
✅ **Output:**
```
{1, 2, 3}
```
🧠 **Set automatically removes duplicates.**

### Common Set Operations

| Operation | Example | Meaning |
|------------|----------|----------|
| Add value | `numbers.add(4)` | Adds one element |
| Remove value | `numbers.remove(2)` | Removes element |
| Contains | `numbers.contains(3)` | Checks if exists |
| Union | `set1.union(set2)` | Combines two sets |
| Intersection | `set1.intersection(set2)` | Common elements |
| Difference | `set1.difference(set2)` | Elements not in other |
| Length | `numbers.length` | Returns total count |
| Clear | `numbers.clear()` | Removes all elements |

**Looping through Set**
```dart
for (var n in numbers) {
  print(n);
}
```

✅ Prints each element (order not guaranteed).

---

### 🧱 3️⃣ MAP — Key–Value Pairs

**Structure**
```dart
Map<String, dynamic> student = {
  "name": "Ali",
  "age": 20,
  "marks": 89.5
};
```

**Example**
```dart
print(student);
print(student["name"]);
print(student.keys);
print(student.values);
```

### Common Map Operations

| Operation | Example | Meaning |
|------------|----------|----------|
| Add key-value | `student["grade"] = "A";` | Adds a new key-value |
| Remove key | `student.remove("age")` | Removes entry |
| Update value | `student["marks"] = 90;` | Updates existing key |
| Contains key | `student.containsKey("name")` | Checks for key |
| Contains value | `student.containsValue(20)` | Checks for value |
| Add all | `student.addAll({"city": "Dhaka"})` | Adds multiple entries |
| Clear | `student.clear()` | Removes all pairs |
| Length | `student.length` | Returns total pairs |

**Loops with Maps**
```dart
student.forEach((key, value) {
  print("$key: $value");
});
for (var key in student.keys) {
  print("Key: $key, Value: ${student[key]}");
}
```

✅ Both print all keys and their values.

---

## 10. Null Safety

Avoiding “null errors” — one of the most common bugs in programming.

### 🧱 What is Null?
`null` means nothing / empty / no value.

In Dart, a variable can hold null only if you allow it.

```dart
String? name = null; // OK
String name = null;  // ❌ Error
```

💡 Dart says:  
> “If you don’t mark a variable as nullable (?), it can never be null!”

### 🧱 Why We Need Null Safety

Before null safety, if you forgot to assign a value, your program might crash with:  
`NullPointerException`.

Now Dart helps you catch null issues **before running your code**.

### 🧩 How to Use Null Safety

**Example 1: Nullable Variable**
```dart
String? name;
print(name); // Output: null
```

**Example 2: Non-nullable Variable**
```dart
String name = "Sabit";
print(name);
```

**Example 3: Using ! (Null Assertion)**
```dart
String? name = "Ali";
print(name!);
```

**Example 4: Using ?? (Default if Null)**
```dart
String? name;
print(name ?? "Guest");
```

✅ Output → `Guest`

**Example 5: Using ??= (Assign Default)**
```dart
String? user;
user ??= "DefaultUser";
print(user);
```

✅ Output → `DefaultUser`

🧠 Means “If user is null, assign it to ‘DefaultUser’”.

---

## 11. Exception Handling

Handling runtime errors safely.

### 🧱 What is an Exception?
An exception is an error that happens while your program is running — like dividing by zero or invalid input.

```dart
int result = 10 ~/ 0; // ❌ Error: Division by zero
```

### 🧱 Why We Handle Exceptions
To stop your app from crashing — and show a friendly message instead.

### 🧩 Structure
```dart
try {
  // code that may cause error
} catch (error) {
  // code that runs if an error happens
}
```

### Example 1: Basic Try-Catch
```dart
void main() {
  try {
    int result = 10 ~/ 0;
    print(result);
  } catch (e) {
    print("Error: $e");
  }
}
```
✅ Output → `Error: IntegerDivisionByZeroException`

### Example 2: Try-Catch-Finally
The `finally` block runs no matter what (error or not).

```dart
void main() {
  try {
    int result = 10 ~/ 2;
    print("Result: $result");
  } catch (e) {
    print("Error: $e");
  } finally {
    print("Code Finished!");
  }
}
```
✅ Output →  
```
Result: 5
Code Finished!
```