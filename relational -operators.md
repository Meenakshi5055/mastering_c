<div align="center">

# 🔎 Relational Operators in C

### Compare values • Make decisions • Write smarter conditions

![C Language](https://img.shields.io/badge/Language-C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Level](https://img.shields.io/badge/Level-Beginner-success?style=for-the-badge)
![Topic](https://img.shields.io/badge/Topic-Operators-orange?style=for-the-badge)

</div>

> 💡 **Quick idea:** Relational operators ask a question such as “Is `a` greater than `b`?” C answers with `1` for true or `0` for false.

---

## 🎯 What You Will Gain

By the end of this module, you will be able to:

- ✅ Compare numbers and characters correctly.
- ✅ Choose between `==`, `!=`, `<`, `>`, `<=`, and `>=`.
- ✅ Use comparisons in `if`, `while`, and `for` conditions.
- ✅ Understand the difference between assignment (`=`) and comparison (`==`).
- ✅ Predict comparison results and avoid common beginner mistakes.
- ✅ Handle boundary values like “at least” and “at most”.

---

## 🤔 What Are Relational Operators?

Relational operators compare two values. The expression produces an `int` result:

- `1` means **true** ✅
- `0` means **false** ❌

C does not print the words `true` and `false` by default. If you want to use those words explicitly, include `<stdbool.h>`.

---

## 🧰 The Six Relational Operators

| Operator | Meaning | Example | Result when `a = 10`, `b = 20` |
|:---:|---|---|:---:|
| `==` | Equal to | `a == b` | `0` ❌ |
| `!=` | Not equal to | `a != b` | `1` ✅ |
| `>` | Greater than | `a > b` | `0` ❌ |
| `<` | Less than | `a < b` | `1` ✅ |
| `>=` | Greater than or equal to | `a >= b` | `0` ❌ |
| `<=` | Less than or equal to | `a <= b` | `1` ✅ |

These are **binary operators** because they work with two operands.

### 🧠 Easy way to remember the symbols

The open side of `<` or `>` faces the larger value:

```text
3 < 8       → 3 is less than 8
8 > 3       → 8 is greater than 3
```

The `=` added to `<` or `>` means “or equal to”:

```text
x >= 18     → x is 18 or more
x <= 18     → x is 18 or less
```

---

## 💻 Basic Example

```c
#include <stdio.h>

int main(void) {
    int a = 10;
    int b = 20;

    printf("a == b: %d\n", a == b);
    printf("a != b: %d\n", a != b);
    printf("a > b:  %d\n", a > b);
    printf("a < b:  %d\n", a < b);

    return 0;
}
```

### Output

```text
a == b: 0
a != b: 1
a > b:  0
a < b:  1
```

---

## 🚦 Using Comparisons in Conditions

Relational expressions are most useful inside decision-making statements:

```c
#include <stdio.h>

int main(void) {
    int age = 20;

    if (age >= 18) {
        printf("You are eligible to vote.\n");
    } else {
        printf("You are not eligible to vote yet.\n");
    }

    return 0;
}
```

`age >= 18` is true because `age` is `20`, so the `if` block executes.

---

## ⚠️ Important Rules and Common Mistakes

### 1. Do not confuse `=` with `==`

- `=` assigns a value.
- `==` compares two values.

```c
int num = 10;

if (num = 5) {       // Wrong when you meant to compare
    printf("This runs!\n");
}
```

The assignment changes `num` to `5`. The assignment expression has the value `5`, which is non-zero, so C treats it as true. Use `if (num == 5)` when you want to compare.

> 🛠️ Compile with warnings enabled: `gcc -Wall -Wextra program.c` will help reveal this mistake.

### 2. `==` does not compare strings

This is not a reliable way to compare text:

```c
if (name == "Alice") { /* incorrect for string contents */ }
```

Use `strcmp()` from `<string.h>` instead:

```c
if (strcmp(name, "Alice") == 0) {
    printf("Names match.\n");
}
```

### 3. Do not chain comparisons like mathematics

This does **not** mean “`0 < x` and `x < 10`” in C:

```c
if (0 < x < 10) { /* misleading */ }
```

C evaluates it from left to right. Write both comparisons explicitly:

```c
if (0 < x && x < 10) {
    printf("x is between 0 and 10.\n");
}
```

### 4. Be careful when comparing floating-point values

Calculations with `float` or `double` can contain tiny rounding errors. Prefer a tolerance when checking calculated values:

```c
#include <math.h>

if (fabs(result - expected) < 0.000001) {
    printf("Values are close enough.\n");
}
```

### 5. Characters are compared by their numeric character codes

```c
'A' < 'a'   // usually true: 'A' is 65 and 'a' is 97 in ASCII
```

For alphabetical comparisons, remember that uppercase and lowercase letters have different ASCII values.

### 6. Parentheses make conditions easier to read

Even when operator precedence makes an expression valid, parentheses communicate your intention:

```c
if ((marks >= 40) && (attendance >= 75)) {
    printf("Eligible.\n");
}
```

---

## 🧪 Practice Problems

Try to answer each question before opening its solution. ✍️

### Problem 1 — Equal values

What is the output?

```c
printf("%d", 5 == 5);
```

<details>
<summary>💡 Show solution</summary>

Output: `1` — both values are equal.

</details>

---

### Problem 2 — Character comparison

What is the output?

```c
printf("%d", 'A' > 'a');
```

<details>
<summary>💡 Show solution</summary>

Output: `0`. In ASCII, `'A'` is `65` and `'a'` is `97`, so `65 > 97` is false.

</details>

---

### Problem 3 — Boundary values

If `int x = 15;`, what do these expressions produce?

```c
x != 10
x <= 15
x < 15
```

<details>
<summary>💡 Show solution</summary>

- `x != 10` → `1`
- `x <= 15` → `1` because equality is included
- `x < 15` → `0` because `x` is equal to 15, not less than it

</details>

---

### Problem 4 — `if` and `else`

What does this program print?

```c
int age = 18;

if (age >= 18) {
    printf("Eligible to vote\n");
} else {
    printf("Not eligible to vote\n");
}
```

<details>
<summary>💡 Show solution</summary>

`Eligible to vote` — `18 >= 18` is true because `>=` includes equality.

</details>

---

### Problem 5 — Assignment mistake

What is wrong with this condition?

```c
int num = 10;
if (num = 5) {
    printf("Number is 5\n");
}
```

<details>
<summary>💡 Show solution</summary>

`num = 5` assigns `5` to `num`; it does not compare. The non-zero value `5` is treated as true, so the message prints. Use `num == 5` for comparison.

</details>

---

### Problem 6 — `>` versus `>=`

What will this print?

```c
int score = 50;

if (score > 50) {
    printf("Above passing score\n");
} else if (score >= 50) {
    printf("Passed exactly at the limit\n");
} else {
    printf("Failed\n");
}
```

<details>
<summary>💡 Show solution</summary>

`Passed exactly at the limit` — `score > 50` is false, but `score >= 50` is true.

</details>

---

### Problem 7 — Negative numbers

What are the results?

```c
int temperature = -3;
printf("%d\n", temperature < 0);
printf("%d\n", temperature >= -3);
printf("%d\n", temperature == 3);
```

<details>
<summary>💡 Show solution</summary>

```text
1
1
0
```

`-3` is below zero, equal to `-3`, and not equal to positive `3`.

</details>

---

### Problem 8 — A chained comparison trap

What does this condition really evaluate?

```c
int x = 5;
if (0 < x < 10) {
    printf("Inside if\n");
}
```

<details>
<summary>💡 Show solution</summary>

The first comparison, `0 < x`, produces `1`. Then C evaluates `1 < 10`, which is also true. This example can accidentally seem to work. For `x = -5`, it would still evaluate as `1 < 10`, so use `0 < x && x < 10` instead.

</details>

---

### Problem 9 — Comparing expression results

What is printed?

```c
int a = 4;
int b = 2;

printf("%d\n", a + b == 6);
printf("%d\n", a * b != 8);
```

<details>
<summary>💡 Show solution</summary>

```text
1
0
```

`a + b` is `6`, while `a * b` is `8`, so the second comparison is false.

</details>

---

### Problem 10 — Zero and non-zero values in `if`

What does this program print?

```c
int value = -2;

if (value) {
    printf("Non-zero\n");
} else {
    printf("Zero\n");
}
```

<details>
<summary>💡 Show solution</summary>

`Non-zero` — in a C condition, `0` is false and every non-zero integer, including negative numbers, is true. This is not a relational comparison, but it is essential for understanding conditions.

</details>

---

## ✅ Quick Revision

- `==` checks equality; `=` performs assignment.
- `<` and `>` exclude equality.
- `<=` and `>=` include equality.
- A comparison produces `1` or `0`.
- Use `strcmp()` for string contents, not `==`.
- Do not write mathematical chained comparisons in C.
- Use warnings and parentheses to make code safer and clearer.

<div align="center">

### 🎉 You can now compare values and make your C programs decide!

</div>

<div align="left">

⬅️ [Previous: Arithmetic Operators](arithmetic-operators.md)

</div>

<div align="right">

[Next: Logical Operators](logical-operators.md) ➡️

</div>
