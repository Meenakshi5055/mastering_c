# Topic 6: Compiler Setup & Your First C Program

## Learning objectives

By the end of this topic, you should be able to:

- explain the role of a compiler and editor
- verify that a C compiler is installed
- compile and run a C program from a terminal
- understand the basic parts of a Hello World program

## Compiler and editor

A **text editor** or IDE is where you write source code. A **compiler** translates C source code into an executable program. An IDE may combine editing, compiling, debugging, and project tools, but an editor alone is not a compiler.

## The four compilation stages

1. **Preprocessing:** Expands headers and macros and removes comments.
2. **Compilation:** Converts preprocessed C into assembly code.
3. **Assembly:** Converts assembly into an object file.
4. **Linking:** Combines object files and libraries into an executable.

## Choose an environment

- **VS Code:** Lightweight editor; install a C compiler separately.
- **Code::Blocks:** Beginner-friendly IDE; choose a current distribution with a compiler.
- **Online compilers:** Programiz, OnlineGDB, and OneCompiler are useful for quick practice.

Avoid relying on Turbo C for modern learning because it is obsolete and does not represent current C toolchains.

## Install a compiler

### Windows

Install a current GCC toolchain such as **MSYS2 MinGW-w64**, then ensure its compiler directory is available in `PATH`. Open a new terminal and verify:

```bash
gcc --version
```

### macOS

Install Apple’s Command Line Tools:

```bash
xcode-select --install
```

Then verify the compiler:

```bash
clang --version
gcc --version
```

On modern macOS systems, `gcc` may point to Apple Clang rather than GNU GCC; that is fine for compiling standard C programs.

### Ubuntu or Debian

```bash
sudo apt update
sudo apt install build-essential
cc --version
gcc --version
```

## Write your first program

Create a file named `hello.c`:

```c
#include <stdio.h>

int main(void) {
    printf("Hello, World!\n");
    return 0;
}
```

Compile with warnings enabled:

```bash
gcc -std=c17 -Wall -Wextra -pedantic hello.c -o hello
```

Run it on macOS or Linux:

```bash
./hello
```

On Windows, the executable may be named `hello.exe`:

```bash
hello.exe
```

Expected output:

```text
Hello, World!
```

## Code breakdown

- `#include <stdio.h>` provides the declaration for `printf`.
- `int main(void)` defines the program entry point and says it accepts no arguments.
- `printf` writes text to standard output.
- `\n` moves the cursor to a new line.
- `return 0` indicates successful completion.

## Troubleshooting

- If `gcc` or `clang` is not found, install a compiler and check your `PATH`.
- If compilation reports warnings, read them before running the program.
- If the executable does not run, use the platform-specific command above.
- Make sure the file is saved as `hello.c`, not `hello.c.txt`.

## Module checkpoint

You are ready for Module 02 when you can explain what a compiler does and compile the Hello World program without copying commands blindly.

---

[⬅️ Previous topic: Logic Building](./05-logic-building.md) | [📋 Module 01 Index](./module-01.md) | [➡️ Module 02](./module-02.md)
