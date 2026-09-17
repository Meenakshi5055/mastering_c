# 🔢 04 · Constants in C

<div align="center">

[![C Language](https://img.shields.io/badge/Language-C-00599C?style=for-the-badge&logo=c&logoColor=white)](https://en.wikipedia.org/wiki/C_(programming_language))
[![Level](https://img.shields.io/badge/Level-Beginner-2ea44f?style=for-the-badge)](#)
[![Topic](https://img.shields.io/badge/Topic-Constants-8A2BE2?style=for-the-badge)](#)

**A constant is a value that does not change while a program runs.** 🔒

</div>

> 💡 **In one line:** `25`, `3.14`, `'A'`, and `"Hello"` are all literal values written directly in a C program.

---

## 🧠 What is a constant?

A **constant** is a fixed value. Unlike a variable, its value is not intended to change during program execution.

```c
int age = 25;
```

Here, `25` is an **integer constant**. It is a fixed value used to initialize `age`.

> ⚠️ **Important:** A literal such as `25` is not the same thing as a named constant declared with `const`. For example, `const int days = 7;` declares a variable that cannot be modified through `days` after initialization.

---

## 🗺️ Types of constants in C

```text
Constants
├── Integer constants
│   ├── Decimal
│   ├── Octal
│   └── Hexadecimal
├── Floating-point constants
├── Character constants
└── String literals
```

---

## 1️⃣ Integer constants

An integer constant represents a whole number. It has no decimal point and may be positive, negative, or zero.

### 🔟 Decimal integers

- Use the normal base-10 system: digits `0`–`9`.
- Examples: `25`, `-100`, `0`, `2024`

### 🐙 Octal integers

- Use base 8: digits `0`–`7` only.
- Begin with a leading `0`.
- Examples: `010` equals decimal `8`; `017` equals decimal `15`.

```c
int permission = 0644; // Octal notation
```

> 🚫 `018` is invalid octal notation because the digit `8` is not allowed.

### 🧮 Hexadecimal integers

- Use base 16: digits `0`–`9` and letters `A`–`F` (uppercase or lowercase).
- Begin with `0x` or `0X`.
- Examples: `0x1A` equals decimal `26`; `0X2F` equals decimal `47`.

```c
int color = 0xFF; // Hexadecimal notation
```

---

## 2️⃣ Floating-point constants

A floating-point constant represents a fractional value. It may use decimal notation or exponential notation.

| Form | Examples | Meaning |
|---|---|---|
| Decimal | `3.14`, `0.001`, `-25.5` | A value with a fractional part |
| Exponential | `2.5e3`, `1.2E-4` | `2.5 × 10³` and `1.2 × 10⁻⁴` |

C also permits forms such as `.5` and `5.`. The decimal point is not required when an exponent is present: `1e3` is valid too.

```c
double distance = 12.5;
double large_number = 1.2e4; // 12000
```

---

## 3️⃣ Character constants and string literals

### 🔤 Character constants

A character constant contains **one character** enclosed in single quotes.

```c
char grade = 'A';
char digit = '5';
char newline = '\n';
```

Escape sequences such as `\n` (newline) and `\t` (tab) represent special characters.

### 💬 String literals

A string literal is a sequence of characters enclosed in double quotes.

```c
"Hello"
"C Programming"
"123"
```

C stores a string as an array of characters ending with a hidden null character, `\0`.

```c
char message[] = "Hi";
// Stored as: 'H'  'i'  '\0'
```

> ✅ **Remember:** `'A'` is one character, while `"A"` is a string containing one character plus the terminating `\0`.

---

## 📏 Rules to remember

1. Use **single quotes** for a character constant and **double quotes** for a string literal.
2. Integer constants do not contain a decimal point or spaces.
3. Octal constants begin with `0` and may contain only digits `0`–`7`.
4. Hexadecimal constants begin with `0x` or `0X` and may contain `0`–`9`, `A`–`F`, or `a`–`f`.
5. Floating-point constants may use decimal or exponential notation, such as `.5`, `5.`, `3.14`, or `1e3`.
6. A string literal ends with the null character `\0` when stored in a character array.

---

## 🧪 Quick practice

What is the type of each value?

```c
42       // Integer constant
010      // Octal integer constant
0x2A     // Hexadecimal integer constant
3.14     // Floating-point constant
'A'      // Character constant
"Hello"  // String literal
```

<details>
<summary>✨ Click to see a simple challenge</summary>

Which value represents the number `10` in octal notation?

**Answer:** `012` ✅

</details>

---

## 📚 Quick reference

| Type | Example | Key idea |
|---|---|---|
| Decimal integer | `100` | Base 10 |
| Octal integer | `0144` | Starts with `0`; digits `0`–`7` |
| Hexadecimal integer | `0x64` | Starts with `0x`; digits `0`–`9`, `A`–`F` |
| Floating-point | `3.14` | Represents a fractional value |
| Character constant | `'A'` | One character in single quotes |
| String literal | `"Hello"` | Text in double quotes; ends with `\0` in storage |

---

<div align="center">

### 🎉 You can now identify the most common values used in C!

</div>

<table width="100%">
<tr>
<td align="left">⬅️ <a href="03-keywords.md">03 · Keywords</a></td>
<td align="right"><a href="05-strings.md">05 · Strings</a> ➡️</td>
</tr>
</table>

<div align="center">

[⬆️ Back to top](#-04--constants-in-c)

</div>
