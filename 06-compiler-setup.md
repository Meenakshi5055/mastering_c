# 🛠️ Topic 6: Compiler Setup & Your First C Program

[![Module 01](https://img.shields.io/badge/Module%2001-Environment%20Setup-2563eb?style=for-the-badge)](./module-01.md)
[![Level](https://img.shields.io/badge/Level-Beginner-22c55e?style=for-the-badge)](#learning-objectives)
[![Language](https://img.shields.io/badge/Language-C-0f172a?style=for-the-badge)](https://en.wikipedia.org/wiki/C_(programming_language))
[![Compiler](https://img.shields.io/badge/Setup-GCC%20%2F%20Clang-ff6b35?style=for-the-badge)](#install-and-verify-a-compiler)

> 🌱 **Welcome to your first real C setup!**
> This topic helps you install the tools, write your first program, compile it, and understand what happens behind the scenes. By the end, you will be able to run C code on your computer with confidence.

## 🎯 Learning objectives

By the end of this topic, you should be able to:

- explain what a compiler is and why C needs one;
- install or verify a C compiler on Windows, macOS, or Linux;
- use VS Code or another editor to create a `.c` file;
- compile and run a C program from the terminal;
- understand the meaning of `#include`, `main`, `printf`, `\n`, and `return 0;`;
- troubleshoot common beginner mistakes.

## 💡 What will you gain from this topic?

After completing this lesson, you will be able to:

- ✅ set up a working C environment on your computer;
- ✅ create and save a `.c` file;
- ✅ compile code into an executable program;
- ✅ run that program successfully;
- ✅ debug basic compiler errors;
- ✅ understand the flow from source code to a final executable.

> 🧠 **Simple idea:**
> Your editor helps you write code. The compiler translates that code into something the computer can run.

---

## ⚙️ What is a compiler?

A compiler is a program that converts C source code into machine code or an executable file.

C is a compiled language. Unlike Python or JavaScript, C source code must be converted into a runnable program before it can execute.

### The 4 stages of compilation

1. **Preprocessing**: reads the source code and expands headers like `#include <stdio.h>`.
2. **Compilation**: converts the preprocessed code into assembly language.
3. **Assembly**: turns assembly into object code.
4. **Linking**: combines object code with library files to create a final executable.

```text
hello.c → preprocessing → compilation → assembly → linking → hello.exe / hello
```

> 🔍 **Why this matters:**
> If there is a problem with a header, syntax, variable, or library, it can show up at different stages of compilation. Understanding this helps you fix errors faster.

---

## 🧰 Editor, IDE, or compiler?

| Tool | Purpose | Example |
| --- | --- | --- |
| **Text editor** | Write and edit code | VS Code, Vim, Neovim |
| **Compiler** | Translate code into an executable | GCC, Clang |
| **IDE** | Write, compile, run, and debug code | Code::Blocks, Visual Studio |

### Quick beginner rule

- If you are writing code, you need an editor.
- If you want to run C code, you need a compiler.
- An IDE is just a more complete package.

---

## 🌍 What tools can you use?

### Offline tools

- **VS Code** – lightweight and popular for learning C
- **Code::Blocks** – beginner-friendly IDE with built-in tools
- **Dev-C++** – simple C/C++ IDE
- **Vim / Neovim** – terminal-based editor for advanced users

### Online tools

- **Programiz** – quick and beginner-friendly
- **OnlineGDB** – allows coding and debugging in browser
- **OneCompiler** – fast testing environment

> ✅ Online compilers are great for quick practice, but an offline setup is preferred when you want to build real projects and learn proper tools.

> ⚠️ **Turbo C++** is outdated and not recommended for modern learning.

---

## 📥 Install and verify a compiler

### 🪟 Windows

Use a modern GCC toolchain such as **MinGW-w64** or **MSYS2**.

1. Download it from: https://www.mingw-w64.org
2. Install it and remember the folder path, such as `C:\MinGW\bin`
3. Add that folder to your system `PATH`
4. Open a new terminal and run:

```bash
gcc --version
```

If it prints a version number, your compiler is installed correctly.

> 💡 If `gcc` is not recognized, your environment variables may not be set properly.

### 🍎 macOS

Install the command-line tools:

```bash
xcode-select --install
```

Then verify the compiler:

```bash
gcc --version
```

On modern macOS systems, `gcc` often points to Clang, which is completely normal and works for C development.

### 🐧 Linux

On Ubuntu/Debian-based systems:

```bash
sudo apt update
sudo apt install build-essential
```

Verify it:

```bash
gcc --version
```

> 📌 On other distributions, package names and installation commands may differ, but the goal is the same: install the C compiler toolchain.

---

## ✍️ Set up VS Code

### Step 1: Install VS Code

- Go to https://code.visualstudio.com
- Download the installer for your OS
- Run the installer and keep the default options

### Step 2: Install C extensions

Open VS Code and go to the **Extensions** tab.

Install:

- **C/C++** by Microsoft
- **Code Runner**

These give you:

- syntax highlighting;
- error detection;
- IntelliSense suggestions;
- a quick Run button.

### Step 3: Create a project folder

- Create a folder on your computer for C programs
- Open that folder in VS Code
- Create a new file named `hello.c`

> ✅ The file extension `.c` tells the compiler that this is a C source file.

---

## 🚀 Write your first program

Create this file called `hello.c`:

```c
#include <stdio.h>

int main(void) {
    printf("Hello, World!\n");
    return 0;
}
```

### Compile it

#### Windows

```bash
gcc hello.c -o hello.exe
hello.exe
```

#### macOS / Linux

```bash
gcc hello.c -o hello
./hello
```

### Expected output

```text
Hello, World!
```

🎉 **That is your first successful C program!**

---

## 🔎 Code breakdown

- `#include <stdio.h>`: includes the input/output library so we can use `printf()`
- `int main(void)`: the main function where program execution starts
- `printf("Hello, World!\n")`: prints text to the terminal
- `\n`: newline escape sequence, moves the cursor to the next line
- `return 0;`: tells the operating system that the program ended successfully

### Mini explanation

Think of this program like a simple instruction set:

- “Include standard I/O tools.”
- “Start the program.”
- “Print a message.”
- “Return success.”

That is the foundation of almost every C program you will write later.

---

## 🧩 Common beginner doubts

### Why do I need both an editor and a compiler?

Because they do different jobs:

- the editor helps you type and edit code;
- the compiler turns your code into an executable form.

### Why doesn’t VS Code run C by itself?

VS Code is just a text editor and a code environment. It does not include a C compiler by default. You still need a compiler like GCC or Clang installed.

### Why do I need `#include <stdio.h>`?

Because `printf()` is defined in the standard input/output library. Without the header, the compiler may not know what `printf` is.

### What happens if I forget a semicolon?

The compiler will report a syntax error. In C, semicolons end statements. Missing them usually breaks the code.

### Why is `return 0;` important?

It tells the operating system: “Everything worked correctly.” A program can still run without it in some cases, but returning `0` is the standard successful exit.

### What if the compiler says command not found?

Then your compiler is not installed correctly or not added to `PATH`. Check the installation steps and restart the terminal.

### What happens if I write the file as `hello.txt`?

The compiler may not treat it as a C source file, because it expects a `.c` extension.

> 🧠 **Operator reminder:**
> Operators like `+`, `-`, `*`, `/`, `%`, `==`, `&&`, and `||` are introduced later. They perform actions on values. Example: `2 + 3` gives `5`.

---

## ⚠️ Common errors and fixes

### Error: `gcc: command not found`

Fix:

- install GCC/Clang
- verify it is in your `PATH`
- reopen the terminal

### Error: `file not found`

Fix:

- make sure you are in the same folder as `hello.c`
- check the file name exactly
- use `ls` or `dir` to confirm it exists

### Error: `implicit declaration of function 'printf'`

Fix:

- add `#include <stdio.h>`
- compile again

### Error: `expected ';' before '}'`

Fix:

- check for missing semicolons
- inspect the lines around the error

---

## 🧪 Quick practice challenge

Create a file named `about-me.c` and print:

```text
My name is ______.
I am learning C.
```

You can do this with:

```c
#include <stdio.h>

int main(void) {
    printf("My name is ______.\n");
    printf("I am learning C.\n");
    return 0;
}
```

Try changing the text and then compile and run it.

---

## ✅ Module checkpoint

You are ready for the next step when you can:

- explain what a compiler does;
- explain the difference between editor and compiler;
- install or verify GCC/Clang;
- create a `.c` file;
- compile and run a C program;
- explain the purpose of `printf`, `main`, and `return 0;`;
- fix basic setup problems.

---

<div style="display: block; width: 100%; overflow: hidden;">
  <a href="./05-logic-building.md" style="float: left;">⬅️ Previous: Logic Building</a>
  <a href="./module-02.md" style="float: right;">Next: Module 02 🚀 ➡️</a>
</div>

<br>

<div align="center">
  <a href="./module-01.md">📋 Module 01 Index</a>
</div>
