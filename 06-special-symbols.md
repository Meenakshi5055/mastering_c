## 06: Special Symbols in C

![C](https://img.shields.io/badge/Language-C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Level](https://img.shields.io/badge/Level-Beginner-2ea44f?style=for-the-badge)
![Topic](https://img.shields.io/badge/Topic-Special%20Symbols-f39c12?style=for-the-badge)

> 🧭 **Focus of this lesson:** Learn the symbols that give C code its structure, meaning, and readability.

### 🎯 What are special symbols?

Special symbols are characters in C that have a **special meaning** in the language. They are not just letters or numbers — they help define code structure, access values, separate parts of declarations, and begin preprocessor instructions.

These symbols act like the **punctuation in C**.

---

### ✅ What belongs in special symbols?

The most important special symbols are the ones used for:

- ending statements
- grouping code blocks
- separating values or arguments
- enclosing strings and characters
- accessing data in arrays and structures
- beginning preprocessor instructions

> ⚠️ **Important:** `\r` (carriage return) does not belong to the main “special symbol” list as a core symbol. It belongs to the category of **escape sequences**. `\r` is a specific escape sequence, not a standalone special symbol like `;` or `{}`.

---

### 📊 Special symbols in C

| Symbol | Name | Category | Purpose |
|:---:|---|---|---|
| `;` | Semicolon | Delimiter | Ends a statement |
| `,` | Comma | Delimiter | Separates variables, function arguments, or values |
| `{ }` | Curly braces | Block delimiter | Marks the start and end of a block of code |
| `( )` | Parentheses | Grouping symbol | Used in function calls, function definitions, and expressions |
| `[ ]` | Square brackets | Array symbol | Declares arrays and accesses array elements |
| `.` | Dot | Member access | Accesses a member of a structure directly |
| `->` | Arrow | Pointer member access | Accesses a structure member through a pointer |
| `:` | Colon | Delimiter | Used in labels and in the ternary operator |
| `#` | Hash / pound | Preprocessor | Starts a preprocessor directive like `#include` |
| `" "` | Double quotes | String literal | Encloses a string |
| `' '` | Single quotes | Character literal | Encloses a single character |
| `\` | Backslash | Escape-sequence starter | Starts escape sequences like `\n`, `\t`, `\r` |
| `//` | Double slash | Comment | Starts a single-line comment |
| `/* */` | Block comment | Comment | Starts and ends a multi-line comment |
| `...` | Ellipsis | Variadic symbol | Used in function declarations with variable arguments |
| `?` | Question mark | Conditional symbol | Used in the ternary operator `condition ? a : b` |
| `##` | Token pasting | Preprocessor | Used in macros for combining tokens |
| `<>` | Angle brackets | Header include syntax | Used in `#include <stdio.h>` |

---

### 🧠 Example using multiple special symbols

```c
#include <stdio.h>

struct Student {
    char name[20];
    int age;
};

int main(void) {
    struct Student s1 = {"Meenakshi", 20};
    struct Student *ptr = &s1;

    printf("%s is %d years old\n", ptr->name, s1.age);
    return 0;
}
```

Here:

- `#include` starts a preprocessor directive
- `{ }` marks the structure and function blocks
- `;` ends statements
- `[]` declares the string array
- `&` gets the address of `s1`
- `->` accesses a member through the pointer
- `.` accesses a member directly
- `\n` is an escape sequence

---

### 🔤 Carriage return `\r`: where does it belong?

`\r` is not a big special symbol like `;` or `{}`. It belongs to the concept of **escape sequences**.

#### Escape sequence = general concept
A backslash followed by another character is called an escape sequence.

Examples:

- `\n` = new line
- `\t` = tab
- `\r` = carriage return
- `\\` = backslash itself

#### Why it is not part of the core special symbols list

Because `\r` is not a structural symbol like braces or semicolon. It is used inside string literals to represent a special control character.

So the correct place is:

- `\` belongs in the special symbol list
- `\r` belongs under **escape sequences**

---

### 📌 Common escape sequences in C

| Escape sequence | Meaning |
|:---:|---|
| `\n` | New line |
| `\r` | Carriage return (moves to the start of the same line) |
| `\t` | Horizontal tab |
| `\\` | Backslash |
| `\'` | Single quote |
| `\"` | Double quote |
| `\0` | Null character |
| `\a` | Alert / bell |
| `\b` | Backspace |

---

### 🧪 Difference between `\n` and `\r`

- `\n` moves the cursor to the **next line**.
- `\r` moves the cursor **to the beginning of the current line**.

```c
printf("Hello\rWorld\n");
```

This prints:

```text
World
```

Because `\r` returns the cursor to the start of the same line, and then `World` overwrites `Hello`.

---

### ✅ Quick recap

- `;`, `{}`, `()`, `[]`, `.` and `->` are classic special symbols.
- `#` and `##` are important in preprocessor programming.
- `\` is the special symbol that begins escape sequences.
- `\r` is a **type of escape sequence**, not a main special symbol itself.
- `//`, `/* */`, and `...` are also useful symbolic tokens in C.

---

<div align="left">
  ⬅️ <a href="05-strings.md">Previous: 05. Strings</a>
</div>
<div align="right">
  <a href="07-operators.md">Next: 07. Operators</a> ➡️
</div>
