## 04: Constants

**What is a Constant?**
A constant is a **value that does not change** during the execution of a program. Unlike a variable, once a constant's value is set, it stays fixed throughout the program.

```c
int age = 25;
```
Here, `25` is a constant — a fixed value that doesn't change while the program runs.

---

### Types of Constants in C

Constants in C are divided into two main categories: **Numeric Constants** and **Character Constants**.

```
Constants
├── Numeric Constants
│   ├── Integer Constants
│   │   ├── Decimal
│   │   ├── Octal
│   │   └── Hexadecimal
│   └── Real (Floating-Point) Constants
└── Character Constants
    ├── Single Character
    └── String
```

---

## 1. Numeric Constants

These represent numbers — either whole numbers or numbers with decimal points.

### A) Integer Constants
An integer constant is a whole number with **no decimal point**. It can be positive, negative, or zero. Integer constants come in three forms, based on the number system used:

**i) Decimal Integer Constants**
- Written in the normal base-10 number system (digits 0-9).
- Example: `25`, `-100`, `0`, `2024`

**ii) Octal Integer Constants**
- Written in base-8, using digits **0 to 7** only.
- Must begin with a **leading 0**.
- Example: `010` (equals decimal 8), `017` (equals decimal 15)

**iii) Hexadecimal Integer Constants**
- Written in base-16, using digits **0-9** and letters **A-F** (or a-f).
- Must begin with **0x** or **0X**.
- Example: `0x1A` (equals decimal 26), `0X2F` (equals decimal 47)

### B) Real (Floating-Point) Constants
A real constant is a number that **includes a decimal point** or is written in exponential (scientific) form — used to represent fractional values.
- Decimal form: `3.14`, `0.001`, `-25.5`
- Exponential form: `2.5e3` (means 2.5 × 10³ = 2500), `1.2E-4` (means 1.2 × 10⁻⁴)

---

## 2. Character Constants

These represent text — either a single character or a sequence of characters.

### A) Single Character Constant
- A **single character** enclosed in **single quotes** `' '`.
- Example: `'A'`, `'5'`, `'$'`, `'\n'` (newline is also a valid single character constant, called an escape sequence)

### B) String Constant
- A **sequence of characters** enclosed in **double quotes** `" "`.
- Example: `"Hello"`, `"C Programming"`, `"123"`
- Internally, C automatically adds a hidden `\0` (null character) at the end of every string to mark where it ends.

---

### Rules for Constants

1. A single character constant must use **single quotes**, and a string constant must use **double quotes** — they are not interchangeable.
2. Integer constants **cannot contain a decimal point or spaces**.
3. Octal constants must start with `0`, and their digits must only be **0-7**.
4. Hexadecimal constants must start with `0x` or `0X`, and can use digits **0-9** and letters **A-F/a-f**.
5. Real constants must have **at least one digit before and after the decimal point** (e.g., `0.5`, not `.5`).
6. A string constant is technically stored as an **array of characters**, ending with a null character (`\0`), even though this isn't visible when you write it.

---

### Quick Reference Table

| Type | Example | Notes |
|---|---|---|
| Decimal Integer | `100` | Normal base-10 number |
| Octal Integer | `0144` | Starts with 0, digits 0-7 |
| Hexadecimal Integer | `0x64` | Starts with 0x, digits 0-9/A-F |
| Real Constant | `3.14` | Contains a decimal point |
| Single Character | `'A'` | Enclosed in single quotes |
| String | `"Hello"` | Enclosed in double quotes |

---

⬅️ [Previous: 03. Keywords](#) | [Next: 05. Strings](#) ➡️
