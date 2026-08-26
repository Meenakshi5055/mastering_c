## Topic_3 Computer languages 

**Why do different types of languages exist?**

A computer only understands one language: binary (0s and 1s). But writing programs directly in 0s and 1s is very hard for humans. So, over time, programmers created languages that are easier for people to write, and then built tools to convert those languages back into binary for the computer to run. This is why programming languages are grouped into levels — based on how close they are to human language versus machine language.

**Two main levels:**

1. Low-Level Languages
These are close to the computer's hardware and far from human language.
* Machine Level Language: Written purely in 0s and 1s. This is the only language the computer's processor directly understands.
- Advantage: Runs very fast and uses the computer efficiently, since no translation is needed.
- Disadvantage: Extremely hard for humans to read, write, or debug. Also, it's different for every type of processor, so code written for one computer won't work on another.
* Assembly Level Language: Uses short human-readable codes (called mnemonics, like ADD, MOV, SUB) instead of pure binary.
Advantage: Easier to write and understand than machine code.
Disadvantage: Still tied to a specific processor type, and still fairly hard to learn. Needs a translator called an assembler to convert it into machine code.
2. High-Level Languages
These are close to human language (English-like) and far from machine language. Examples: C, Python, Java.
* Advantage: Much easier to read, write, and fix. The same code can often run on different computers with little or no change (portability).
* Disadvantage: Needs a translator (a compiler or interpreter) to convert it into machine code, which can make it slightly slower than low-level code.

**How the translation works:**

* Assembly code → converted by an assembler → machine code
* High-level code → converted by a compiler (all at once) or an interpreter (line by line) → machine code

**Where does C fit in?**

C is called a middle-level language. This means:
It has the readability and structure of a high-level language (easy to write, uses English-like keywords like if, while, return).
But it also gives you low-level access to memory and hardware (through pointers), which is normally only possible in low-level languages.
This combination is exactly why C became so important: it's easy enough for humans to write real programs, but powerful enough to build operating systems and control hardware directly — something pure high-level languages usually can't do as well.

Quick comparison:

Level
Example
Speed
Ease of Use
Portability
Machine Level
Binary (0,1)
Fastest
Hardest
None
Assembly Level
Mnemonics (ADD, MOV)
Very Fast
Hard
Very Low
High Level
C, Python, Java
Slower
Easy
High
C (Middle Level)
C
Fast
Easy–Moderate
High