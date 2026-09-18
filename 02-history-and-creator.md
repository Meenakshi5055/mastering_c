# 🕰️ Topic 2: History & Creator

![Topic](https://img.shields.io/badge/Topic-History%20%26%20Creator-1E90FF)
![Level](https://img.shields.io/badge/Level-Beginner-2EA44F)
![Reading](https://img.shields.io/badge/Reading-5%20minutes-orange)
![Practice](https://img.shields.io/badge/Practice-Included-8A2BE2)

> 🎯 **Why learn the history of C?** Understanding where C came from makes its design choices—speed, portability, pointers, and strict syntax—much easier to understand.

## 🎯 Learning objectives

By the end of this topic, you will be able to:

- Identify who created C and where it was developed
- Explain the connection between B, C, and Unix
- Describe why rewriting Unix in C was important
- Recognise major C standardisation milestones
- Explain why C remains influential today

## 🎁 What will you gain?

After reading this topic, you will understand:

- 👨‍💻 Who created C and the problem it was designed to solve
- 🔗 How **B → C → Unix** are connected
- ⚙️ Why C can offer both hardware control and efficient programs
- 🌍 Why portability made C useful across different machines
- 📚 Why later languages borrowed ideas from C

## 👨‍💻 Who created C?

C was developed by **Dennis Ritchie** at Bell Labs in the United States. Development took place mainly between **1969 and 1973**. **Ken Thompson**, who created the earlier B language, strongly influenced the development of C.

> 📌 **Important:** Dennis Ritchie is generally credited as the creator of C, while Ken Thompson was an important collaborator and influenced its early design.

## 🔗 From B to C

Ken Thompson created **B**, a simpler language influenced by BCPL. B was useful for systems programming, but it did not provide all the features needed for the evolving Unix project.

Dennis Ritchie extended these ideas and developed **C**. C provided better data types and more control while remaining efficient and portable.

```text
BCPL → B → C → C++, Java, C#, Go, Rust and many other languages
```

## 🐚 C and Unix

C was created while Bell Labs was developing the **Unix** operating system. Unix was initially written largely in assembly language. Rewriting much of Unix in C made it easier to maintain, understand, and port to different hardware platforms.

### Why did this matter?

- 🧩 Assembly code is closely tied to one processor.
- 🔁 C made it possible to reuse much of the same source code on another system.
- 🛠️ Developers could maintain a large operating system more easily.
- ⚡ C still produced efficient compiled programs.

## 📅 Major milestones

| Period | Milestone | Why it matters |
|---|---|---|
| 1969–1973 | C developed at Bell Labs | Created for practical systems programming |
| 1978 | Kernighan and Ritchie published *The C Programming Language* | Helped spread C widely; often called K&R C |
| 1989/1990 | ANSI C / C89/C90 standardised | Created a common language specification |
| 1999 | C99 introduced major improvements | Added useful language and library features |
| 2011 | C11 added modern features | Improved support for concurrency and programming safety |
| 2017 | C17 provided clarifications and fixes | Improved consistency without a major redesign |
| 2023 | C23 brought further improvements | Continued modernisation of the language |

## ⚙️ Why did C become important?

- 🚀 **Efficiency:** C can produce fast compiled programs.
- 🧠 **Control:** Pointers and memory access allow close interaction with hardware.
- 🌍 **Portability:** The same source code can often be compiled for different platforms.
- 🪶 **Small runtime:** C is suitable for systems with limited resources.
- 🌱 **Influence:** Its syntax and concepts influenced C++, Java, C#, Go, Rust, and others.

## 🌐 C today

C remains common in:

- Operating-system kernels and system utilities
- Microcontroller firmware and embedded devices
- Databases and networking software
- Compilers, interpreters, and language runtimes
- High-performance libraries and security tools

## ❓ Common doubts

**1. Was C created before Unix?**

No. C was developed during the early Unix project and was then used to rewrite much of Unix.

**2. Is C the same as B?**

No. B influenced C, but C added stronger data types and capabilities that made it more suitable for larger systems.

**3. What happens if I use an operator in C?**

An operator performs an action on one or more operands. For example, `total = price + tax;` uses `=` for assignment and `+` for addition. The result depends on the operator and the data types involved. Operators are covered in detail in a later topic.

**4. What if I use `/` instead of `%`?**

`/` calculates a quotient, while `%` calculates a remainder when working with integers. For example, `7 / 2` produces `3` in integer arithmetic, while `7 % 2` produces `1`.

**5. Why can C be powerful but dangerous?**

C gives programmers direct control over memory. That control is useful for performance, but mistakes such as using an uninitialised pointer or accessing an array outside its bounds can cause crashes or security problems.

**6. Why is C still used if it is old?**

Its age is not its only measure of value. C is fast, portable, widely supported, and useful when performance and hardware control matter.

## 🧠 Quick practice

1. Who created C, and where was it developed?
2. What was the relationship between B and C?
3. Why was rewriting Unix in C useful?
4. Match the standards: **C99, C11, C17, C23**.
5. What is the difference between `/` and `%` for integer operands?
6. Name two advantages and one risk of giving programmers direct memory control.

## ✅ Key takeaway

C grew from practical systems-programming needs. It became influential because it combines **portability, efficiency, and hardware control**—a balance that continues to make it valuable today.

<p align="left">
  ⬅️ <a href="./01-definition-and-overview.md">Previous topic: Definition &amp; Overview</a>
</p>

<p align="right">
  <a href="./03-language-levels.md">Next topic: Computer Language Levels</a> ➡️
</p>
