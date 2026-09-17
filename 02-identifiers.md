# 🏷️ 02. Identifiers in C

![C Language](https://img.shields.io/badge/Language-C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Beginner Friendly](https://img.shields.io/badge/Level-Beginner-2EA44F?style=for-the-badge)
![Chapter 02](https://img.shields.io/badge/Chapter-02-F97316?style=for-the-badge)

> 💡 **An identifier is a name you give to something in your C program.**

Identifiers help you name and access:

- 📦 Variables
- ⚙️ Functions
- 📋 Arrays
- 🧱 Structures
- 🔧 Other user-defined items

---

## 🧠 What Is an Identifier?

```c
int marks = 90;
```

In this example:

| Part | Meaning |
|---|---|
| `int` | Data type |
| `marks` | Identifier — the name of the variable |
| `90` | Value stored in the variable |

So, `marks` is the identifier used to refer to the value `90`.

> 🌱 Think of an identifier like a **label** on a box. The label helps you remember what is inside the box.

---

## ✅ Rules for Naming Identifiers

A valid identifier:

1. Can contain letters: `A-Z` and `a-z`
2. Can contain digits: `0-9`
3. Can contain underscores: `_`
4. Must begin with a letter or underscore
5. Must not begin with a digit
6. Must not contain spaces or special symbols
7. Must not be a C keyword
8. Is case-sensitive

> ⚠️ **Remember:** `age`, `Age`, and `AGE` are three different identifiers.

---

## 🟢 Valid Identifiers

| Identifier | Why it is valid |
|---|---|
| `age` | Starts with a letter |
| `_count` | Starts with an underscore |
| `total_marks` | Uses an underscore correctly |
| `num1` | Contains a digit, but does not start with one |
| `studentName` | Uses letters and mixed case |

```c
int age;
int total_marks;
int num1;
int studentName;
```

---

## 🔴 Invalid Identifiers

| Identifier | Why it is invalid |
|---|---|
| `1number` | Cannot start with a digit |
| `total-marks` | Hyphen `-` is not allowed |
| `int` | `int` is a reserved keyword |
| `first name` | Spaces are not allowed |
| `salary%` | Special symbols are not allowed |

```c
// ❌ These declarations are invalid

int 1number;
int total-marks;
int int;
int first name;
int salary%;
```

---

## 🔠 Identifiers Are Case-Sensitive

C treats uppercase and lowercase letters as different:

```c
int marks = 90;
int Marks = 80;
int MARKS = 70;
```

These are three separate identifiers:

- `marks`
- `Marks`
- `MARKS`

> 🧩 **Tip:** Choose one naming style and use it consistently throughout your program.

---

## 🌟 Good Naming Practices

Meaningful identifiers make your code easier to read and understand.

### ❌ Difficult to understand

```c
int x;
int y;
int z;
```

### ✅ Easy to understand

```c
int studentAge;
int totalMarks;
int numberOfStudents;
```

> ✨ Prefer `studentAge` over `x` because the name explains what the value represents.

### Common Naming Styles

| Style | Example | Suitable for |
|---|---|---|
| camelCase | `studentAge` | Variables and functions |
| snake_case | `student_age` | Variables and functions |
| UPPER_CASE | `MAX_SIZE` | Constants and macros |

```c
#define MAX_SIZE 100
```

---

## 🧪 Quick Challenge

Which of these are valid identifiers?

1. `student_name`
2. `2ndPlace`
3. `totalMarks`
4. `float`
5. `_ score`
6. `price2`

<details>
<summary>🎯 Click to reveal the answer</summary>

### ✅ Valid

- `student_name`
- `totalMarks`
- `price2`

### ❌ Invalid

- `2ndPlace` — starts with a digit
- `float` — is a reserved keyword
- `_ score` — contains a space

</details>

---

## 📌 Quick Summary

| Rule | Example |
|---|---|
| Start with a letter or `_` | `name`, `_value` ✅ |
| Digits are allowed after the first character | `value2` ✅ |
| Do not use spaces | `student_name` ✅ |
| Do not use special symbols | `total-marks` ❌ |
| Do not use C keywords | `int` ❌ |
| Remember case sensitivity | `age` ≠ `Age` |

> 🚀 **Best practice:** Use meaningful names that clearly describe your data.

---

<div align="left">

⬅️ [Previous: 01. Introduction to Tokens](01-tokens-intro.md) &nbsp;•&nbsp;         

[Next: 03. Keywords](03-keywords.md) ➡️

</div>


<div align="right">

[Next: 03. Keywords](03-keywords.md) ➡️

</div>


