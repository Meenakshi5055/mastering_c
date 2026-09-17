## 03: Keywords

**What is a Keyword?**
A keyword is a **word that already has a fixed, special meaning** in the C language. Because the compiler reserves these words for specific purposes, they cannot be used as identifiers (names for variables, functions, etc.).

```c
int age = 20;
```
Here, `int` is a keyword — it tells the compiler "this is going to store a whole number." You can't rename `int` to mean something else.

---

### Rules for Keywords

1. C has exactly **32 keywords** (as defined in the ANSI C / C89 standard).
2. All keywords are written in **lowercase** only.
3. They **cannot be used as identifiers** — you cannot name a variable `int` or `for`.
4. Each keyword has a **fixed purpose** that cannot be changed by the programmer.

---

### The 32 Keywords in C

| # | Keyword | # | Keyword |
|---|---|---|---|
| 1 | `auto` | 17 | `int` |
| 2 | `break` | 18 | `long` |
| 3 | `case` | 19 | `register` |
| 4 | `char` | 20 | `return` |
| 5 | `const` | 21 | `short` |
| 6 | `continue` | 22 | `signed` |
| 7 | `default` | 23 | `sizeof` |
| 8 | `do` | 24 | `static` |
| 9 | `double` | 25 | `struct` |
| 10 | `else` | 26 | `switch` |
| 11 | `enum` | 27 | `typedef` |
| 12 | `extern` | 28 | `union` |
| 13 | `float` | 29 | `unsigned` |
| 14 | `for` | 30 | `void` |
| 15 | `goto` | 31 | `volatile` |
| 16 | `if` | 32 | `while` |

---

### Keywords Grouped by Purpose (for easier understanding)

**Data Types** — define what kind of value is stored:
`int`, `char`, `float`, `double`, `void`, `short`, `long`, `signed`, `unsigned`

**Control Flow** — decision-making and loops:
`if`, `else`, `switch`, `case`, `default`, `for`, `while`, `do`, `break`, `continue`, `goto`

**Storage Classes** — control how/where a variable is stored:
`auto`, `register`, `static`, `extern`

**Structures & User-Defined Types** — group data together:
`struct`, `union`, `enum`, `typedef`

**Functions & Values** — related to functions and return behavior:
`return`, `sizeof`

**Type Qualifiers** — modify how a variable behaves:
`const`, `volatile`

---

### Example Showing Multiple Keywords Together
```c
const int MAX = 100;

int main() {
    static int count = 0;
    for (int i = 0; i < MAX; i++) {
        if (i == 5)
            break;
    }
    return 0;
}
```
Here, `const`, `int`, `static`, `for`, `if`, `break`, and `return` are all keywords — each doing a specific, fixed job that the compiler already understands.

---

⬅️ [Previous: 02. Identifiers](#) | [Next: 04. Constants](#) ➡️
