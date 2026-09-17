## Operand Arity: Unary, Binary & Ternary

**What is an Operand?**
An operand is the **value or variable that an operator works on**. In the expression `a + b`, both `a` and `b` are operands, and `+` is the operator acting on them.

**What is Arity?**
Arity simply means **how many operands an operator needs to do its job**. Based on this, every operator in C falls into one of three groups: **Unary**, **Binary**, or **Ternary**.

---

### 1. Unary Operators
A unary operator works on **only 1 operand**.

| Operator | Meaning | Example |
|---|---|---|
| `-` | Unary minus (negates a value) | `-a` |
| `+` | Unary plus (rarely used, just states a positive value) | `+a` |
| `!` | Logical NOT (reverses true/false) | `!a` |
| `++` | Increment (increases value by 1) | `++a` or `a++` |
| `--` | Decrement (decreases value by 1) | `--a` or `a--` |
| `&` | Address-of (gets memory address) | `&a` |
| `*` | Dereference (accesses value at a pointer) | `*ptr` |
| `sizeof` | Returns the size of a data type/variable | `sizeof(a)` |

```c
int a = 5;
int b = -a;      // unary minus, 1 operand: a
printf("%d", !0); // unary NOT, 1 operand: 0
```

---

### 2. Binary Operators
A binary operator works on **2 operands** — one on each side of the operator. This is the **largest group** of operators in C.

| Category | Examples |
|---|---|
| Arithmetic | `a + b`, `a - b`, `a * b`, `a / b`, `a % b` |
| Relational | `a > b`, `a == b`, `a != b` |
| Logical | `a && b`, `a \|\| b` |
| Assignment | `a = b`, `a += b`, `a -= b` |
| Bitwise | `a & b`, `a \| b`, `a ^ b` |
| Shift | `a << b`, `a >> b` |

```c
int sum = a + b;   // binary +, 2 operands: a and b
```

---

### 3. Ternary Operator
A ternary operator works on **3 operands**. C has **only one** ternary operator: the **Conditional Operator** `? :`.

```c
int max = (a > b) ? a : b;
```
Here, there are 3 operands:
1. `a > b` (the condition)
2. `a` (result if the condition is true)
3. `b` (result if the condition is false)

This single line means: "if `a` is greater than `b`, set `max` to `a`; otherwise, set `max` to `b`."

---

### Quick Summary Table

| Type | Number of Operands | Symbol Example | Sample |
|---|---|---|---|
| Unary | 1 | `!`, `-`, `++`, `--` | `!a` |
| Binary | 2 | `+`, `>`, `&&`, `=` | `a + b` |
| Ternary | 3 | `? :` | `a ? b : c` |

---

### Why This Matters
Almost every operator you'll learn in the upcoming topics (Arithmetic, Relational, Logical, etc.) already fits into one of these three groups. Keeping this in mind while learning each operator type will make it easier to remember how many values that operator actually needs to work.

---

⬅️ [Previous: 07. Operators Index](#) | [Next: Arithmetic Operators](#) ➡️
