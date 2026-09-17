# 🧮 07: Operators in C — Learning Index

![Language](https://img.shields.io/badge/Language-C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Level](https://img.shields.io/badge/Level-Beginner-2ea44f?style=for-the-badge)
![Topic](https://img.shields.io/badge/Topic-Operators-7B61FF?style=for-the-badge)
![Learning](https://img.shields.io/badge/Learning-Step--by--step-2ea44f?style=for-the-badge)

> 🧭 **Lesson goal:** Understand how operators help C programs calculate, compare, decide, update values, and work with memory.

## 🎁 What you will gain

By the end of this operator series, you will be able to:

- ✅ Explain the difference between an operator, an operand, and an expression.
- ✅ Identify unary, binary, and ternary operators.
- ✅ Choose the right operator for calculations and comparisons.
- ✅ Combine conditions using logical operators.
- ✅ Update variables efficiently with assignment and increment/decrement operators.
- ✅ Understand bitwise and shift operations at a beginner-friendly level.
- ✅ Use parentheses to make precedence and evaluation order clear.

---

## 💡 What are operators?

An **operator** is a special symbol or keyword that tells the compiler to perform an operation on one or more values. The values acted on are called **operands**.

```c
int sum = a + b;
```

In this example:

- `+` is the **operator**.
- `a` and `b` are the **operands**.
- `a + b` is an **expression** that produces a value.

> 🌱 **Simple idea:** Operators are the action words of C. They tell your program to add, compare, assign, combine, shift, or transform data.

---

## 🗺️ Operators learning path

Follow the topics in order. First learn how many operands an operator needs, then explore each operator family.

### 1. 🧩 [Operand Arity: Unary, Binary & Ternary](./operand-arity.md)

Learn how operators are grouped by the number of operands they use:

- **Unary:** works with one operand, such as `-x`, `!ready`, or `x++`.
- **Binary:** works with two operands, such as `a + b` or `a == b`.
- **Ternary:** works with three parts, such as `age >= 18 ? "Adult" : "Minor"`.

> 📌 **Why this comes first:** Arity is a general concept that applies to every operator family below.

---

### 2. ➕ [Arithmetic Operators](./arithmetic-operators.md)

Perform mathematical calculations with values.

**Symbols:** `+` `-` `*` `/` `%`

---

### 3. ⚖️ [Relational Operators](./relational-operators.md)

Compare two values and produce a true or false result.

**Symbols:** `==` `!=` `>` `<` `>=` `<=`

---

### 4. 🧠 [Logical Operators](./logical-operators.md)

Combine conditions or reverse a condition’s result.

**Symbols:** `&&` `||` `!`

---

### 5. ✍️ [Assignment Operators](./assignment-operators.md)

Store a value in a variable or update its current value.

**Symbols:** `=` `+=` `-=` `*=` `/=` `%=`

---

### 6. 🔁 [Increment & Decrement Operators](./increment-decrement-operators.md)

Increase or decrease a value by one.

**Symbols:** `++` `--`

> 🔎 You will also learn the difference between **prefix** (`++x`) and **postfix** (`x++`) forms.

---

### 7. 🧱 [Bitwise Operators](./bitwise-operators.md)

Work directly with the individual binary bits of an integer value.

**Symbols:** `&` `|` `^` `~`

#### ↔️ [Subtopic: Shift Operators](./shift-operators.md)

Shift the bits of a value to the left or right.

**Symbols:** `<<` `>>`

> 💡 Shift operators are technically bitwise operators, but they are listed separately because they are commonly taught and practiced as their own concept.

---

### 8. ❓ [Conditional (Ternary) Operator](./conditional-(ternary)-operator.md)

Choose one of two values using a compact expression instead of a simple `if...else` statement.

**Symbols:** `? :`

---

### 9. 🧰 [Special Operators](./special-operators.md)

Explore useful operators and operator-like syntax for size, sequencing, and memory access.

**Includes:**

- `sizeof` — find the size of a type or object.
- `,` — evaluate expressions in sequence.
- `&` — get an object’s address.
- `*` — declare a pointer or dereference a pointer.

> ⚠️ Some symbols, such as `&` and `*`, have different meanings depending on context. Always read the surrounding expression carefully.

---

## 🧭 Quick concept check

Before opening the next page, identify the arity of each operator:

```c
int total = a + b;                 // binary
int negative = -total;             // unary
int label = score >= 50 ? 1 : 0;   // ternary
```

<details>
<summary>💬 Show the answer</summary>

- `+` is **binary** because it uses `a` and `b`.
- `-` is **unary** because it acts on `total`.
- `? :` is **ternary** because it uses a condition and two possible results.

</details>

---

## 🧠 Remember

- Operators perform actions on operands.
- **Arity** tells you how many operands an operator needs.
- Precedence and associativity affect evaluation order.
- Parentheses can make an expression easier to read and can force the order you want.
- The same symbol can have different meanings in different contexts.

> 🚀 **Start here:** [Operand Arity: Unary, Binary & Ternary](./operand-arity.md)  
> Then continue through each operator family one concept at a time.

---

<div align="left">
  ⬅️ <a href="./06-special-symbols.md">Previous: 06. Special Symbols</a>
</div>

<br>

<div align="right">
  <a href="./operand-arity.md">Next: Operand Arity</a> ➡️
</div>
