## Relational Operators

**What are Relational Operators?**
Relational operators are used to **compare two values**. The result of a relational operation is always either **1 (true)** or **0 (false)** — C does not have a separate boolean type, so it uses integers to represent true/false.

---

### List of Relational Operators

| Operator | Meaning | Example | Result (if a=10, b=20) |
|---|---|---|---|
| `==` | Equal to | `a == b` | `0` (false) |
| `!=` | Not equal to | `a != b` | `1` (true) |
| `>` | Greater than | `a > b` | `0` (false) |
| `<` | Less than | `a < b` | `1` (true) |
| `>=` | Greater than or equal to | `a >= b` | `0` (false) |
| `<=` | Less than or equal to | `a <= b` | `1` (true) |

These are all **binary operators** (2 operands, as covered earlier).

---

### Important Rules & Behaviors

1. **Result is always `1` or `0`** — never `true`/`false` as words, since C doesn't have a built-in boolean type (unless you explicitly use `<stdbool.h>`).
2. **Don't confuse `=` with `==`.** A single `=` **assigns** a value; a double `==` **compares** two values. Writing `if (a = 5)` is a very common mistake — it assigns 5 to `a` instead of checking if `a` equals 5.
3. Relational operators are most often used inside **conditions** — `if`, `while`, `for` — to decide whether a block of code should run.
4. You can compare integers, floats, and characters (characters are compared using their ASCII values).

---

### Example Program

```c
#include <stdio.h>

int main() {
    int a = 10, b = 20;
    printf("%d\n", a == b);
    printf("%d\n", a != b);
    printf("%d\n", a > b);
    printf("%d\n", a < b);
    return 0;
}
```
**Output:**
```
0
1
0
1
```

---

## Practice Problems

**Problem 1 (Syntax-based):** What is the output of `printf("%d", 5 == 5);`?

<details>
<summary>Click to see solution</summary>

Output: `1`
Since 5 is equal to 5, the comparison is true, and C represents true as `1`.

</details>

---

**Problem 2 (Syntax-based):** What is the output of `printf("%d", 'A' > 'a');`?

<details>
<summary>Click to see solution</summary>

Output: `0`
Characters are compared using ASCII values. `'A'` is 65 and `'a'` is 97, so `'A' > 'a'` is false, giving `0`.

</details>

---

**Problem 3 (Logic-based, no full program):** If `x = 15`, what will `x != 10` and `x <= 15` evaluate to?

<details>
<summary>Click to see solution</summary>

`x != 10` → `1` (true, since 15 is not equal to 10)
`x <= 15` → `1` (true, since 15 is equal to 15, and `<=` includes equal)

</details>

---

**Problem 4 (Full Program):** What does this program print, and why?

```c
#include <stdio.h>

int main() {
    int age = 18;
    if (age >= 18) {
        printf("Eligible to vote\n");
    } else {
        printf("Not eligible to vote\n");
    }
    return 0;
}
```

<details>
<summary>Click to see solution</summary>

Output: `Eligible to vote`

Explanation: `age >= 18` checks if `age` is 18 (equal is included). Since `age` is exactly 18, `age >= 18` evaluates to `1` (true), so the code inside the `if` block runs, printing "Eligible to vote."

</details>

---

**Problem 5 (Full Program — common mistake):** What is the problem with this code?

```c
#include <stdio.h>

int main() {
    int num = 10;
    if (num = 5) {
        printf("Number is 5\n");
    } else {
        printf("Number is not 5\n");
    }
    return 0;
}
```

<details>
<summary>Click to see solution</summary>

Output: `Number is 5`

Explanation: This is a classic bug. `num = 5` uses a single `=`, which **assigns** 5 to `num` instead of comparing it. Since the assignment itself returns the value `5` (which is non-zero, meaning "true" in C), the `if` block runs regardless of what `num` was before. The correct code should use `num == 5` to actually compare.

</details>

---

⬅️ [Previous: Arithmetic Operators](#) | [Next: Logical Operators](#) ➡️
