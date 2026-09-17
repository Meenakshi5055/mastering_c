## Arithmetic Operators

**What are Arithmetic Operators?**
Arithmetic operators perform basic **mathematical calculations** on numeric values — the same operations you use in everyday math, adapted for programming.

---

### List of Arithmetic Operators

| Operator | Meaning | Example | Result (if a=10, b=3) |
|---|---|---|---|
| `+` | Addition | `a + b` | `13` |
| `-` | Subtraction | `a - b` | `7` |
| `*` | Multiplication | `a * b` | `30` |
| `/` | Division | `a / b` | `3` |
| `%` | Modulus (remainder) | `a % b` | `1` |

All of these are **binary operators** — each needs exactly 2 operands (as covered in the previous topic).

---

### Important Rules & Behaviors

1. **Integer Division:** When both operands are integers, `/` gives only the **whole number part**, dropping any decimal. `10 / 3` gives `3`, not `3.33`.
2. **To get a decimal result**, at least one operand must be a `float` or `double`: `10.0 / 3` gives `3.333333`.
3. **Modulus (`%`) only works with integers.** It gives the **remainder** after division: `10 % 3` gives `1` (because 10 ÷ 3 = 3 remainder 1). Using `%` with `float`/`double` causes a compiler error.
4. **Order of operations (precedence)** follows standard math rules: `*`, `/`, `%` are evaluated before `+` and `-`. Use parentheses `()` to control the order explicitly.
5. **Modulus with negative numbers** takes the sign of the first operand in C: `-10 % 3` gives `-1`, not `2`.

---

### Example Program

```c
#include <stdio.h>

int main() {
    int a = 10, b = 3;
    printf("Sum: %d\n", a + b);
    printf("Difference: %d\n", a - b);
    printf("Product: %d\n", a * b);
    printf("Quotient: %d\n", a / b);
    printf("Remainder: %d\n", a % b);
    return 0;
}
```
**Output:**
```
Sum: 13
Difference: 7
Product: 30
Quotient: 3
Remainder: 1
```

---

## Practice Problems

**Problem 1:** What is the output of `printf("%d", 7 / 2);`?

<details>
<summary>Click to see solution</summary>

Output: `3`
Since both operands are integers, `/` performs integer division and drops the decimal part (7 ÷ 2 = 3.5 → 3).

</details>

---

**Problem 2:** What is the output of `printf("%d", 7 % 2);`?

<details>
<summary>Click to see solution</summary>

Output: `1`
7 divided by 2 gives quotient 3 and remainder 1, so `%` returns `1`.

</details>

---

**Problem 3:** What is the output of `printf("%f", 7.0 / 2);`?

<details>
<summary>Click to see solution</summary>

Output: `3.500000`
Since one operand (`7.0`) is a float, the division is performed as floating-point division, keeping the decimal part.

</details>

---

**Problem 4:** What is the output of `printf("%d", -7 % 2);`?

<details>
<summary>Click to see solution</summary>

Output: `-1`
In C, the result of `%` takes the sign of the first operand (the dividend). Since `-7` is negative, the remainder is also negative.

</details>

---

**Problem 5:** Evaluate `10 + 5 * 2 - 3 / 3` following operator precedence.

<details>
<summary>Click to see solution</summary>

Output: `19`
Step by step:
- `5 * 2 = 10` (multiplication first)
- `3 / 3 = 1` (division first)
- `10 + 10 - 1 = 19` (then addition/subtraction, left to right)

</details>

---

⬅️ [Previous: Operand Arity](#) | [Next: Relational Operators](#) ➡️
