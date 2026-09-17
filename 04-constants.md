# 🔢 04 · Constants in C

<div align="center">

[![Language](https://img.shields.io/badge/Language-C-00599C?style=for-the-badge&logo=c&logoColor=white)](https://en.wikipedia.org/wiki/C_(programming_language))
[![Level](https://img.shields.io/badge/Level-Beginner-2ea44f?style=for-the-badge)](#)
[![Topic](https://img.shields.io/badge/Topic-Constants-8A2BE2?style=for-the-badge)](#)

### 🔒 A constant is a fixed value used by a C program.

</div>

> 💡 **Remember:** `25`, `3.14`, `'A'`, `"A"`, and `"Hello\nWorld"` are different kinds of constants or literals.

---

## 🧠 What is a constant?

A constant is a value written directly in a program. Its value does not change during evaluation.

```c
int age = 25;       // age is a variable; 25 is an integer constant
const int days = 7; // days cannot be modified through days
```

## 🗺️ Classification of constants

```text
Constants
├── 1. Numeric Constants
│   ├── A. Integer Constants
│   │   ├── i. Decimal
│   │   ├── ii. Octal
│   │   └── iii. Hexadecimal
│   └── B. Real (Floating-point) Constants
└── 2. Character Constants
    ├── A. Single Character Constants
    │   └── Escape Sequences
    └── B. String Constants
```

---

# 1️⃣ Numeric Constants 🔢

## A) Integer Constants

An integer constant is a whole number without a fractional part. Integer constants use different number systems, called **bases**.

### i) Decimal integer constants — base 10 🔟

- Use the base-10 number system.
- Use digits `0` to `9`.
- Have no special prefix.
- Examples: `25`, `-100`, `0`, and `2024`.

### ii) Octal integer constants — base 8 🐙

- Use the base-8 number system.
- Use only digits `0` to `7`.
- Begin with a leading `0`.
- Example: `010` is decimal `8` because `1 × 8 + 0 = 8`.
- Example: `017` is decimal `15` because `1 × 8 + 7 = 15`.

### iii) Hexadecimal integer constants — base 16 🧮

- Use the base-16 number system.
- Use digits `0` to `9` and letters `A` to `F` or `a` to `f`.
- Begin with `0x` or `0X`.
- Example: `0x1A` is decimal `26` because `1 × 16 + 10 = 26`.
- Example: `0x2F` is decimal `47` because `2 × 16 + 15 = 47`.

> ⚠️ **Correction:** Hexadecimal uses **base 16**, not base 10. Decimal uses base 10, octal uses base 8, and hexadecimal uses base 16.

### 🧪 One program for decimal, octal, and hexadecimal constants

The same integer value can be written in three bases. Here, decimal `26`, octal `032`, and hexadecimal `0x1A` all represent the same value.

```c
#include <stdio.h>

int main(void) {
    int decimal_value = 26;  // base 10
    int octal_value = 032;   // base 8: 3 × 8 + 2 = 26
    int hex_value = 0x1A;    // base 16: 1 × 16 + 10 = 26

    printf("Decimal constant:     %d\n", decimal_value);
    printf("Octal as decimal:     %d\n", octal_value);
    printf("Hexadecimal as decimal: %d\n", hex_value);

    printf("Same value in decimal:     %d\n", decimal_value);
    printf("Same value in octal:       %o\n", decimal_value);
    printf("Same value in hexadecimal: %X\n", decimal_value);

    return 0;
}
```

**Output:**

```text
Decimal constant:     26
Octal as decimal:     26
Hexadecimal as decimal: 26
Same value in decimal:     26
Same value in octal:       32
Same value in hexadecimal: 1A
```

> 🚫 `018` is invalid octal notation because `8` is not an octal digit.

### 🖨️ Integer `printf()` format specifiers

| Representation/type | Specifier | Meaning |
|---|---|---|
| Decimal `int` | `%d` or `%i` | Base-10 output |
| Octal `int` | `%o` | Base-8 output |
| Hexadecimal `int` | `%x` or `%X` | Base-16 output |
| Unsigned `int` | `%u` | Unsigned decimal output |
| `long int` | `%ld` | Long decimal output |
| `long long int` | `%lld` | Long-long decimal output |

> 📌 A constant does not have a format specifier by itself. The specifier tells `printf()` how to display the value.

## B) Real (floating-point) constants 🌊

Examples: `3.14`, `.5`, `5.`, `2.5e3`, and `1.2E-4`. A floating-point literal is `double` by default; `2.5f` is `float` and `2.5L` is `long double`.

```c
#include <stdio.h>

int main(void) {
    double value = 3.14;
    printf("Value: %.2f\n", value);
    return 0;
}
```

Common `printf()` specifiers are `%f`, `%e`/`%E`, `%g`/`%G`, and `%Lf` for `long double`.

---

# 2️⃣ Character Constants 🔤

## A) Single character constants

A valid single character constant contains exactly one character or one escape sequence between single quotes.

```c
'A'       // valid ordinary character
'5'       // character 5, not integer 5
' '       // one space
'\n'      // one newline character
'\t'      // one tab character
'\''      // one single quote
'\\'      // one backslash
'\x41'    // hexadecimal code for A
'\101'    // octal code for A
```

### ❌ Invalid single character constants

```c
''        // empty character constant
'AB'      // more than one character
'A        // missing closing quote
'\q'      // not a standard escape sequence
'\'       // the backslash escapes the closing quote
```

`"A"` is valid C, but it is a **string literal**, not a single character constant. Use `%c` with `printf()` for a character.

### 🧩 Escape sequences

| Sequence | Name | Meaning |
|---|---|---|
| `\a` | Alert/bell | Audible or visual alert if supported |
| `\b` | Backspace | Moves back one position |
| `\f` | Form feed/page feed | Advances to the next page on supported devices |
| `\n` | Newline | Moves to the next line |
| `\r` | Carriage return | Moves to the beginning of the current line |
| `\t` | Horizontal tab | Moves to the next tab stop |
| `\v` | Vertical tab | Moves to the next vertical tab stop |
| `\\` | Backslash | A literal backslash |
| `\'` | Single quote | A literal single quote |
| `\"` | Double quote | A literal double quote |
| `\?` | Question mark | A literal question mark |
| `\0` | Null character | Character value zero |
| `\ooo` | Octal escape | One to three octal digits |
| `\xhh` | Hexadecimal escape | One or more hexadecimal digits |

```c
#include <stdio.h>

int main(void) {
    printf("First line\nSecond line\n");
    printf("Tab:\tDone\n");
    printf("Quote: \"C\"\n");
    printf("Backslash: \\\n");
    printf("Question mark: \?\n");
    return 0;
}
```

## B) String constants (string literals) 💬

A string constant is a sequence of characters enclosed in double quotes. It may contain zero, one, or many visible characters.

```c
""              // empty string: zero visible characters
"A"             // one visible character
"      "        // exactly six spaces
"Hello"         // five visible characters
"Hello\nWorld"  // contains a newline character
```

### Empty string, null character, and zero

| Term | Example | Meaning |
|---|---|---|
| Empty string | `""` | Zero visible characters; an array stores only `\0` |
| Null character | `'\0'` | One character whose value is zero |
| Digit zero | `'0'` or `"0"` | The printable digit character zero |
| Null pointer | `NULL` | A pointer value, not a string or character |

```c
char empty[] = "";        // '\0'; sizeof is 1
char one[] = "A";         // 'A', '\0'; sizeof is 2
char spaces[] = "      "; // six spaces, '\0'; sizeof is 7
char line[] = "A\nB";     // 'A', newline, 'B', '\0'; sizeof is 4
```

The terminating `\0` is automatically added when a string literal initializes a character array. It is not visible and is not counted by `strlen()`.

### One-character string versus character constant

```c
char character = 'A'; // one character; print with %c
char text[] = "A";    // 'A' and '\0'; print with %s
```

`'A'` and `"A"` are not interchangeable. Likewise, ` '\n' ` is one newline character, while `"\n"` is a one-character string plus its terminating `\0` when stored in an array.

### Newline inside a string

```c
#include <stdio.h>

int main(void) {
    printf("First line\nSecond line\n");
    return 0;
}
```

Use `\n` for a newline. Do not place an unescaped physical line break inside a string literal.

### Six spaces, `strlen()`, and `sizeof`

```c
#include <stdio.h>
#include <string.h>

int main(void) {
    char six_spaces[] = "      ";

    printf("[%s]\n", six_spaces);
    printf("Visible length: %zu\n", strlen(six_spaces)); // 6
    printf("Array size: %zu\n", sizeof six_spaces);       // 7
    return 0;
}
```

`strlen()` counts characters before the first `\0`. `sizeof` includes the terminating `\0` when used on the array itself.

### Null character inside a string

```c
#include <stdio.h>
#include <string.h>

int main(void) {
    char text[] = "A\0B";

    printf("%s\n", text);              // prints A only
    printf("Length: %zu\n", strlen(text)); // 1
    printf("Array size: %zu\n", sizeof text); // 4: A, \0, B, \0
    return 0;
}
```

`%s` and `strlen()` stop at the first `\0`, even when later array elements still exist.

---

## 📏 Rules to remember

1. Decimal integer constants use base 10, octal constants use base 8, and hexadecimal constants use base 16.
2. Decimal integers use digits `0`–`9` and no prefix.
3. Octal integers begin with `0` and use only `0`–`7`.
4. Hexadecimal integers begin with `0x` or `0X` and use `0`–`9` and `A`–`F`.
5. A single character constant uses single quotes and contains one character or one escape sequence.
6. A string constant uses double quotes and may contain zero, one, or many characters.
7. `''`, `'AB'`, and unclosed character literals are invalid ordinary single-character constants.
8. `' '` is a valid one-space character constant.
9. `""` is a valid empty string; a character array initialized with it stores one `\0`.
10. Six spaces in `"      "` are six data characters plus one terminating `\0`.
11. `\n` is a newline escape sequence; an unescaped physical newline cannot be placed inside a string literal.
12. `\0` is the null character, not the digit character `'0'` and not `NULL`.
13. `%c` prints one character; `%s` prints a string up to its first `\0`.
14. A string literal initialized into an array receives an automatic terminating `\0`.
15. Escape sequences can occur in character constants and string literals.
16. The visible effect of `\a`, `\b`, `\f`, `\r`, and `\v` depends on the terminal or output device.

---

## 🧪 Quick practice

```c
'A'       // valid single character
' '       // valid single space
'\n'      // valid escape-sequence character
"A"       // one-character string plus '\0'
"      "  // six spaces plus '\0'
""        // empty string; array storage contains '\0'
'AB'      // invalid ordinary single character constant
''        // invalid empty character constant
```

<details>
<summary>✨ Check your understanding</summary>

1. What base does decimal use? **10**.
2. What base does octal use? **8**.
3. What base does hexadecimal use? **16**.
4. What is the length of `"      "`? **6**.
5. What is the array size of `char s[] = "      ";`? **7**.
6. Is `""` the same as `'\0'`? **No.** The first is an empty string; the second is one null character.
7. Which specifier prints one character? **`%c`**.
8. Which specifier prints a string? **`%s`**.

</details>

---

## 📚 Quick reference

| Category | Example | Base/meaning | Output specifier |
|---|---|---|---|
| Decimal integer | `26` | Base 10 | `%d` |
| Octal integer | `032` | Base 8; value 26 | `%o` |
| Hexadecimal integer | `0x1A` | Base 16; value 26 | `%x` or `%X` |
| Real constant | `3.14` | Floating-point value | `%f` |
| Character | `'A'` | One character | `%c` |
| Escape character | `'\n'` | One newline character | `%c` |
| Empty string | `""` | Zero visible characters | `%s` |
| Six-space string | `"      "` | Six spaces plus `\0` | `%s` |

---

<div align="center">

### 🎉 You can now distinguish bases, characters, strings, whitespace, newlines, and null characters!

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
