# 🧮 07: Operators in C

![Language](https://img.shields.io/badge/Language-C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Level](https://img.shields.io/badge/Level-Beginner-2ea44f?style=for-the-badge)
![Topic](https://img.shields.io/badge/Topic-Operators-7B61FF?style=for-the-badge)
![Hands-on](https://img.shields.io/badge/Learning-Hands--on-2ea44f?style=for-the-badge)

> 🧭 **Lesson goal:** Learn how operators help C programs calculate, compare, decide, and update values.

## 🎁 What you will gain

By the end of this lesson, you will be able to:

- ✅ Explain what an operator and an operand are.
- ✅ Choose the right operator for a calculation or condition.
- ✅ Read expressions using arithmetic, relational, and logical operators.
- ✅ Update variables with assignment, increment, and decrement operators.
- ✅ Understand precedence and use parentheses to make expressions clear.
- ✅ Recognize how operators can work with bits, pointers, and conditional expressions.

---

## 💡 What is an operator?

An **operator** is a special symbol that tells the compiler to perform an operation on one or more values. The values being operated on are called **operands**.

```c
int sum = a + b;
```

In this example:

- `+` is the **operator**.
- `a` and `b` are the **operands**.
- `a + b` is an **expression** that produces a value.

> 🌱 **Simple idea:** Operators are the action words of C. They tell your program to add, compare, assign, combine, or transform data.

---

## 🧩 Types of operators in C

Use the links below to explore each operator family. Each topic focuses on one practical idea, so you can learn step by step.

| # | Operator family | What it helps you do | Common symbols |
|:---:|---|---|---|
| 1 | ➕ [Arithmetic operators](./arithmetic-operators.md) | Perform calculations | `+` `-` `*` `/` `%` |
| 2 | ⚖️ [Relational operators](./relational-operators.md) | Compare values | `==` `!=` `>` `<` `>=` `<=` |
| 3 | 🧠 [Logical operators](./logical-operators.md) | Combine conditions | `&&` `||` `!` |
| 4 | ✍️ [Assignment operators](./assignment-operators.md) | Store or update values | `=` `+=` `-=` `*=` `/=` |
| 5 | 🔁 [Increment & decrement operators](./increment-decrement-operators.md) | Change a value by one | `++` `--` |
| 6 | 🧱 [Bitwise operators](./bitwise-operators.md) | Work with individual bits | `&` `|` `^` `~` `<<` `>>` |
| 7 | ❓ [Conditional operator](./conditional-(ternary)-operator.md) | Write a compact choice | `? :` |
| 8 | 🧰 [Special operators](./special-operators.md) | Inspect size, sequence, and memory | `sizeof` `,` `&` `*` |

> 🎯 **Recommended order:** Start with arithmetic, then learn comparisons and logic. These three groups appear frequently in `if` statements, loops, and functions.

---

## 🔍 Operators in a real expression

```c
#include <stdio.h>

int main(void) {
    int age = 20;
    int minimum_age = 18;

    if (age >= minimum_age && age <  v 100) {
        printf("You can continue.\n");
    }

    return 0;
}
```

> ⚠️ The expression above contains a typo (`<  v 100`) intentionally? No—C does not understand it. The correct expression is shown below:

```c
if (age >= minimum_age && age < 100) {
    printf("You can continue.\n");
}
```

Here, `>=`, `<`, and `&&` compare or combine values, while `=` assigns values to variables.

---

## 🧭 Three important operator ideas

### 1. Operands matter

Most operators need two operands, such as `a + b`. Some need one, such as `-a` or `!ready`. The conditional operator `? :` uses three parts.

### 2. Precedence controls evaluation

Some operators are evaluated before others. For example, multiplication happens before addition:

```c
int result = 2 + 3 * 4;       // 14
int clear_result = (2 + 3) * 4; // 20
```

### 3. Parentheses improve clarity

Even when you know the precedence rules, parentheses make your intention easier to read and reduce mistakes:

```c
if ((score >= 50) && (attempts < 3)) {
    printf("Passed\n");
}
```

> ✨ **Readability tip:** Prefer a clear expression over a clever expression. Code is written once but read many times.

---

## 🧠 Quick challenge

What will this program print?

```c
#include <stdio.h>

int main(void) {
    int a = 10;
    int b = 3;

    printf("%d\n", a + b * 2);
    printf("%d\n", (a + b) * 2);

    return 0;
}
```

<details>
<summary>💬 Show the answer</summary>

It prints:

```text
16
26
```

The first expression multiplies `b` before adding `a`. The parentheses in the second expression force the addition to happen first.

</details>

---

## ✅ Key takeaways

- Operators perform actions on operands.
- Arithmetic operators calculate values.
- Relational operators compare values.
- Logical operators combine conditions.
- Assignment operators store or update values.
- Precedence and associativity affect evaluation order.
- Parentheses make expressions safer and easier to understand.

> 🚀 **Ready to practice?** Begin with [Arithmetic Operators](./arithmetic-operators.md) and turn simple values into useful calculations.

---

<div align="left">
  ⬅️ <a href="./06-special-symbols.md">Previous: 06. Special Symbols</a>
</div>

<br>

<div align="right">
  <a href="./arithmetic-operators.md">Next: Arithmetic Operators</a> ➡️
</div>
