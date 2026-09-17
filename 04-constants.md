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

A **constant** is a value that remains fixed while a program is running. For example, `25` is an integer constant in the following statement:

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
| Hexadecimal `int` lowercase | `%x` | `printf("%x", number);` |
| Hexadecimal `int` uppercase | `%X` | `printf("%X", number);` |
| Unsigned decimal | `%u` | `printf("%u", number);` |
| `long int` | `%ld` | `printf("%ld", number);` |
| `long long int` | `%lld` | `printf("%lld", number);` |

> ✅ `%i` and `%d` both display a decimal `int` with `printf()`. In `scanf()`, `%i` can also detect decimal, octal, or hexadecimal input from its prefix, while `%d` reads decimal input.

## B) Real (Floating-point) Constants 🌊

A real constant represents a number with a fractional part or a number written in exponential notation.

### Decimal form

Examples: `3.14`, `0.001`, `-25.5`, `.5`, and `5.`

### Exponential form

The pattern is:

```text
mantissa e exponent
```

Examples:

- `2.5e3` means `2.5 × 10³`, which is `2500`.
- `1.2E-4` means `1.2 × 10⁻⁴`, which is `0.00012`.
- `1e3` means `1000`.

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

### 🖨️ Format specifiers for real values

| Type | `printf()` specifier | Example |
|---|---|---|
| `float` or `double` | `%f` | `printf("%f", value);` |
| Scientific notation | `%e` or `%E` | `printf("%e", value);` |
| Shortest suitable form | `%g` or `%G` | `printf("%g", value);` |
| `long double` | `%Lf` | `printf("%Lf", value);` |

> 🎯 Precision can be selected with a number after `%`. For example, `%.2f` displays two digits after the decimal point.

---

# 2️⃣ Character Constants 🔤

Character constants represent characters or text. They are divided into **single character constants** and **string constants**.

## A) Single Character Constants

- Contain one character.
- Are enclosed in **single quotes**.
- Examples: `'A'`, `'5'`, `'$'`.
- Escape sequences such as `'\\n'` and `'\\t'` also represent one character.

```c
#include <stdio.h>

int main(void) {
    char grade = 'A';
    char newline = '\\n';

    printf("Grade: %c\\n", grade);
    printf("The next output begins after a newline.%c", newline);
    return 0;
}
```

**Format specifier:** Use `%c` with `printf()` to display a character.

> ⚠️ `'5'` is a character constant, not the integer constant `5`. The first is displayed with `%c`; the second is displayed with `%d`.

## B) String Constants 💬

A string constant, commonly called a **string literal**, is a sequence of characters enclosed in **double quotes**.

Examples: `"Hello"`, `"C Programming"`, and `"123"`.

C automatically stores a null character, `\\0`, at the end of a string in a character array.

```c
#include <stdio.h>

int main(void) {
    char message[] = "Hello";

    printf("%s\\n", message);
    return 0;
}
```

The array contains:

```text
'H'  'e'  'l'  'l'  'o'  '\0'
```

**Format specifier:** Use `%s` with `printf()` to display a string.

> ✅ `'A'` is one character. `"A"` is a string containing `'A'` followed by `\\0` in storage.

---

## 📏 Complete rules for constants

1. C constants are classified here into two main categories: **numeric constants** and **character constants**.
2. Numeric constants contain integer constants and real (floating-point) constants.
3. Integer constants may be decimal, octal, or hexadecimal.
4. Decimal integer constants use digits `0`–`9` and have no prefix.
5. Octal integer constants begin with `0` and use only digits `0`–`7`.
6. Hexadecimal integer constants begin with `0x` or `0X` and use digits `0`–`9` and letters `A`–`F` or `a`–`f`.
7. An integer constant cannot contain a decimal point, exponent, or spaces.
8. An integer constant can have an integer suffix such as `U`, `L`, or `LL`, for example `25U` or `100L`.
9. A real constant can use decimal notation or exponential notation.
10. A real constant must contain digits appropriately around its decimal point or contain an exponent; forms such as `.5`, `5.`, and `1e3` are valid C forms.
11. A floating-point constant is `double` by default. Use `f`/`F` for `float` and `l`/`L` for `long double`.
12. A single character constant is enclosed in single quotes, such as `'A'`.
13. A string constant is enclosed in double quotes, such as `"Hello"`.
14. A character constant represents one character; a string constant represents a sequence of characters.
15. A string stored in a character array ends with the null character `\\0`.
16. Format specifiers are used to display constants and variables with input/output functions; they are not part of the constant itself.
17. Use `%d`, `%i`, `%o`, and `%x`/`%X` for common integer output; use `%f`, `%e`, `%g`, `%c`, and `%s` for floating-point, character, and string output.

---

## 🧪 Quick practice

Identify each constant and choose a suitable `printf()` format specifier:

```c
42       // Decimal integer: %d
010      // Octal integer: %o
0x2A     // Hexadecimal integer: %x or %X
3.14     // Real constant: %f
'A'      // Single character constant: %c
"Hello"  // String constant: %s
```

<details>
<summary>✨ Click to check your understanding</summary>

1. Which value represents decimal `10` in octal notation? **`012`** ✅
2. Which specifier displays an integer in hexadecimal notation? **`%x` or `%X`** ✅
3. Which is a string: `'C'` or `"C"`? **`"C"`** ✅

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
| Character | String constant | `"Hello"` | `%s` |

---

<div align="center">

### 🎉 You can now classify, write, print, and recognize constants in C!

</div>

<!-- The table below is used only for navigation alignment, not for the badges. -->
<table width="100%">
<tr>
<td align="left">⬅️ <a href="03-keywords.md">03 · Keywords</a></td>
<td align="right"><a href="05-strings.md">05 · Strings</a> ➡️</td>
</tr>
</table>

<div align="center">

[⬆️ Back to top](#-04--constants-in-c)

</div>
