# 🌱 Topic 01: Introduction to C Tokens

> Welcome to the first topic of Module 02!  
> Before we build complete C programs, we need to understand the small pieces that make them possible.

---

## 🌼 What Is a Token?

A **token** is the smallest meaningful unit in a C program.

When you write C code, the compiler does not understand the entire program as one large sentence. Instead, it reads the code as a collection of smaller pieces.

These meaningful pieces are called **tokens**.

You can think of tokens as the vocabulary of the C language:

- Words such as `int` and `return`
- Names such as `age` and `total`
- Numbers such as `25` and `3.14`
- Text such as `"Hello"`
- Symbols such as `+`, `=`, and `;`

Together, these pieces form C expressions, statements, functions, and complete programs.

---

## 💡 Why Are Tokens Important?

Understanding tokens helps you read C code more comfortably.

When you see a statement such as:

```c
int age = 25;
```

you can recognize that it is not one mysterious line. It is a small collection of meaningful parts:

```text
int   age   =   25   ;
```

Each part has a different purpose.

Once you can recognize these pieces, C programs become easier to understand, write, and debug.

---

## 🧩 A Simple Example

Consider this statement:

```c
int age = 25;
```

This statement contains **five tokens**:

| Token | Type | What it does |
|---|---|---|
| `int` | Keyword | Tells C that `age` will store an integer |
| `age` | Identifier | The name selected for the variable |
| `=` | Operator | Assigns a value |
| `25` | Integer constant | The value stored in `age` |
| `;` | Special symbol / punctuator | Marks the end of the statement |

The semicolon is important because it tells the compiler:

> This statement is complete.

---

## 🌈 The Six Main Types of C Tokens

C tokens are commonly grouped into six categories.

| Category | Example | Meaning |
|---|---|---|
| 🔑 **Keywords** | `int`, `if`, `return` | Reserved words with a fixed meaning |
| 🏷️ **Identifiers** | `age`, `total`, `main` | Names created by the programmer |
| 🔢 **Constants** | `25`, `3.14`, `'A'` | Fixed values |
| 💬 **String literals** | `"Hello"` | Text enclosed in double quotation marks |
| 🧮 **Operators** | `+`, `=`, `>`, `==` | Symbols that perform operations |
| ✳️ **Special symbols / punctuators** | `;`, `{`, `}`, `(`, `)` | Symbols that organize the structure of a program |

> 🌼 **Small vocabulary note:**  
> In standard C terminology, many “special symbols” are called **punctuators**. We will use both names when helpful.

---

## 🔍 Looking at a Complete Example

Now let us examine a slightly larger example:

```c
int age = 20;
printf("Age: %d\\n", age);
return 0;
```

| Token | Type | Explanation |
|---|---|---|
| `int` | Keyword | Defines an integer data type |
| `age` | Identifier | Name of a variable |
| `=` | Operator | Assigns a value |
| `20` | Integer constant | A fixed whole-number value |
| `;` | Special symbol | Ends the declaration |
| `printf` | Identifier | Name of a library function |
| `(` and `)` | Special symbols | Enclose function arguments |
| `"Age: %d\\n"` | String literal | Text and formatting instructions |
| `,` | Special symbol | Separates function arguments |
| `return` | Keyword | Sends a value back from a function |
| `0` | Integer constant | Indicates successful completion |
| `;` | Special symbol | Ends the statement |

Notice how different types of tokens work together to create understandable instructions.

---

## 🎨 Constants and String Literals Are Different

Beginners often confuse constants and strings.

```c
25
```

This is an integer constant.

```c
3.14
```

This is a floating-point constant.

```c
'A'
```

This is a character constant.

```c
"Hello"
```

This is a string literal.

The quotation marks are important:

- `'A'` represents one character.
- `"A"` represents a string containing one character.

They look similar, but they are not the same kind of token.

---

## 🌿 How the Compiler Sees Your Code

During the early stages of compilation, the compiler processes your source code and recognizes its tokens. This process is called **lexical analysis**.

For example:

```c
int count = 10;
```

The compiler recognizes:

```text
[int] [count] [=] [10] [;]
```

Spaces and line breaks usually help humans read the program, but they are not normally treated as meaningful tokens.

Comments are also ignored when the compiler creates the final program:

```c
// This comment explains the next line
int count = 10;
```

The comment helps the programmer, but it does not become part of the program's instructions.

---

## 💭 A Friendly Way to Remember Tokens

Think of a C program as a sentence:

| C language | Human language |
|---|---|
| Keyword | A grammar word |
| Identifier | A name |
| Constant | A value |
| String literal | A piece of text |
| Operator | An action word or symbol |
| Punctuator | Punctuation |

Just as sentences need words and punctuation, C programs need tokens.

---

## 🌼 Remember

- A token is a meaningful unit of a C program.
- C programs are built from different categories of tokens.
- Keywords have fixed meanings and cannot be used as ordinary names.
- Identifiers are names created by the programmer.
- Constants represent fixed values.
- String literals contain text inside double quotation marks.
- Operators perform actions such as assignment or addition.
- Special symbols, also called punctuators, organize program structure.
- Spaces, tabs, and comments mainly help humans read the code.

---

## 🌈 Topic Summary

A C program may look complicated at first, but it is built from small, understandable pieces.

When you learn to recognize tokens, you can begin to read C code step by step instead of seeing it as one large block of symbols.

In the next topic, we will explore **identifiers** and learn how to create valid names for variables and functions.

---

[📋 Back to Module 02 Index](./module-02.md) | [➡️ Next Topic 02: Identifiers](./02-identifiers.md)
