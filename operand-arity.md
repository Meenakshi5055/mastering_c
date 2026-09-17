# 🧩 Operand Arity in C

![Language](https://img.shields.io/badge/Language-C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Level](https://img.shields.io/badge/Level-Beginner-2ea44f?style=for-the-badge)
![Topic](https://img.shields.io/badge/Topic-Operators-7B61FF?style=for-the-badge)
![Lesson](https://img.shields.io/badge/Lesson-Operand%20Arity-F59E0B?style=for-the-badge)

> 🎯 **Lesson goal:** Learn how to identify an operator by the number of operands it uses.

## 🌟 What you will gain

After this lesson, you will be able to:

- ✅ Explain the difference between an **operator**, an **operand**, and an **expression**.
- ✅ Identify **unary**, **binary**, and **ternary** operators.
- ✅ Count the operands used in a C expression.
- ✅ Understand why the same symbol can be unary in one expression and binary in another.
- ✅ Read later operator lessons with more confidence.

---

## 🧠 First, understand the vocabulary

### What is an operand?

An **operand** is the value, variable, or expression that an operator works on.

```c
int total = price + tax;
```

- `+` is the **operator** — it performs addition.
- `price` and `tax` are the **operands** — the values being added.
- `price + tax` is an **expression** — it produces a result.

### What is arity?

**Arity** means the number of operands an operator needs.

> 💡 **Easy memory trick:**
> - **Unary** → **uni** = one operand
> - **Binary** → **bi** = two operands
> - **Ternary** → **three** operands

---

## 🗺️ The three kinds of operator arity

| Arity | Operands | Visual pattern | Example |
|:---:|:---:|:---|:---|
| 🟢 **Unary** | 1 | `operator value` | `-a` |
| 🔵 **Binary** | 2 | `value operator value` | `a + b` |
| 🟣 **Ternary** | 3 | `condition ? true : false` | `a > b ? a : b` |

---

## 1️⃣ Unary operators — one operand

A **unary operator** works with only one operand. It usually appears before its operand, although increment and decrement can appear before or after it.

| Operator | Meaning | Example |
|---|---|---|
| `-` | Unary minus; changes the sign | `-a` |
| `+` | Unary plus; keeps the sign | `+a` |
| `!` | Logical NOT; reverses true/false | `!ready` |
| `++` | Increases a value by one | `++count` or `count++` |
| `--` | Decreases a value by one | `--count` or `count--` |
| `&` | Address-of; obtains an address | `&number` |
| `*` | Dereference; accesses a pointed-to value | `*ptr` |
| `sizeof` | Finds the size of a type or object | `sizeof(number)` |

```c
#include <stdio.h>

int main(void) {
    int a = 5;
    int negative = -a;       // unary -, operand: a
    int is_zero = !0;        // unary !, operand: 0

    printf("%d %d\n", negative, is_zero);
    return 0;
}
```

> ⚠️ **Watch the context:** `-` is unary in `-a`, but binary in `a - b`. Likewise, `*` is unary in `*ptr`, but binary in `a * b`.

---

## 2️⃣ Binary operators — two operands

A **binary operator** works with two operands: one on each side. This is the largest operator group in C.

| Category | Examples |
|---|---|
| Arithmetic | `a + b`, `a - b`, `a * b`, `a / b`, `a % b` |
| Relational | `a > b`, `a == b`, `a != b` |
| Logical | `a && b`, `a || b` |
| Assignment | `a = b`, `a += b`, `a -= b` |
| Bitwise | `a & b`, `a \| b`, `a ^ b` |
| Shift | `a << b`, `a >> b` |

```c
int a = 10;
int b = 3;
int sum = a + b;       // binary +, operands: a and b
int is_larger = a > b; // binary >, operands: a and b
```

> 🔍 **Reading tip:** For `a + b`, start at the operator and look left and right. The two values it connects are its operands.

---

## 3️⃣ Ternary operator — three operands

C has one ternary operator: the **conditional operator** `? :`.

```c
int max = (a > b) ? a : b;
```

This expression has three parts:

1. `a > b` — the **condition**
2. `a` — the value used when the condition is true
3. `b` — the value used when the condition is false

In plain English:

> 🗣️ “If `a` is greater than `b`, choose `a`; otherwise, choose `b`.”

The ternary operator is useful for short, simple choices. For longer decisions, a normal `if...else` statement is usually easier to read.

---

## 🎮 Quick practice: identify the arity

Try to identify the arity before opening the answer.

```c
int result = -score;
int total = price + tax;
int status = age >= 18 ? 1 : 0;
```

<details>
<summary>💬 Show the answer</summary>

- `-score` → 🟢 **Unary**: `-` uses one operand, `score`.
- `price + tax` → 🔵 **Binary**: `+` uses two operands, `price` and `tax`.
- `age >= 18 ? 1 : 0` → 🟣 **Ternary**: the conditional operator chooses between `1` and `0` using a condition.

</details>

---

## 🚀 Why does arity matter?

Knowing arity helps you:

- 📖 Read unfamiliar C expressions more quickly.
- 🧩 Understand what an operator is acting on.
- 🐞 Spot misplaced or missing operands while debugging.
- 🧠 Distinguish symbols that change meaning based on context.
- 🛠️ Build a strong foundation for arithmetic, logical, pointer, and conditional operators.

> ✅ **Remember:** Arity tells you **how many operands an operator uses**. It does not tell you the operator's precedence or the order in which an expression is evaluated.

---

## 📌 One-minute recap

| Type | Number of operands | Example |
|:---:|:---:|:---|
| 🟢 Unary | 1 | `!ready` |
| 🔵 Binary | 2 | `a + b` |
| 🟣 Ternary | 3 | `a ? b : c` |

> 🌱 **Key takeaway:** Before asking “What does this operator do?”, ask “How many operands does it use?”

---

<div align="left">
  ⬅️ <a href="./07-operators.md">Previous: 07. Operators Index</a>
</div>

<br>

<div align="right">
  <a href="./arithmetic-operators.md">Next: Arithmetic Operators</a> ➡️
</div>
