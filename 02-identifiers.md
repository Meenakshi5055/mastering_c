## 02: Identifiers

**What is an Identifier?**
An identifier is the **name you give** to things in your program — like variables, functions, arrays, and other user-defined items. It's how you refer to a piece of data or a block of code later in your program.

```c
int marks = 90;
```
Here, `marks` is an identifier — the name given to that piece of data.

---

### Rules for Naming an Identifier

1. Can only contain **letters (A-Z, a-z)**, **digits (0-9)**, and the **underscore (_)**.
2. Must **start with a letter or an underscore** — never with a digit.
3. **No spaces or special symbols** are allowed (like `@`, `-`, `%`, `#`).
4. **Cannot be a keyword** (reserved words like `int`, `if`, `while` cannot be used as identifiers).
5. Identifiers are **case-sensitive** — `total`, `Total`, and `TOTAL` are treated as three different identifiers.
6. No fixed limit on length in modern C, but only the first **31 characters** are guaranteed to be recognized as unique by the compiler — so very long names should still stay meaningful within that range.

---

### Valid Identifiers
| Identifier | Why it's valid |
|---|---|
| `age` | Starts with a letter |
| `_count` | Starts with an underscore |
| `total_marks` | Underscore used correctly between words |
| `num1` | Digit allowed, but not at the start |
| `studentName` | Letters only, mixed case allowed |

### Invalid Identifiers
| Identifier | Why it's invalid |
|---|---|
| `1number` | Starts with a digit |
| `total-marks` | Hyphen (`-`) is not allowed |
| `int` | `int` is a reserved keyword |
| `first name` | Contains a space |
| `salary%` | Contains a special symbol (`%`) |

---

### Good Practice (Not a Rule, but Recommended)
While C allows short or unclear names, it's good practice to choose identifiers that describe what they store — for example, `studentAge` is clearer than `x`. This makes code easier to read later, both for you and for anyone else viewing your repo.

---

[⬅️ Previous: 01. Introduction to tokens](/01-tokens-intro.md) | [➡️ Next: 03. Keywords](/03-keywords.md) 
