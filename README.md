<div align="center">

# 🚀 **Introduction to Dart & Setting Up Environment**
![Dart](https://img.shields.io/badge/Dart-Language-blue?logo=dart&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-Compatible-02569B?logo=flutter)
![License](https://img.shields.io/badge/License-Free-brightgreen)
![Author](https://img.shields.io/badge/Author-Shahrier%20Jaman-orange)

</div>

---

## 🌀 **What is Dart?**

Dart is a programming language created by **Google**.  
It’s mostly used for building mobile apps (with **Flutter**), web apps, and server-side programs.

---

## 💡 **Why Dart?**

It’s easy to read, fast, and supports both **object-oriented** and **functional programming** styles.

---

## 🛠️ **Setup**

You can write Dart code online using [**DartPad**](https://dartpad.dev) — no installation needed!  

Or install the **Dart SDK** or **Flutter SDK** on your computer.  

Use an editor like **VS Code** or **Android Studio** to write and run your code.

---

## 🧾 **Basic Syntax & Structure**

A simple Dart program looks like this:

```dart
void main() {
  print('Hello, Sabit!');
}
```
🧠 Explanation

void main() → This is the starting point of every Dart program.

{ } → Curly braces hold the block of code to run.

print() → Displays text or data on the screen.

Variables & Data Types

Variables are containers that store information (like boxes with labels).

🔹 Example:
int age = 20;         // integer
double price = 9.99;  // decimal
String name = 'Ali';  // text
bool isActive = true; // true/false

Data Types tell Dart what kind of value you are storing:
int → whole numbers
double → decimal numbers
String → text
bool → true/false
var → Dart guesses the type automatically


🔒 Constants & Final
🧭 Final keyword
You can assign the value only once, but the value can be decided while the program is running (runtime).
final name = 'Ali';
print(name);

⚙️ const keyword
The value must be known before the program runs — at compile-time.
const pi = 3.14159;
const gravity = 9.8;
print(pi * gravity);

final currentTime = DateTime.now();
print(currentTime);
✅ Works fine too!

const currentTime = DateTime.now(); // ❌ ERROR!
❌ This won’t work — because DateTime.now() is not known until the program runs.
💡 Use final instead for such values.

🔢 Operators
Operators help you perform actions on values.

➕ Mathematical Operators:
var a = 10, b = 3;
print(a + b); // 13
print(a - b); // 7
print(a * b); // 30
print(a / b); // 3.333...
print(a % b); // 1 (remainder)

⚖️ Comparison Operators:
print(a == b); // false
print(a != b); // true
print(a > b);  // true
print(a < b);  // false

🔗 Logical Operators:
bool x = true, y = false;
print(x && y); // false (AND)
print(x || y); // true  (OR)
print(!x);     // false (NOT)


🧭 Control Flow in Dart

Control flow means deciding what your program should do next — based on conditions or repetition.
Think of it like giving your code directions:
“If this happens → do that.”

🧩 1. if Statement
Used to check a condition and run code only if it’s true.
Structure :
if (condition) {
  // code runs if condition is true
}

Example : 
int age = 20;
if (age >= 18) {
  print('You are an adult.');
}


🔹 2. if...else Statement
Used when you want to do one thing if true, and another if false.

Structure:
if (condition) {
  // code runs if condition is true
} else {
  // code runs if condition is false
}

Example:
int age = 16;
if (age >= 18) {
  print('You can vote.');
} else {
  print('You are too young to vote.');
}
✅ Output:
You are too young to vote.



🔹 3. if...else if...else Statement
Used when there are multiple conditions to check.

Structure : 
if (condition1) {
  // runs if condition1 is true
} else if (condition2) {
  // runs if condition2 is true
} else {
  // runs if all above are false
}

Example :
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
✅ Output: Grade: A

💡 Dart checks conditions from top to bottom — once one is true, it stops checking the rest.



🔹4. switch Statement
Used to check one variable against many fixed values — a cleaner alternative to multiple if-else statements.

Structure:
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


Example :
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
✅ Output: Second day of the week.
💡 The break keyword stops the switch after a match is found.
If no case matches, default runs.






























