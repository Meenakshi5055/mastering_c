# Topic 3: Computer Language Levels

## Learning objectives

- distinguish machine, assembly, and high-level languages
- understand how source code is translated
- explain where C fits in this comparison
- compare readability, portability, and hardware control

## Why do language levels exist?

Processors execute machine instructions, represented internally as bits. Writing programs directly in machine code is difficult, so programmers use increasingly readable languages and translators.

## Low-level languages

### Machine language

Machine language consists of processor-specific instructions represented as binary or encoded bytes. It can be executed directly by the processor, but it is difficult to read, write, debug, and move between processor families.

### Assembly language

Assembly uses mnemonics such as `MOV`, `ADD`, and `SUB`. An **assembler** translates assembly into machine code. Assembly provides precise hardware control but remains processor-specific.

## High-level languages

High-level languages use abstractions and syntax that are easier for people to understand. Examples include C, Python, and Java. A compiler or interpreter translates the program into a form the computer can execute.

Portability is not automatic: a program may still need platform-specific changes, libraries, or compiler settings.

## Where does C fit?

C is generally considered a high-level language with low-level capabilities. It provides functions, control structures, and readable syntax while also supporting pointers, manual memory management, and bitwise operations.

Calling C a **middle-level language** is an informal teaching term, not an official classification.

| Feature | Machine | Assembly | C |
| --- | --- | --- | --- |
| Readability | Very low | Low | Moderate to high |
| Hardware dependence | Very high | Very high | Lower, but platform code exists |
| Translator | None | Assembler | Compiler |
| Hardware control | Direct | Direct | Strong, through language features |
| Portability | Very low | Very low | Usually higher |

## Practice

1. Why is assembly more portable than machine code only in a limited sense?
2. Name two C features that provide low-level control.
3. Why does C still require a compiler even though it is close to hardware?

## Key takeaway

C bridges readable programming structure and low-level control, which makes it useful for software that must be both efficient and close to the hardware.

---

[⬅️ Previous topic: History & Creator](./02-history-and-creator.md) | [➡️ Next topic: Advantages & Disadvantages](./04-advantages-disadvantages.md)
