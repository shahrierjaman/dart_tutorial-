# Introduction to Dart & Setting Up Environment

![Dart](https://img.shields.io/badge/Dart-Language-blue?logo=dart&logoColor=white)
![Flutter](https://img.shields.io/badge/Flutter-Compatible-02569B?logo=flutter)
![License](https://img.shields.io/badge/License-Free-brightgreen)
![Author](https://img.shields.io/badge/Author-Shahrier%20Jaman-orange)

---

## 1. What is Dart?

Dart is a programming language created by **Google**.  
It’s mostly used for building mobile apps (with **Flutter**), web apps, and server-side programs.

---

## 2. Why Dart?

It’s easy to read, fast, and supports both **object-oriented** and **functional programming** styles.

---

## 3. Setup

You can write Dart code online using [**DartPad**](https://dartpad.dev) — no installation needed!  

Or install the **Dart SDK** or **Flutter SDK** on your computer.  

Use an editor like **VS Code** or **Android Studio** to write and run your code.

---

## 4. Basic Syntax & Structure

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

## 12. Collections (Lists, Sets, Maps)

### 🧱 List — Ordered Collection

#### Common List Operations
| Operation | Example | Meaning |
|------------|----------|----------|
| Add item | `names.add("Rafi")` | Adds element at end |
| Insert item | `names.insert(1, "Arif")` | Adds element at position |
| Remove item | `names.remove("Sabit")` | Removes specific element |
| Remove by index | `names.removeAt(0)` | Removes element at index |
| Length | `names.length` | Returns total elements |
| Sort | `names.sort()` | Sorts list alphabetically |
| Reverse | `names.reversed.toList()` | Returns reversed list |
| Contains | `names.contains("Ali")` | Checks if value exists |
| Clear | `names.clear()` | Removes all elements |
| Join | `names.join(", ")` | Converts list to string |

---

### 🧱 Set — Unordered Collection (Unique Values)

#### Common Set Operations
| Operation | Example | Meaning |
|------------|----------|----------|
| Add value | `numbers.add(4)` | Adds one element |
| Remove value | `numbers.remove(2)` | Removes one element |
| Contains | `numbers.contains(3)` | Checks if element exists |
| Union | `set1.union(set2)` | Combines two sets |
| Intersection | `set1.intersection(set2)` | Common elements |
| Difference | `set1.difference(set2)` | Elements not in other set |
| Length | `numbers.length` | Total count |
| Clear | `numbers.clear()` | Removes all elements |
| Is Empty | `numbers.isEmpty` | Checks if set has no elements |

---

### 🧱 Map — Key–Value Pairs

#### Common Map Operations
| Operation | Example | Meaning |
|------------|----------|----------|
| Add key-value | `student["grade"] = "A";` | Adds new pair |
| Remove key | `student.remove("age")` | Deletes entry |
| Update value | `student["marks"] = 95;` | Updates existing key |
| Contains key | `student.containsKey("name")` | Checks key presence |
| Contains value | `student.containsValue(20)` | Checks value presence |
| Clear | `student.clear()` | Removes all pairs |
| Length | `student.length` | Total entries |
| Add all | `student.addAll({"city": "Dhaka"})` | Adds multiple pairs |
| Keys | `student.keys` | Returns all keys |
| Values | `student.values` | Returns all values |

---
