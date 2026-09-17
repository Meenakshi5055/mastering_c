# 06 · Special Symbols in C

![C](https://img.shields.io/badge/Language-C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Level](https://img.shields.io/badge/Level-Beginner-2ea44f?style=for-the-badge)
![Topic](https://img.shields.io/badge/Topic-Special%20Symbols-f39c12?style=for-the-badge)

> 🧭 **In this module:** Learn how punctuation and special characters give structure and meaning to C programs.

## 🎯 Learning goals

By the end of this module, you will be able to:

- recognize the most common special symbols in C;
- understand where each symbol is used; and
- distinguish an escape sequence from the carriage-return character (`\r`).

---

## 🔎 What are special symbols?

Special symbols are characters with a **reserved purpose** in C. They help the compiler understand the structure of your program—for example, where a statement ends, where a block begins, or how to access a structure member.

Think of them as the **punctuation marks of C**: just as punctuation makes written sentences easier to read, special symbols make code meaningful and organized.

> 💡 **Quick tip:** A symbol can have different meanings depending on its context. For example, `*` can mean multiplication, declare a pointer, or dereference a pointer.

---

## 🧩 Common special symbols in C

| Symbol | Name | What it does | Example |
|:---:|---|---|---|
| `;` | Semicolon | Ends a statement | `count = 1;` |
| `,` | Comma | Separates declarations or arguments | `int x, y;` |
| `{ }` | Curly braces | Groups a block of code | `if (ok) { ... }` |
| `( )` | Parentheses | Groups expressions and holds function arguments | `printf("Hi");` |
| `[ ]` | Square brackets | Declares and accesses array elements | `scores[0]` |
| `#` | Hash / pound | Starts a preprocessor directive | `#include <stdio.h>` |
| `" "` | Double quotes | Encloses a string literal | `"Hello"` |
| `' '` | Single quotes | Encloses a character constant | `'A'` |
| `.` | Dot | Accesses a structure member directly | `student.age` |
| `->` | Arrow | Accesses a member through a structure pointer | `ptr->age` |
| `*` | Asterisk | Multiplication, pointer declaration, or dereference | `int *ptr;` |
| `&` | Ampersand | Gets an address or performs bitwise AND | `&number` |
| `:` | Colon | Separates a label or parts of `?:` | `result = ok ? 1 : 0;` |
| `\` | Backslash | Starts an escape sequence | `"Line 1\nLine 2"` |

> ⚠️ **Remember:** `*` and `&` are included here because they are important symbols, but they are also operators in some contexts.

---

## 🧪 Example: several symbols working together

```c
#include <stdio.h>

struct Student {
    char name[20];
    int age;
};

int main(void) {
    struct Student student = {"Meenakshi", 20};
    struct Student *pointer = &student;

    printf("%s is %d years old\n", pointer->name, student.age);
    return 0;
}
```

### 🧠 Read the symbols in the example

- `#include` uses `#` to start a preprocessor directive.
- `{ }` define the structure and function blocks.
- `;` ends declarations and statements.
- `[20]` reserves space for an array of 20 characters.
- `&student` gets the address of `student`.
- `pointer->name` accesses a member through a pointer.
- `student.age` accesses a member directly.
- `\n` moves the output to the next line.

---

## ↩️ Escape sequences and carriage return

### What is an escape sequence?

An **escape sequence** is a backslash (`\`) followed by another character. Together, they represent a special character or action inside a string or character constant.

For example, `\n` does not print the two characters `\` and `n`; it tells the output device to move to a new line.

### Is carriage return the same as an escape sequence?

**Carriage return (`\r`) is one type of escape sequence.** It is not a separate category.

- **Escape sequence** = the general concept: `\` plus another character.
- **Carriage return** = one specific escape sequence: `\r`.

### 📚 Common escape sequences

| Escape sequence | Meaning | Everyday idea |
|:---:|---|---|
| `\n` | New line | Move down to the next line |
| `\r` | Carriage return | Return to the start of the current line |
| `\t` | Horizontal tab | Insert a tab space |
| `\\` | Backslash | Print a backslash |
| `\'` | Single quote | Print `'` inside a character/string context |
| `\"` | Double quote | Print `"` inside a string |
| `\0` | Null character | Marks the end of a C string |
| `\a` | Alert | Request a bell or alert sound |
| `\b` | Backspace | Move one position backward |

> 📝 **Important:** `\0` is the null character. It is different from the digit character `'0'` and from the null pointer `NULL`.

---

## `\n` versus `\r`

| Sequence | Cursor movement |
|:---:|---|
| `\n` | Moves to a new line. |
| `\r` | Returns to the beginning of the current line without moving down. |

```c
#include <stdio.h>

int main(void) {
    printf("Hello\rWorld\n");
    return 0;
}
```

### Expected terminal output

```text
World
```

`\r` moves the cursor back to the beginning of the same line, so `World` is written over `Hello`. The exact display can vary with the terminal and output destination; when output is redirected to a file, both control characters are stored rather than visually overwriting text.

> ✅ **Practical use:** `\r` is often used to refresh a progress message on one terminal line.

---

## ✅ Quick recap

- Special symbols provide structure and meaning in C.
- `;` ends statements, while `{ }` group blocks of code.
- `.` accesses a structure member directly; `->` accesses one through a pointer.
- A backslash introduces an escape sequence.
- `\r` is a carriage-return escape sequence, while `\n` starts a new line.

---

<div align="left">
  ⬅️ <a href="05-strings.md">Previous: 05. Strings</a>
</div>
<div align="right">
  <a href="07-operators.md">Next: 07. Operators</a> ➡️
</div>
