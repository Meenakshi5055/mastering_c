## Setting up the environment and first c_programming

To write and run C programs, you need two things: a compiler (converts your C code into a program the computer can run) and, usually, an editor or IDE (a place to write your code comfortably). Here are the common choices.

C is a compiled language. Unlike interpreted languages, C source code must be converted into an executable file before running.

**The 4 Stages of Compilation:**

1. **Preprocessing (`.c` -> `.i`):** Removes comments and expands macros/header files (e.g., `#include <stdio.h>`).
2. **Compilation (`.i` -> `.s`):** Translates preprocessed code into assembly code.
3. **Assembly (`.s` -> `.o` / `.obj`):** Converts assembly code into binary machine object code.
4. **Linking (`.o` -> `.exe`):** Combines object code with C standard library code to produce the final executable file.

---

**Environment Setup:**

Available Tools to Write & Run C

> *Offline (installed on your computer):

VS Code – A free, lightweight code editor. Needs a separate compiler installed, plus extensions added.
Code::Blocks – A free IDE made specifically for C/C++. Comes bundled with a compiler, so setup is simpler.
Dev-C++ – Another free, beginner-friendly IDE with a bundled compiler.
Turbo C++ – An old, outdated compiler. Not recommended for beginners today since it doesn't support modern systems well.
Vim / Neovim – Lightweight text editors, mainly used by more experienced programmers who prefer working from the terminal.

> *Online (no installation needed, runs in the browser):

* Programiz – Simple online C compiler, good for quick practice.
* OnlineGDB – Lets you write, run, and debug C code online.
* OneCompiler – Another browser-based compiler for quick testing.

Online compilers are the fastest way to start practicing immediately with no setup. Installing an offline setup is better once you're ready to build real projects.

**Setting Up VS Code (Step-by-Step):**

* Step 1: Install VS Code

. Go to https://code.visualstudio.com.

. Download the installer for your operating system (Windows/Mac/Linux).

. Run the installer and follow the on-screen steps (keep default options selected).

* Step 2: Install a C Compiler (MinGW, for Windows)*

. VS Code doesn't compile code by itself — it needs a compiler installed separately.

. Download MinGW-w64 from https://www.mingw-w64.org (or via MSYS2, a common installer for it).

. Install it, making sure to note the installation folder (e.g., C:\MinGW\bin).

. Add it to PATH (so your computer knows where to find the compiler from any folder):
Search "Environment Variables" in Windows search.

. Under "System variables," find Path, click Edit, then Add.

. Paste the path to the compiler's bin folder (e.g., C:\MinGW\bin).

. Click OK on all windows to save.

. To check it worked, open a terminal (Command Prompt) and type gcc --version. If it shows a version number, the compiler is correctly installed and linked.

* Step 3: Install VS Code Extensions
Open VS Code.*

. Click the Extensions icon on the left sidebar (it looks like four small squares).

. Search for "C/C++" (by Microsoft) and click Install — this gives you syntax highlighting, error checking, and IntelliSense (auto-suggestions).

. Search for "Code Runner" and install it — this adds a simple "Run" button so you can execute your C file with one click.

* Step 4: Create a Project and File

.Create a new folder on your computer for your C projects.

.In VS Code, go to File → Open Folder, and select that folder.

. Create a new file inside it named hello.c (the .c extension tells the compiler it's a C file).

I would recommend VS code because it allows different types of programs to run in one place by downloading extensions and runs offline.

**First C Program: "Hello, World!"**

```c
#include <stdio.h>

int main() {
    // Print text to the screen
    printf("Hello, World!\n");
    return 0;
}

**Breakdown of the Code:**

* ​#include <stdio.h>: Includes the Standard Input Output library header needed for printf().
* ​int main(): The main entry point function where program execution begins.
* ​printf("...");: Built-in C function used to output text inside double quotes to the console.
* ​\n: Escape sequence for a new line.
* ​return 0;: Signals to the operating system that the program executed successfully.

**​🎉  Module 01 is completed: Introduction & Environment Setup!**

[⬅️ Previous topic 05:Logic building](./05-logic-building.md) | 

[📋 Module 01 Index]() | 

[➡️ 🚀 Move to Module 02]()