# Topic 1: Definition & Overview

## Learning objectives

By the end of this topic, you should be able to:

- define the C programming language
- identify common uses of C
- describe its main characteristics
- explain why C is important to learn

## What is C?

C is a general-purpose, procedural, statically typed programming language. It was designed to provide a practical balance between readable code and direct control over computer resources.

C programs are usually compiled: a compiler translates source code into machine code that the computer can execute. C gives programmers access to memory through pointers and supports efficient, predictable programs.

> “Middle-level language” is an informal description of C. It reflects C’s combination of high-level structure and low-level memory and hardware access; it is not an official language category.

## Where is C used?

- operating systems and system utilities
- embedded systems and device firmware
- compilers, interpreters, and runtimes
- databases and networking software
- performance-critical libraries and applications

## Key characteristics

- **Compiled:** Source code is translated before execution.
- **Procedural:** Programs are organized around functions and ordered steps.
- **Statically typed:** Variables have declared types checked by the compiler.
- **Efficient:** C has very little runtime overhead.
- **Portable:** Standard C can be compiled for many platforms, although platform-specific code may require changes.
- **Hardware-aware:** Pointers and bitwise operations enable fine-grained control.
- **Case-sensitive:** `main`, `Main`, and `MAIN` are different identifiers.

## A minimal example

```c
#include <stdio.h>

int main(void) {
    printf("Hello, C!\n");
    return 0;
}
```

The `stdio.h` header declares `printf`, `main` is the program entry point, and `return 0` reports successful completion.

## Practice

1. Name two areas where C is used.
2. Why does C need a compiler?
3. What is the difference between a compiled language and a procedural language?

## Key takeaway

C is a small, efficient, and powerful language that helps you understand both programming logic and how software interacts with hardware.

---

[⬅️ Module 01 Index](./module-01.md) | [➡️ Next topic: History & Creator](./02-history-and-creator.md)
