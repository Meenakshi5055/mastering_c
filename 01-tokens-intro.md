## Topic 01: Introduction to C Tokens as Building Blocks

**What is a Token?**

A token is the smallest individual unit in a C program that has meaning. When the compiler reads your code, it doesn't see full sentences — it breaks everything down into these small pieces first, and then checks whether they're arranged correctly. Think of tokens as the letters and words of a language, while a full C program is like a paragraph built from them.

**Why tokens matter:**

Before you can understand how to write correct C statements, you need to know the individual pieces those statements are made of. Every single character you type — a word, a number, a symbol — falls into one of C's token categories. Once you understand these categories, you'll be able to read any line of C code and identify what each part is doing.

Example — breaking a line into tokens:

int age = 25;

This single line is made up of 5 tokens:
| Token | Type |
|---|---|
| int | Keyword |
| age | Identifier |
| = | Operator |
| 25 | Constant |
| ; | Special Symbol |

*"The 6 types of tokens in C:**

* Keywords – reserved words with a fixed meaning (like int, if, return)
* Identifiers – names you create for variables, functions, etc. (like age, total)
* Constants – fixed values that don't change (like 25, 3.14, 'A')
* Strings – text enclosed in double quotes (like "Hello")
* Operators – symbols that perform actions (like +, =, >)
* Special Symbols – punctuation marks with special meaning (like ;, {, }, (, ))

During the **preprocessing and compilation stages**, the C compiler breaks your source code into a stream of tokens (a process called *Lexical Analysis*). Blank spaces, tabs, and comments are ignored except where they serve to separate tokens.


Each of these is covered in detail in the next topics of this module. By the end, you'll be able to look at any C program and immediately recognize every piece it's built from.



[📋 Module 02 Index](./module-02-.md) | 

[➡️ Next Topic 02: Identifiers](./02-identifiers.md)




