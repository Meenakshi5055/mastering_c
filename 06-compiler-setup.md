## Setting up the environment and first c_programming

To write and run C programs, you need two things: a compiler (converts your C code into a program the computer can run) and, usually, an editor or IDE (a place to write your code comfortably). Here are the common choices.

C is a compiled language. Unlike interpreted languages, C source code must be converted into an executable file before running.

**The 4 Stages of Compilation:**

1. **Preprocessing (`.c` -> `.i`):** Removes comments and expands macros/header files (e.g., `#include <stdio.h>`).
2. **Compilation (`.i` -> `.s`):** Translates preprocessed code into assembly code.
3. **Assembly (`.s` -> `.o` / `.obj`):** Converts assembly code into binary machine object code.
4. **Linking (`.o` -> `.exe`):** Combines object code with C standard library code to produce the final executable file.

---