# 🔑 03 · Keywords in C

[![C Language](https://img.shields.io/badge/Language-C-00599C?style=for-the-badge&logo=c&logoColor=white)](https://en.wikipedia.org/wiki/C_(programming_language))
[![Level](https://img.shields.io/badge/Level-Beginner-2ea44f?style=for-the-badge)](#)
[![C89/C90](https://img.shields.io/badge/Standard-C89%2FC90-orange?style=for-the-badge)](#)

> 💡 **Quick idea:** A keyword is a reserved word with a special meaning that the C compiler already understands.

---

## 🧠 What is a keyword?

A **keyword** is a word that has a fixed meaning in the C language. The compiler reserves it for a specific purpose, so it **cannot be used as an identifier** such as a variable, function, or structure name.

```c
int age = 20;
```

Here, `int` tells the compiler that `age` stores a whole number. We cannot rename `int` or use it as a variable name.

> ✅ **Remember:** Keywords are part of C's grammar — they are not created or redefined by the programmer.

## 📌 Rules to remember

| Rule | Meaning |
|---|---|
| 🔢 **32 keywords** | C89/C90 defines 32 keywords. Later C standards add more. |
| 🔡 **Lowercase only** | `int` is a keyword, but `Int` is not. C is case-sensitive. |
| 🚫 **Reserved names** | You cannot use `for`, `int`, or `return` as identifiers. |
| 🎯 **Fixed purpose** | Each keyword has a predefined job understood by the compiler. |

## 🧾 The 32 C89/C90 keywords

| # | Keyword | # | Keyword |
|:---:|:---|:---:|:---|
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

## 🧩 Keywords by purpose

### 🧱 Data types
Define the kind of value a variable can store:

`char` · `double` · `float` · `int` · `long` · `short` · `signed` · `unsigned` · `void`

### 🔀 Control flow
Control decisions, repetition, and program execution:

`break` · `case` · `continue` · `default` · `do` · `else` · `for` · `goto` · `if` · `switch` · `while`

### 💾 Storage classes
Describe a variable's storage and lifetime:

`auto` · `extern` · `register` · `static`

### 🧰 User-defined types
Create or organize custom data types:

`enum` · `struct` · `typedef` · `union`

### 🎯 Functions and type information
Return from a function or find a type's size:

`return` · `sizeof`

### 🛡️ Type qualifiers
Modify how a value may be accessed or changed:

`const` · `volatile`

## 💻 Example: several keywords working together

```c
#include <stdio.h>

int main(void) {
    const int MAX = 5;
    static int count = 0;

    for (int i = 0; i < MAX; i++) {
        if (i == 3) {
            break;
        }
        count++;
    }

    printf("Count: %d\\n", count);
    return 0;
}
```

### 🔍 Spot the keywords

`const` sets a value that should not change · `int` declares whole numbers · `static` preserves a variable's lifetime · `for` repeats code · `if` checks a condition · `break` stops the loop · `return` sends a result back.

## ⚠️ Common mistake

```c
int for = 10;      // ❌ Error: for is a keyword
int total = 10;    // ✅ Correct: total is a valid identifier
```

> 🌟 **Tiny challenge:** Which keyword would you use to declare a value that should not be changed after initialization?  
> **Answer:** `const` ✅

---

<div align="center">

### 🎉 You now know the building blocks of C syntax!

</div>

<table width="100%">
<tr>
<td align="left">⬅️ <a href="02-identifiers.md">02 · Identifiers</a></td>
<td align="right"><a href="04-constants.md">04 · Constants</a> ➡️</td>
</tr>
</table>

<div align="center">

[⬆️ Back to top](#-03--keywords-in-c)

</div>
