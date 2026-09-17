# 🧮 Arithmetic Operators in C

![Language](https://img.shields.io/badge/Language-C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Level](https://img.shields.io/badge/Level-Beginner-2ea44f?style=for-the-badge)
![Topic](https://img.shields.io/badge/Topic-Arithmetic%20Operators-7B61FF?style=for-the-badge)
![Practice](https://img.shields.io/badge/Practice-5%20Problems-F59E0B?style=for-the-badge)

> 🎯 **Lesson goal:** Learn how to use C's arithmetic operators, understand integer and floating-point division, and evaluate expressions using precedence.

## 🌟 What you will gain

After this lesson, you will be able to:

- ✅ Use `+`, `-`, `*`, `/`, and `%` in C programs.
- ✅ Distinguish integer division from floating-point division.
- ✅ Find a quotient and remainder confidently.
- ✅ Apply operator precedence and use parentheses correctly.
- ✅ Predict the result of common arithmetic expressions.
- ✅ Understand how C handles negative remainders.
- 🛠️ Build a foundation for calculations in real programs such as bill calculators, score systems, and unit converters.

---

## 🧠 What are arithmetic operators?

Arithmetic operators perform **mathematical calculations** on numeric values—the same operations you use in everyday mathematics, expressed in C.

> 💡 **Simple idea:** Values go in, an operator performs a calculation, and an expression produces a result.

```c
int total = price + tax;
```

Here, `+` is the operator, while `price` and `tax` are its operands.

---

## ➕ The five essential arithmetic operators

| Operator | Meaning | Example | Result when `a = 10`, `b = 3` |
|:---:|---|---:|---:|
| `+` | Addition | `a + b` | `13` |
| `-` | Subtraction | `a - b` | `7` |
| `*` | Multiplication | `a * b` | `30` |
| `/` | Division | `a / b` | `3` |
| `%` | Modulus (remainder) | `a % b` | `1` |

All five are **binary operators**: each one works with exactly two operands.

---

## 🔍 Rules you should remember

### 1️⃣ Integer division drops the decimal

When both operands are integers, `/` returns only the whole-number part:

```c
10 / 3   // 3, not 3.333333
```

> ⚠️ C does not round the answer here—it truncates the fractional part.

### 2️⃣ Use a floating-point operand for decimals

If at least one operand is a `float` or `double`, C performs floating-point division:

```c
10.0 / 3   // 3.333333...
```

### 3️⃣ Modulus returns the remainder

The `%` operator gives the remainder after integer division:

```c
10 % 3    // 1
```

> 🚫 `%` works with integer types, not with `float` or `double` values.

### 4️⃣ Follow operator precedence

C evaluates `*`, `/`, and `%` before `+` and `-`. Operators at the same level are evaluated from left to right.

```c
10 + 5 * 2 - 3 / 3
// 10 + 10 - 1
// 19
```

Use parentheses when you want to make the order obvious:

```c
(10 + 5) * 2   // 30
10 + (5 * 2)   // 20
```

### 5️⃣ Negative remainders keep the dividend's sign

In C, the remainder has the sign of the first operand:

```c
-10 % 3   // -1
```

> 🛑 **Safety reminder:** Never divide by zero. Expressions such as `10 / 0` and `10 % 0` are invalid and can cause undefined behavior.

---

## 💻 Example program

```c
#include <stdio.h>

int main(void) {
    int a = 10;
    int b = 3;

    printf("Sum: %d\n", a + b);
    printf("Difference: %d\n", a - b);
    printf("Product: %d\n", a * b);
    printf("Quotient: %d\n", a / b);
    printf("Remainder: %d\n", a % b);

    return 0;
}
```

### ✅ Output

```text
Sum: 13
Difference: 7
Product: 30
Quotient: 3
Remainder: 1
```

> 🧪 **Try it yourself:** Change `a` and `b`, compile the program, and predict the output before running it.

---

## 🎮 Practice: predict before you reveal

### Problem 1️⃣

What is the output of `printf("%d", 7 / 2);`?

<details>
<summary>💬 Show solution</summary>

**Output:** `3`

Both operands are integers, so C performs integer division and drops `.5`.

</details>

---

### Problem 2️⃣

What is the output of `printf("%d", 7 % 2);`?

<details>
<summary>💬 Show solution</summary>

**Output:** `1`

`7 / 2` has quotient `3` and remainder `1`.

</details>

---

### Problem 3️⃣

What is the output of `printf("%f", 7.0 / 2);`?

<details>
<summary>💬 Show solution</summary>

**Output:** `3.500000`

`7.0` is a floating-point value, so the division keeps the decimal part. In `printf`, `%f` displays a `double` value.

</details>

---

### Problem 4️⃣

What is the output of `printf("%d", -7 % 2);`?

<details>
<summary>💬 Show solution</summary>

**Output:** `-1`

The remainder takes the sign of the first operand, `-7`.

</details>

---

### Problem 5️⃣

Evaluate `10 + 5 * 2 - 3 / 3`.

<details>
<summary>💬 Show solution</summary>

**Output:** `19`

1. `5 * 2 = 10`
2. `3 / 3 = 1`
3. `10 + 10 - 1 = 19`

</details>

---

## 📌 One-minute recap

| Concept | Remember |
|---|---|
| `+`, `-`, `*` | Basic arithmetic calculations |
| `/` with integers | Produces an integer quotient |
| `/` with a float/double | Keeps the fractional part |
| `%` | Returns the integer remainder |
| Precedence | `*`, `/`, `%` before `+`, `-` |
| Zero division | Always avoid it |

> 🌱 **Key takeaway:** Arithmetic in C is easy when you know the operand types, the remainder rule, and the order of evaluation.

---

<div align="left">
  ⬅️ <a href="./operand-arity.md">Previous: Operand Arity</a>
</div>

<br>

<div align="right">
  <a href="./07-operators.md">Next: Operators Overview</a> ➡️
</div>
