# 🔢 04 · Constants in C

<div align="center">

[![Language](https://img.shields.io/badge/Language-C-00599C?style=for-the-badge&logo=c&logoColor=white)](https://en.wikipedia.org/wiki/C_(programming_language))
[![Level](https://img.shields.io/badge/Level-Beginner-2ea44f?style=for-the-badge)](#)
[![Topic](https://img.shields.io/badge/Topic-Constants-8A2BE2?style=for-the-badge)](#)
[![Practice](https://img.shields.io/badge/Practice-Examples%20%2B%20Quiz-ff69b4?style=for-the-badge)](#-quick-practice)

### 🔒 A constant is a fixed value that does not change during program execution.

</div>

> 💡 **Simple idea:** `25`, `3.14`, `'A'`, and `"Hello"` are values written directly in a C program.

---

## 🧠 What is a constant?

A **constant** is a value that remains fixed while a program is running. For example, `25` is an integer constant:

```c
int age = 25;
```

Here, `age` is a variable and `25` is a constant value.

> 📌 **Do not confuse these terms:** `25` is a literal constant. `const int days = 7;` is a declaration that prevents the program from modifying `days` through that name.

---

## 🗺️ Classification of constants in C

C constants are divided into **two main categories**:

```text
Constants
├── 1. Numeric Constants
│   ├── A. Integer Constants
│   │   ├── i. Decimal Integer Constants
│   │   ├── ii. Octal Integer Constants
│   │   └── iii. Hexadecimal Integer Constants
│   └── B. Real (Floating-point) Constants
└── 2. Character Constants
    ├── A. Single Character Constants
    └── B. String Constants
```

---

# 1️⃣ Numeric Constants 🔢

Numeric constants represent numbers. They are divided into **integer constants** and **real (floating-point) constants**.

## A) Integer Constants

An integer constant is a whole number without a fractional part. It may be positive, negative, or zero.

### i) Decimal Integer Constants 🔟

- Written in the base-10 number system.
- Use the digits `0` to `9`.
- Do not use a prefix.
- Examples: `25`, `-100`, `0`, `2024`.

```c
#include <stdio.h>

int main(void) {
    int decimal_number = 25;
    printf("Decimal value: %d\\n", decimal_number);
    return 0;
}
```

**Output:**

```text
Decimal value: 25
```

### ii) Octal Integer Constants 🐙

- Written in the base-8 number system.
- Use only the digits `0` to `7`.
- Must begin with a leading `0`.
- Examples: `010` (decimal `8`), `017` (decimal `15`), `0644` (decimal `420`).

```c
#include <stdio.h>

int main(void) {
    int octal_number = 010;
    printf("Octal value: %o\\n", octal_number);
    printf("Decimal value: %d\\n", octal_number);
    return 0;
}
```

**Output:**

```text
Octal value: 10
Decimal value: 8
```

> 🚫 `018` is invalid as an octal integer constant because octal numbers cannot contain `8` or `9`.

### iii) Hexadecimal Integer Constants 🧮

- Written in the base-16 number system.
- Use digits `0` to `9` and letters `A` to `F` or `a` to `f`.
- Must begin with `0x` or `0X`.
- Examples: `0x1A` (decimal `26`) and `0X2F` (decimal `47`).

```c
#include <stdio.h>

int main(void) {
    int hexadecimal_number = 0x1A;
    printf("Hexadecimal value: %X\\n", hexadecimal_number);
    printf("Decimal value: %d\\n", hexadecimal_number);
    return 0;
}
```

**Output:**

```text
Hexadecimal value: 1A
Decimal value: 26
```

### 🖨️ Format specifiers for integer values

A constant does not have a format specifier by itself. **Format specifiers are used with functions such as `printf()` to display a value.**

| Integer value | `printf()` specifier | Example |
|---|---|---|
| Decimal `int` | `%d` or `%i` | `printf("%d", number);` |
| Octal `int` | `%o` | `printf("%o", number);` |
| Hexadecimal lowercase | `%x` | `printf("%x", number);` |
| Hexadecimal uppercase | `%X` | `printf("%X", number);` |
| Unsigned decimal | `%u` | `printf("%u", number);` |
| `long int` | `%ld` | `printf("%ld", number);` |
| `long long int` | `%lld` | `printf("%lld", number);` |

> ✅ `%i` and `%d` both display a decimal `int` with `printf()`. In `scanf()`, `%i` can detect the base from a prefix, while `%d` reads decimal input.

## B) Real (Floating-point) Constants 🌊

A real constant represents a number with a fractional part or a number written in exponential notation.

- Decimal examples: `3.14`, `0.001`, `-25.5`, `.5`, and `5.`
- Exponential examples: `2.5e3` means `2500`; `1.2E-4` means `0.00012`; `1e3` means `1000`.

By default, a floating-point constant has type `double`. Add `f` or `F` for `float`, or `L` for `long double`.

```c
#include <stdio.h>

int main(void) {
    double price = 3.14;
    float ratio = 2.5f;
    long double precise_value = 1.2L;

    printf("Price: %.2f\\n", price);
    printf("Ratio: %.1f\\n", ratio);
    printf("Precise value: %Lf\\n", precise_value);
    return 0;
}
```

| Type | `printf()` specifier | Example |
|---|---|---|
| `float` or `double` | `%f` | `printf("%f", value);` |
| Scientific notation | `%e` or `%E` | `printf("%e", value);` |
| Shortest suitable form | `%g` or `%G` | `printf("%g", value);` |
| `long double` | `%Lf` | `printf("%Lf", value);` |

> 🎯 `%.2f` displays two digits after the decimal point.

---

# 2️⃣ Character Constants 🔤

Character constants represent characters or text. They are divided into **single character constants** and **string constants**.

## A) Single Character Constants

- Contain one character.
- Are enclosed in **single quotes**.
- Examples: `'A'`, `'5'`, and `'$'`.
- Escape sequences such as `'\\n'` and `'\\t'` also represent one character.

> ⚠️ **Important:** The backslash (`\\`) introduces an **escape sequence**. Escape sequences are written inside character constants or string literals to represent control characters and characters that are difficult to type directly.

### 🧩 Escape sequences you should remember

| Escape sequence | Name | Meaning |
|---|---|---|
| `\\a` | Alert / bell | Produces an alert sound if supported |
| `\\b` | Backspace | Moves the cursor one position backward |
| `\\f` | Form feed / page feed | Advances to the next page on supported devices |
| `\\n` | Newline | Moves the cursor to the beginning of the next line |
| `\\r` | Carriage return | Moves the cursor to the beginning of the current line |
| `\\t` | Horizontal tab | Moves the cursor to the next horizontal tab stop |
| `\\v` | Vertical tab | Moves the cursor to the next vertical tab stop |
| `\\\\` | Backslash | Represents one literal backslash (`\\`) |
| `\\'` | Single quote | Represents a single quote (`'`) |
| `\\\"` | Double quote | Represents a double quote (`\"`) |
| `\\?` | Question mark | Represents a question mark (`?`) |
| `\\0` | Null character | Marks the end of a C string; value is zero |
| `\\ooo` | Octal character code | Character represented by one to three octal digits |
| `\\xhh` | Hexadecimal character code | Character represented by hexadecimal digits |

> 📝 **Terminology note:** `\\f` is called **form feed**. Some books also call it **page feed**. `\\r` is carriage return, `\\n` is newline, and `\\b` is backspace—they are different escape sequences.

### ✅ Escape-sequence example program

```c
#include <stdio.h>

int main(void) {
    printf("1. Newline\\n2. Horizontal tab\\tDone\\n");
    printf("3. Carriage return: ABC\\rXYZ\\n");
    printf("4. Backslash: \\\\\\n");
    printf("5. Single quote: \\\'\\n");
    printf("6. Double quote: \\\"\\n");
    printf("7. Question mark: \\?\\n");
    printf("8. Alert: \\a\\n");
    return 0;
}
```

> 💡 `\\n` and `\\t` are the most frequently used in beginner programs. The visible effect of `\\a`, `\\b`, `\\f`, `\\r`, and `\\v` depends on the terminal or output device.

```c
#include <stdio.h>

int main(void) {
    char newline = '\\n';
    char tab = '\\t';
    char quote = '\'';
    char backslash = '\\\\';

    printf("Line one%c%sLine two%cDone%c", newline, "", newline, tab);
    printf("%c%c%c%c\\n", quote, tab, backslash, quote);
    return 0;
}
```

**Format specifier:** Use `%c` with `printf()` to display a single character.

> ⚠️ `'5'` is a character constant, not the integer constant `5`. The first is displayed with `%c`; the second is displayed with `%d`.

## B) String Constants 💬

A string constant, commonly called a **string literal**, is a sequence of characters enclosed in **double quotes**.

Examples: `"Hello"`, `"C Programming"`, and `"123"`.

C automatically stores a null character, `\\0`, at the end of a string in a character array.

```c
#include <stdio.h>

int main(void) {
    char message[] = "Hello\\nWorld";
    printf("%s", message);
    return 0;
}
```

The array contains the characters of the text, followed by `\\0`:

```text
'H'  'e'  'l'  'l'  'o'  '\\n'  'W'  'o'  'r'  'l'  'd'  '\\0'
```

**Format specifier:** Use `%s` with `printf()` to display a string.

> ✅ `'A'` is one character. `"A"` is a string containing `'A'` followed by `\\0` in storage.

---

## 📏 Complete rules for constants and escape sequences

1. C constants are classified into numeric constants and character constants.
2. Numeric constants contain integer and real (floating-point) constants.
3. Integer constants may be decimal, octal, or hexadecimal.
4. Decimal integer constants use digits `0`–`9` and have no prefix.
5. Octal integer constants begin with `0` and use only digits `0`–`7`.
6. Hexadecimal integer constants begin with `0x` or `0X` and use digits `0`–`9` and letters `A`–`F` or `a`–`f`.
7. An integer constant cannot contain a decimal point, exponent, or spaces.
8. An integer constant can have suffixes such as `U`, `L`, or `LL`, for example `25U` or `100L`.
9. A real constant can use decimal notation or exponential notation.
10. A floating-point constant is `double` by default. Use `f`/`F` for `float` and `l`/`L` for `long double`.
11. A single character constant is enclosed in single quotes, such as `'A'`.
12. A string constant is enclosed in double quotes, such as `"Hello"`.
13. A character constant represents one character; a string constant represents a sequence of characters.
14. A string stored in a character array ends with the null character `\\0`.
15. An escape sequence begins with a backslash, such as `\\n`, `\\t`, or `\\\\`.
16. Use `\\'` for a single quote, `\\\"` for a double quote, `\\?` for a question mark, and `\\\\` for a literal backslash.
17. Use `\\a`, `\\b`, `\\f`, `\\n`, `\\r`, `\\t`, and `\\v` for standard control characters.
18. Escape sequences may appear inside character constants and string literals.
19. `\\0` is the null character used to terminate strings; it is not the same as the character `'0'`.
20. Format specifiers belong to functions such as `printf()` and are not part of the constant itself.

---

## 🧪 Quick practice

Identify each constant and choose a suitable `printf()` format specifier:

```c
42       // Decimal integer: %d
010      // Octal integer: %o
0x2A     // Hexadecimal integer: %x or %X
3.14     // Real constant: %f
'A'      // Single character constant: %c
'\\n'     // Escape-sequence character constant: %c
"Hello"  // String constant: %s
```

<details>
<summary>✨ Click to check your understanding</summary>

1. Which value represents decimal `10` in octal notation? **`012`** ✅
2. Which specifier displays an integer in hexadecimal notation? **`%x` or `%X`** ✅
3. Which is a string: `'C'` or `"C"`? **`"C"`** ✅
4. Which escape sequence moves to the next line? **`\\n`** ✅
5. Which escape sequence represents a literal backslash? **`\\\\`** ✅
6. Which escape sequence is used for a double quote inside a string? **`\\\"`** ✅

</details>

---

## 📚 Quick reference

| Main category | Subcategory | Example | `printf()` specifier |
|---|---|---|---|
| Numeric | Decimal integer | `100` | `%d` |
| Numeric | Octal integer | `0144` | `%o` |
| Numeric | Hexadecimal integer | `0x64` | `%x` or `%X` |
| Numeric | Real constant | `3.14` | `%f` |
| Character | Single character | `'A'` | `%c` |
| Character | Escape sequence | `'\\n'` | `%c` |
| Character | String constant | `"Hello"` | `%s` |

---

<div align="center">

### 🎉 You can now classify, write, print, and recognize constants and escape sequences in C!

</div>

<!-- This table is only for left/right page navigation, not for badge alignment. -->
<table width="100%">
<tr>
<td align="left">⬅️ <a href="03-keywords.md">03 · Keywords</a></td>
<td align="right"><a href="05-strings.md">05 · Strings</a> ➡️</td>
</tr>
</table>

<div align="center">

[⬆️ Back to top](#-04--constants-in-c)

</div>
