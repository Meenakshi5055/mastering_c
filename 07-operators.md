## 07: Operators — Index

**What is an Operator?**
An operator is a **special symbol that tells the compiler to perform a specific operation** on one or more values (called operands). Operators are what let you actually *do* something with your data — add numbers, compare values, assign results, and more.

```c
int sum = a + b;
```
Here, `+` is an operator — it tells the compiler to add the values of `a` and `b`.

---

### Types of Operators in C

C provides several categories of operators, each meant for a different kind of task:

1. **[Arithmetic Operators](/arithmetic-operators.md)** — perform basic math (`+`, `-`, `*`, `/`, `%`)
2. **[Relational Operators](/relational-operators.md)** — compare two values (`==`, `!=`, `>`, `<`, `>=`, `<=`)
3. **[Logical Operators](/logical-operators.md)** — combine or invert true/false conditions (`&&`, `||`, `!`)
4. **[Assignment Operators](/assignment-operators.md)** — assign or update a value in a variable (`=`, `+=`, `-=`, etc.)
5. **[Increment & Decrement Operators](/increment-decrement-operators.md)** — increase or decrease a value by 1 (`++`, `--`)
6. **[Bitwise Operators](/bitwise-operators.md)** — work directly on the binary bits of a value (`&`, `|`, `^`, `~`, `<<`, `>>`)
7. **[Conditional (Ternary) Operator](/conditional-(ternary)-operator.md)** — a shorthand for a simple if-else (`? :`)
8. **[Special Operators](/special-operators.md)** — `sizeof`, comma `,`, and pointer operators (`&`, `*`)

---

### General Rules for Operators

1. Every operator needs the correct number of **operands** — most need two (like `a + b`), some need only one (like `-a` or `!a`), and one needs three (`? :`).
2. Operators follow a strict **order of execution**, called **precedence** — for example, `*` and `/` are evaluated before `+` and `-`.
3. When operators of the same precedence appear together, **associativity** decides the order (left-to-right or right-to-left).
4. Some symbols act as **different operators depending on context** — e.g., `*` means multiplication between two numbers, but means "pointer" when placed before a variable declaration.
5. Parentheses `()` can always be used to force a specific order of evaluation, overriding default precedence.

---

### Where Operators Are Used
Operators appear almost everywhere in a C program — inside conditions (`if`, `while`), inside calculations, while comparing values, while updating variables in loops, and while working with memory addresses through pointers. Understanding each type well is essential before moving into Control Statements (Module 04), since conditions there are built entirely using operators.

---

Ready when you are — tell me which operator type to start with.
