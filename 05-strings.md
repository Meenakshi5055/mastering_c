# 05: Strings in C

> 💡 **Quick idea:** A C string is a sequence of characters that ends with a special character called the **null character**: `\0`.

![C](https://img.shields.io/badge/Language-C-00599C?logo=c&logoColor=white) ![Topic](https://img.shields.io/badge/Topic-Strings-7B2CBF) ![Level](https://img.shields.io/badge/Level-Beginner-2EA44F)

---

## 🎯 What You Will Learn

By the end of this module, you will understand:

- What a string is in C
- Why every string ends with `\0`
- The difference between a string, a string literal, and a variable
- How to declare and print a string
- Why `"A"` and `'A'` are different

---

## 🧠 What Is a String?

A **string** is a sequence of characters stored in a character array and terminated by a null character, `\0`.

```c
char city[] = "Delhi";
```

Here, `"Delhi"` is a **string literal**. It contains five visible characters:

```text
D  e  l  h  i
```

C automatically adds `\0` after the last character, so the complete stored string is:

```text
D  e  l  h  i  \0
```

> ⭐ **Remember:** In C, `\0` marks the end of a string. It is not the same as the character `'0'`.

---

## 📦 How a String Is Stored

`"Delhi"` needs **six character spaces**, not five:

| Index | 0 | 1 | 2 | 3 | 4 | 5 |
|---|---:|---:|---:|---:|---:|---:|
| Character | `D` | `e` | `l` | `h` | `i` | `\0` |

The null character tells functions such as `printf` where the string ends. Without it, a function may continue reading memory beyond the intended text.

---

## 🔍 String vs String Literal vs Variable

These terms are related, but they do not mean exactly the same thing:

| Term | General idea | Example |
|---|---|---|
| **String** | Characters ending with `\0` | `D e l h i \0` |
| **String literal / string constant** | Fixed text written directly in the source code | `"Hello"` |
| **Variable holding a string** | Named, writable storage where a string is kept | `char name[20]` |

### 1. String literal (string constant)

```c
"Meenakshi"
```

This is the actual text typed directly into the program, inside double quotes. It is called a **string literal** or **string constant** because it is a fixed value in the source code.

You must not try to modify a string literal:

```c
"Meenakshi"[0] = 'P'; // ❌ Do not do this
```

### 2. String: the general concept

A string is the broad idea: a sequence of characters ending in `\0`. It does not have to be written directly in the code. It may be created or changed while the program runs.

### 3. Variable holding a string

```c
char name[20] = "Meenakshi";
```

- `name` is the **identifier** of the variable.
- `char` says that the array stores characters.
- `[20]` reserves space for up to 19 visible characters plus `\0`.
- The contents of `name` can be replaced later.

```c
#include <string.h>

strcpy(name, "Priya"); // ✅ name now stores "Priya"
```

You cannot use `strcpy` to replace a literal:

```c
strcpy("Meenakshi", "Priya"); // ❌ A literal is not writable storage
```

> ✅ **Easy way to remember:** `"Meenakshi"` is the text; `name` is the box that stores the text.

---

## ✍️ Declaring a String

A string is stored in an **array of characters**:

```c
char name[20] = "Meenakshi";
```

`"Meenakshi"` has 9 visible characters, so it needs at least 10 character spaces: 9 characters plus `\0`. This declaration reserves 20 spaces, leaving room for a longer value later.

You can also let the compiler count the required spaces:

```c
char greeting[] = "Hello";
```

This creates an array with 6 elements: five letters plus `\0`.

> ⚠️ **Important:** If an array is too small, there is no room for the terminating `\0`. Always reserve enough space.

---

## 🔤 String vs Single Character

| | Single character | String |
|---|---|---|
| Quotes | Single quotes: `' '` | Double quotes: `" "` |
| Example | `'A'` | `"A"` |
| Contains | One character | One or more characters plus `\0` |
| Common format specifier | `%c` | `%s` |

```c
char letter = 'A';
char word[] = "A";
```

`'A'` and `"A"` are **not the same**:

- `'A'` is one character constant.
- `"A"` is a string literal containing `A` and `\0`.

Because a C `char` occupies one byte, the array for `"A"` needs two character elements: one for `A` and one for `\0`.

---

## ✅ Rules for Strings

1. Use **double quotes** for strings: `"Hello"`.
2. Use **single quotes** for one character: `'H'`.
3. C automatically adds `\0` to a string literal.
4. Reserve space for the visible characters **and** `\0`.
5. Strings can contain letters, digits, spaces, and symbols.
6. An empty string, `""`, contains only `\0`.
7. Use `%s` with `printf` to print a string.
8. Do not modify a string literal; copy it into a character array if you need writable storage.

---

## 💻 Complete Example

```c
#include <stdio.h>
#include <string.h>

int main(void) {
    char greeting[20] = "Hello";

    printf("Greeting: %s\n", greeting);

    strcpy(greeting, "Welcome");
    printf("After change: %s\n", greeting);

    return 0;
}
```

**Output:**

```text
Greeting: Hello
After change: Welcome
```

The `%s` format specifier prints characters one by one until it finds `\0`.

---

## 🧩 Quick Check

> What is stored in `char text[] = "Hi";`?
>
> **Answer:** `H`, `i`, and `\0` — so the array has 3 character elements.

---

<div align="left"><a href="04-constants.md">⬅️ Previous: 04. Constants</a></div>
<div align="right"><a href="06-special-symbols.md">Next: 06. Special Symbols ➡️</a></div>

---

<div align="center">🌟 Keep practising — strings become easy when you always look for the hidden <code>\0</code>! 🌟</div>
