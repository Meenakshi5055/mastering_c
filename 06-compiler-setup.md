# 🛠️ Topic 6: Compiler Setup & Your First C Program

[![Module 01](https://img.shields.io/badge/Module%2001-Environment%20Setup-2563eb?style=for-the-badge)](./module-01.md)
[![Level](https://img.shields.io/badge/Level-Beginner-22c55e?style=for-the-badge)](#learning-objectives)
[![Language](https://img.shields.io/badge/Language-C-0f172a?style=for-the-badge)](https://en.wikipedia.org/wiki/C_(programming_language))

> 🌱 **Your first step into real C programming!** In this topic, you will prepare your coding environment, compile a program, run it, and understand what happens behind the scenes.

## 🎯 Learning objectives

By the end of this topic, you should be able to:

- explain the difference between a text editor, an IDE, and a compiler;
- verify that a C compiler is installed;
- compile and run a C program from a terminal;
- understand the basic parts of a `Hello, World!` program; and
- troubleshoot common setup and compilation problems.

## 💡 What can you gain from this topic?

After completing this topic, you can:

- ✅ set up C on **Windows, macOS, or Linux**;
- ✅ create your first `.c` source file;
- ✅ turn source code into an executable program;
- ✅ run a program from the terminal instead of depending only on a Run button; and
- ✅ understand the basic journey from C code to a program your computer can execute.

> 🧠 **Important idea:** VS Code is where you write code. A compiler is what translates that code into a runnable program. VS Code does not compile C by itself.

---

## 🧰 Compiler, editor, or IDE?

| Tool | What it does | Examples |
| --- | --- | --- |
| **Text editor** | Helps you write and edit source code | VS Code, Vim, Neovim |
| **Compiler** | Translates C source code into machine code | GCC, Clang |
| **IDE** | Combines editing, compiling, debugging, and project tools | Code::Blocks, Visual Studio |

You may use VS Code with GCC or Clang. This is a common and flexible setup for learning C.

## ⚙️ The four compilation stages

When you compile a C program, the toolchain normally performs these stages:

1. **Preprocessing:** Expands headers and macros and removes comments.
2. **Compilation:** Converts the preprocessed C code into assembly code.
3. **Assembly:** Converts assembly code into an object file.
4. **Linking:** Combines object files and libraries into an executable program.

```text
hello.c → preprocessing → compilation → assembly → linking → executable
```

> 🔍 **Why does this matter?** Errors can occur at different stages. For example, a missing header may affect preprocessing, while an undefined function may be reported during linking.

---

## 🌍 Choose an environment

- **VS Code:** Lightweight editor; install a C compiler separately.
- **Code::Blocks:** Beginner-friendly IDE; choose a current distribution with a compiler.
- **Online compilers:** Programiz, OnlineGDB, and OneCompiler are useful for quick practice.

⚠️ Avoid relying on Turbo C for modern learning. It is obsolete and does not represent current C toolchains or standards.

---

## 📥 Install and verify a compiler

### 🪟 Windows

Install a current GCC toolchain such as **MSYS2 MinGW-w64**. During setup, make sure the compiler directory is available in your `PATH`.

Open a **new** terminal after installation and verify it:

```bash
gcc --version
```

If Windows says that `gcc` is not recognized, the compiler may not be installed correctly or its `bin` directory may not be in `PATH`.

### 🍎 macOS

Install Apple’s Command Line Tools:

```bash
xcode-select --install
```

Then verify the compiler:

```bash
clang --version
gcc --version
```

On modern macOS systems, `gcc` may point to Apple Clang instead of GNU GCC. That is normal, and it can compile standard C programs.

### 🐧 Ubuntu or Debian Linux

Install the standard C development tools:

```bash
sudo apt update
sudo apt install build-essential
```

Then verify them:

```bash
cc --version
gcc --version
```

> 📌 Other Linux distributions use different package managers. For example, Fedora commonly uses `sudo dnf group install "Development Tools"`.

---

## ✍️ Write your first program

Create a file named `hello.c` and add this code:

```c
#include <stdio.h>

int main(void) {
    printf("Hello, World!\n");
    return 0;
}
```

### ▶️ Compile the program

The following command compiles the file with useful warnings enabled:

```bash
gcc -std=c17 -Wall -Wextra -pedantic hello.c -o hello
```

Here is what the options mean:

- `-std=c17` selects the C17 language standard;
- `-Wall` enables many helpful warnings;
- `-Wextra` enables additional warnings;
- `-pedantic` checks strict standard compliance; and
- `-o hello` names the output executable `hello`.

### 🚀 Run the program

On macOS or Linux:

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

🎉 **Congratulations! You have written, compiled, and executed your first C program.**

---

## 🔎 Code breakdown

- `#include <stdio.h>` provides the declaration for `printf`.
- `int main(void)` defines the program entry point and says that it accepts no arguments.
- `printf(...)` writes text to standard output.
- `"Hello, World!"` is a string literal—the text that will be displayed.
- `\n` is an escape sequence that moves the cursor to a new line.
- `return 0;` reports successful completion to the operating system.

### ❓ What happens if I change the code?

| Change | Result |
| --- | --- |
| Remove the semicolon after `printf(...)` | The compiler reports a syntax error. |
| Change `"Hello, World!"` | The new text is printed. |
| Remove `#include <stdio.h>` | The compiler may warn that `printf` is undeclared, and compilation can fail under strict settings. |
| Replace `\\n` with `\\t` | The output uses a tab instead of a new line. |
| Replace `return 0;` with `return 1;` | The program still runs, but `1` usually communicates failure or an unsuccessful status. |
| Rename `hello.c` to `hello.txt` | The compiler may not treat it as a C source file. |

> 🧩 **About operators:** Operators such as `+`, `-`, `*`, `/`, `==`, and `&&` will be introduced in the next lessons. An operator performs an action on one or more values—for example, `2 + 3` produces `5`. Use this page to focus on setup and compilation first.

---

## 🧯 Common problems and solutions

<details>
<summary>❌ <code>gcc</code> or <code>clang</code> is not found</summary>

Install a compiler for your operating system and check that its executable directory is in `PATH`. Close and reopen the terminal after changing `PATH`.

</details>

<details>
<summary>❌ The compiler says the source file does not exist</summary>

Check that your terminal is open in the folder containing `hello.c`. You can list files with `dir` on Windows or `ls` on macOS/Linux.

</details>

<details>
<summary>❌ The program does not run after compilation</summary>

Use `./hello` on macOS/Linux and `hello.exe` on Windows. Also confirm that compilation completed without errors.

</details>

<details>
<summary>❌ The file is saved as <code>hello.c.txt</code></summary>

Turn on file-name extensions in your file manager and rename the file to exactly `hello.c`.

</details>

<details>
<summary>❌ I see warnings</summary>

Warnings are useful clues, not decorations. Read the warning, locate the relevant line, fix the problem, and compile again.

</details>

## 🧪 Quick practice challenge

Create `about-me.c` and change the program so it prints:

```text
My name is ______.
I am learning C.
```

**Hint:** Use two `printf` statements or one string containing `\n`.

## ✅ Module checkpoint

You are ready for Module 02 when you can:

- explain what a compiler does;
- identify the difference between an editor and a compiler;
- compile the program with warnings enabled;
- run it using the correct command for your operating system; and
- explain what `#include`, `main`, `printf`, `\n`, and `return 0` do.

---

<div align="left">
  <a href="./05-logic-building.md">⬅️ Previous: Logic Building</a>
  <span style="float: right"><a href="./module-02.md">Next: Module 02 🚀 ➡️</a></span>
</div>

<br>

<div align="center">
  <a href="./module-01.md">📋 Module 01 Index</a>
</div>
