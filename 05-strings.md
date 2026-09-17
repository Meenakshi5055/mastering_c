## 05: Strings

**What is a String (as a Token)?**
A string is a **sequence of characters enclosed in double quotes**. It's one of the 6 token types in C, separate from Constants — even though a string might look similar to a character constant at first glance.

```c
char city[] = "Delhi";
```
Here, `"Delhi"` is a string — 5 visible characters, `D`, `e`, `l`, `h`, `i`.

---

### How a String is Stored

This is the most important thing to understand about strings in C: **every string automatically ends with a hidden null character `\0`**, even though you never type it yourself.

So `"Delhi"` is not just 5 characters — it's actually stored as **6 characters** in memory:

| Index | 0 | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|---|
| Character | `D` | `e` | `l` | `h` | `i` | `\0` |

The `\0` (null character) tells the compiler "the string ends here." Without it, the computer wouldn't know where the string stops in memory.

---

### String vs Single Character (Quick Comparison)

| | Single Character Constant | String |
|---|---|---|
| Quotes used | Single quotes `' '` | Double quotes `" "` |
| Example | `'A'` | `"A"` |
| What it stores | Just one character | The character **plus** a hidden `\0` at the end |
| Memory used | 1 byte | 2 bytes (even for one letter!) |

This is why `'A'` and `"A"` are **not the same thing** in C, even though they look similar.

---

### Declaring a String

A string in C is stored as an **array of characters** (arrays are covered fully in Module 08, but you need a basic array to hold a string):

```c
char name[20] = "Meenakshi";
```
Here, `name` is a character array with room for 20 characters, and it's initialized with the string `"Meenakshi"` (plus its hidden `\0`).

---

### Rules for Strings

1. A string must be enclosed in **double quotes** `" "`.
2. C automatically adds a **null character `\0`** at the end of every string — you should not type this yourself.
3. When declaring a character array to hold a string, always leave **enough space for the `\0`** in addition to the visible characters (e.g., a 9-letter word needs an array size of at least 10).
4. A string can contain letters, digits, spaces, and special symbols — anything inside the double quotes.
5. An empty string `""` is still valid — it contains just the null character `\0` and nothing else.

---

### Example
```c
#include <stdio.h>

int main() {
    char greeting[] = "Hello";
    printf("%s\n", greeting);
    return 0;
}
```
**Output:**
```
Hello
```
The `%s` format specifier in `printf` tells C to print characters one by one **until it reaches the `\0`**, which is exactly why the null character matters so much.

---

⬅️ [Previous: 04. Constants](#) | [Next: 06. Special Symbols](#) ➡️
