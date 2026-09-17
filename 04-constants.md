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
const int days = 7; // days is a read-only object after initialization
```

## 🗺️ Classification

```text
Constants
���── 1. Numeric Constants
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

Whole numbers without a fractional part.

- **Decimal:** `25`, `-100`, `0`
- **Octal:** `010` is decimal `8`; begins with `0` and uses only `0`–`7`.
- **Hexadecimal:** `0x1A` is decimal `26`; begins with `0x` or `0X` and uses `0`–`9`, `A`–`F`, or `a`–`f`.

```c
#include <stdio.h>

int main(void) {
    int decimal = 25;
    int octal = 010;       // decimal 8
    int hexadecimal = 0x1A; // decimal 26

    printf("%d %o %X\n", decimal, octal, hexadecimal);
    return 0;
}
```

> 🚫 `018` is invalid octal notation because `8` is not an octal digit.

### Integer `printf()` specifiers

| Representation/type | Specifier |
|---|---|
| Decimal `int` | `%d` or `%i` |
| Octal `int` | `%o` |
| Hexadecimal `int` | `%x` or `%X` |
| Unsigned `int` | `%u` |
| `long int` | `%ld` |
| `long long int` | `%lld` |

## B) Real (Floating-point) Constants 🌊

Examples: `3.14`, `.5`, `5.`, `2.5e3`, and `1.2E-4`. A floating-point literal is `double` by default; `2.5f` is `float` and `2.5L` is `long double`.

```c
#include <stdio.h>

int main(void) {
    double value = 3.14;
    printf("%.2f\n", value);
    return 0;
}
```

Use `%f`, `%e`/`%E`, `%g`/`%G`, or `%Lf` with `printf()` as appropriate.

---

# 2️⃣ Character Constants 🔤

## A) Single Character Constants

A valid single character constant contains **exactly one character** or **one escape sequence** between single quotes.

### ✅ Valid single character constants

```c
'A'       // one ordinary character
'5'       // character 5, not integer 5
' '       // one space
'\n'      // one newline character
'\t'      // one tab character
'\''      // one single-quote character
'\\'      // one backslash character
'\x41'    // character code for A
'\101'    // octal character code for A
```

### ❌ Invalid single character constants

```c
'AB'      // more than one character
''        // empty character constant
'A        // missing closing quote
"A"       // valid string literal, not a character constant
'\'       // invalid: the backslash escapes the closing quote
'\q'      // not a standard C escape sequence
```

> ⚠️ Some implementations accept multi-character constants such as `'AB'` as an extension, but they are not a normal one-character constant and their value is implementation-defined. Do not use them for beginner C programs.

### 🧩 Escape sequences

The backslash introduces an escape sequence. It may represent a control character or a character that is difficult to type directly.

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
| `\0` | Null character | Character value zero; commonly terminates strings |
| `\ooo` | Octal escape | One to three octal digits |
| `\xhh` | Hex escape | One or more hexadecimal digits |

Use `%c` to print a single character:

```c
#include <stdio.h>

int main(void) {
    char letter = 'A';
    char newline = '\n';
    char quote = '\'';
    char slash = '\\';

    printf("Letter: %c%c", letter, newline);
    printf("Quote: %c%c", quote, newline);
    printf("Backslash: %c%c", slash, newline);
    return 0;
}
```

> 📝 `\n` is one character in a character constant, even though its source spelling uses two characters: backslash and `n`.

## B) String Constants (String Literals) 💬

A string constant is a sequence of characters enclosed in double quotes. It may contain zero, one, or many characters.

```c
""              // empty string: zero visible characters
"A"             // one visible character
"      "        // six space characters
"Hello"         // five visible characters
"Hello\nWorld"  // text containing a newline character
```

### 🔲 Empty/null string versus null character

These terms must not be confused:

| Term | Example | Meaning |
|---|---|---|
| Empty string | `""` | Zero visible characters, stored as one element: `\0` |
| Null character | `\0` or `'\0'` | One character whose value is zero |
| Null pointer | `NULL` | A pointer value that points to no object; not a string |
| Text zero | `'0'` or `"0"` | The digit character zero; not the null character |

```c
char empty[] = "";       // array contains only '\0'; sizeof empty is 1
char one[] = "A";        // 'A', '\0'; sizeof one is 2
char spaces[] = "      "; // six spaces, then '\0'; sizeof spaces is 7
char line[] = "A\nB";    // 'A', newline, 'B', '\0'; sizeof line is 4
```

The terminating `\0` is added automatically when a string literal initializes a character array. It is **not displayed** and is not counted as visible text.

### One character in a string versus a character constant

```c
char character = 'A';  // one character; use %c
char text[] = "A";     // string: 'A' followed by '\0'; use %s
```

`'A'` and `"A"` are not interchangeable. Similarly, `"\n"` is a one-character string plus its terminating `\0`, while `'\n'` is one newline character.

### Newline inside a string

```c
#include <stdio.h>

int main(void) {
    printf("First line\nSecond line\n");
    printf("The string above contains a newline escape sequence.\n");
    return 0;
}
```

A string cannot contain an unescaped physical line break between its quotes. Use `\n` instead:

```c
const char *valid = "First line\nSecond line";
/* const char *invalid = "First line
   Second line"; */
```

### Six white spaces

Whitespace is still data inside a string. The following string contains exactly six space characters:

```c
#include <stdio.h>
#include <string.h>

int main(void) {
    char six_spaces[] = "      ";

    printf("[%s]\n", six_spaces);          // spaces are visible between brackets
    printf("Length: %zu\n", strlen(six_spaces)); // 6
    printf("Storage: %zu\n", sizeof six_spaces); // 7, including '\0'
    return 0;
}
```

Use `%s` to print a string. `strlen()` counts characters before `\0`; `sizeof` includes the terminating `\0` when used on the array itself.

### Null character inside a string

```c
#include <stdio.h>
#include <string.h>

int main(void) {
    char text[] = "A\0B";

    printf("%s\n", text);          // prints only A
    printf("Length: %zu\n", strlen(text)); // 1
    printf("Array size: %zu\n", sizeof text); // 4: A, \0, B, \0
    return 0;
}
```

A `\0` inside a string stops functions such as `%s` and `strlen()` at that point, although later array elements may still exist.

---

## 📏 Rules to remember

1. Single character constants use single quotes; string constants use double quotes.
2. A single character constant must contain one character or one escape sequence.
3. `''`, `'AB'`, and an unclosed quote are invalid ordinary character constants.
4. `'A'` is a character; `"A"` is a string containing `A` and `\0`.
5. A space is a character, so `' '` is valid.
6. A string may contain zero characters: `""` is valid and has only its terminating `\0` in an array.
7. Six spaces in `"      "` are six data characters plus one terminating `\0`.
8. Escape sequences begin with a backslash and can occur in character constants and strings.
9. `\n` is a newline character; it is not the same as the two ordinary characters `\\` and `n`.
10. Use `\n` for a newline inside a string; do not place an unescaped physical line break inside a string literal.
11. `\0` is the null character, not the digit character `'0'`.
12. A string initialized into an array receives an automatic terminating `\0`.
13. A string literal can contain an escaped quote, backslash, tab, newline, or other escape sequence.
14. `%c` prints one character; `%s` prints characters up to the first `\0`.
15. A null character is not the same as a null pointer (`NULL`).
16. Ordinary C string literals cannot contain an unescaped double quote or unescaped backslash.
17. Multi-character constants such as `'AB'` should not be used as ordinary single-character constants.
18. The visible effect of `\a`, `\b`, `\f`, `\r`, and `\v` depends on the terminal or output device.

---

## 🧪 Quick practice

```c
'A'       // valid single character
' '       // valid single space
'\n'      // valid escape-sequence character
"A"       // one-character string, plus '\0'
"      "  // six spaces, plus '\0'
""        // empty string, plus '\0' when stored in an array
'AB'      // invalid for a normal single-character lesson
''        // invalid empty character constant
```

<details>
<summary>✨ Check your understanding</summary>

1. What is the length of `"      "`? **6**.
2. What is its array size after initialization? **7**, because of the final `\0`.
3. What does `"A\nB"` contain? **A, newline, B, and the terminating `\0`**.
4. Is `""` a null character? **No.** It is an empty string; its array contains a terminating null character.
5. Which prints a character: `%c` or `%s`? **`%c`**.
6. Which prints a string? **`%s`**.

</details>

---

## 📚 Quick reference

| Category | Example | Meaning | Output specifier |
|---|---|---|---|
| Integer | `25` | Decimal integer | `%d` |
| Real | `3.14` | Floating-point value | `%f` |
| Character | `'A'` | One character | `%c` |
| Escape character | `'\n'` | One newline character | `%c` |
| Empty string | `""` | Zero visible characters | `%s` |
| One-character string | `"A"` | `A` plus `\0` in storage | `%s` |
| Six-space string | `"      "` | Six spaces plus `\0` in storage | `%s` |
| Newline string | `"A\nB"` | A, newline, B, then `\0` | `%s` |

---

<div align="center">

### 🎉 You can now distinguish characters, strings, whitespace, newlines, and null characters!

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
