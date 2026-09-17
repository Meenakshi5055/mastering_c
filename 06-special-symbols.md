## 06: Special Symbols

**What are Special Symbols?**
Special symbols are characters that have a **specific, reserved purpose** in C, other than being letters, digits, or operators. They're used to structure code — grouping statements, separating parts of a program, and marking where things begin or end.

---

### List of Special Symbols in C

| Symbol | Name | Purpose |
|---|---|---|
| `;` | Semicolon | Ends every statement (like a full stop) |
| `,` | Comma | Separates items — multiple variables, function arguments |
| `{ }` | Curly Braces | Marks the start and end of a block of code (function body, loop body, etc.) |
| `( )` | Parentheses | Used in function calls/definitions, and to group expressions |
| `[ ]` | Square Brackets | Used for array declaration and accessing array elements |
| `#` | Hash / Pound | Used before preprocessor directives (e.g., `#include`, `#define`) |
| `"  "` | Double Quotes | Encloses string literals |
| `'  '` | Single Quotes | Encloses a single character constant |
| `.` | Period / Dot | Accesses a member of a structure (`student.age`) |
| `->` | Arrow | Accesses a structure member through a pointer |
| `*` | Asterisk | Declares or dereferences a pointer (also used as multiplication operator) |
| `&` | Ampersand | Refers to the address of a variable (also used as bitwise AND) |
| `:` | Colon | Used in labels (with `goto`) and in the ternary operator (`? :`) |
| `\` | Backslash | Used to form escape sequences (explained below) |

---

### Example Showing Special Symbols in Use
```c
#include <stdio.h>

struct Student {
    char name[20];
    int age;
};

int main() {
    struct Student s1 = {"Meenakshi", 20};
    struct Student *ptr = &s1;

    printf("%s is %d years old\n", ptr->name, s1.age);
    return 0;
}
```
Here: `#` starts a preprocessor directive, `{ }` marks blocks, `;` ends statements, `.` accesses a member directly, `->` accesses a member through a pointer, and `&` gets the address of `s1`.

---

### Is Carriage Return the Same as Escape/Backslash Characters?

Not exactly — they're related, but they answer different questions:

- **Escape sequences** are a *general concept*: a backslash `\` followed by a character, used to represent something that can't be typed normally inside a string or character constant (like a new line, a tab, or a quote symbol itself).
- **Carriage return (`\r`)** is just **one specific escape sequence** among many — it's not a separate thing from escape sequences, it's a *member* of that group.

**Common escape sequences in C:**

| Escape Sequence | Meaning |
|---|---|
| `\n` | New line (moves cursor to the start of the next line) |
| `\r` | Carriage return (moves cursor to the start of the **same** line, without moving down) |
| `\t` | Horizontal tab |
| `\\` | Backslash itself |
| `\'` | Single quote |
| `\"` | Double quote |
| `\0` | Null character (marks the end of a string) |
| `\a` | Alert/bell sound |
| `\b` | Backspace |

**Difference between `\n` and `\r` specifically:**
- `\n` moves the cursor **down to a new line**.
- `\r` moves the cursor **back to the beginning of the current line**, without going down — so anything printed after `\r` overwrites what's already on that line.

```c
printf("Hello\rWorld\n");
```
**Output:** `World` (because `\r` sends the cursor back to the start, and `World` overwrites `Hello`)

So: **carriage return is a type of escape sequence**, not a separate category — and escape sequences themselves are formed using the backslash special symbol, which is why backslash appears in the Special Symbols list above.

---

⬅️ [Previous: 05. Strings](#) | [Next: 07. Operators](#) ➡️
