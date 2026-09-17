## Setting up the environment and first C program

To write and run C programs, you need two things: a compiler (which converts C source code into an executable program) and, usually, an editor or IDE (a place to write your code comfortably). Here are the basics you need to get started.

C is a compiled language. Unlike interpreted languages, C source code must be converted into an executable file before it can run.

---

### The 4 Stages of Compilation:

1. **Preprocessing (`.c` -> `.i`)**: Removes comments and expands macros and header files (for example, `#include <stdio.h>`).
2. **Compilation (`.i` -> `.s`)**: Translates the preprocessed code into assembly code.
3. **Assembly (`.s` -> `.o` / `.obj`)**: Converts the assembly code into binary machine object code.
4. **Linking (`.o` -> `.exe`)**: Combines the object code with the C standard library to create the final executable file.

---

### Environment Setup:

#### Available tools to write and run C

> **Offline (installed on your computer):**

- **VS Code** – A free, lightweight code editor. It needs a separate compiler installed, plus extensions.
- **Code::Blocks** – A free IDE made specifically for C/C++. It comes bundled with a compiler, so setup is easier.
- **Dev-C++** – Another beginner-friendly IDE with a bundled compiler.
- **Turbo C++** – An older compiler that is not recommended for beginners today because it does not support modern systems well.
- **Vim / Neovim** – Lightweight text editors mainly used by experienced programmers who prefer working from the terminal.

> **Online (no installation needed, runs in the browser):**

- **Programiz** – A simple online C compiler, good for quick practice.
- **OnlineGDB** – Lets you write, run, and debug C code online.
- **OneCompiler** – Another browser-based compiler for quick testing.

Online compilers are great for practicing immediately without setup, but an offline setup is better once you are ready to build real projects.

---

### Setting Up VS Code (Step-by-Step):

**Step 1: Install VS Code**

- Go to https://code.visualstudio.com.
- Download the installer for your operating system (Windows, macOS, or Linux).
- Run the installer and follow the on-screen steps, keeping the default options selected.

**Step 2: Install a C Compiler**

VS Code itself does not compile code. It needs a compiler installed separately.

#### For Windows

- Download **MinGW-w64** from https://www.mingw-w64.org or install it using **MSYS2**.
- Install it and note the installation folder (for example, `C:\MinGW\bin`).
- Add the compiler folder to your `PATH` so your computer can find `gcc` from any terminal.
- To do this:
  - Search for **Environment Variables** in the Windows search bar.
  - Under **System variables**, find **Path** and click **Edit**.
  - Add the path to the compiler's `bin` folder (for example, `C:\MinGW\bin`).
  - Click **OK** to save.
- Check if it worked by opening Command Prompt and typing:

```bash
gcc --version
```

If a version number appears, the compiler is installed correctly.

#### For macOS

- Open the Terminal app.
- Install the Xcode Command Line Tools by running:

```bash
xcode-select --install
```

- After installation, check the compiler:

```bash
gcc --version
```

If the command works, your compiler is ready.

#### For Linux

On Ubuntu or Debian-based systems, you can install the compiler using:

```bash
sudo apt update
sudo apt install build-essential
```

Then verify it with:

```bash
gcc --version
```

If the version is displayed, the compiler is installed and working.

**Step 3: Install VS Code Extensions**

- Open VS Code.
- Click the **Extensions** icon in the left sidebar (it looks like four small squares).
- Search for **C/C++** by Microsoft and click **Install**.
  - This gives you syntax highlighting, error checking, and IntelliSense.
- Search for **Code Runner** and install it.
  - This adds a simple **Run** button to execute your C file with one click.

**Step 4: Create a Project and File**

- Create a new folder on your computer for your C projects.
- In VS Code, go to **File → Open Folder** and select that folder.
- Create a new file inside it named `hello.c`.
  - The `.c` extension tells the compiler that this is a C source file.

*I recommend VS Code because it is lightweight, flexible, and supports many tools and extensions. It works well for beginner projects and larger programs too.*

---

### First C Program: "Hello, World!"

```c
#include <stdio.h>

int main() {
    // Print text to the screen
    printf("Hello, World!\n");
    return 0;
}
```

**How to run it:**

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

You should see:

```bash
Hello, World!
```

---

### Breakdown of the Code:

- `#include <stdio.h>`: Includes the Standard Input Output library, which provides functions like `printf()`.
- `int main()`: The main function where the program starts running.
- `printf("...")`: Prints text to the console.
- `\n`: Escape sequence for a new line.
- `return 0;`: Tells the operating system that the program executed successfully.

---

**🎉 Module 01 is completed: Introduction & Environment Setup!**

[⬅️ Previous topic 05: Logic Building](./05-logic-building.md) | 

[📋 Module 01 Index](./module-01.md) | 

[➡️ 🚀 Move to Module 02](./module-02.md)
