## Topic_5 Logic building: Algorithm, Pseudo code, Flowchart.

Before writing real C code, it's important to plan how a program should solve a problem. This planning stage uses three tools: *Algorithm, Pseudocode, and Flowchart.*

**Algorithm:**

An algorithm is a step-by-step method to solve a problem. It's a clear set of instructions that, when followed in order, always ends with a result.
*Properties every algorithm must have:*
* Finiteness – It must end after a fixed number of steps (it can't run forever).
* Definiteness – Every step must be clear and mean exactly one thing (no confusion).
* Input – It can take zero or more inputs.
* Output – It must produce at least one output.
* Effectiveness – Every step must be simple enough to actually be carried out.

*Example:* Algorithm to find the average of three numbers.

> * Start
> * Let a, b, c be three numbers
> * Display the message "Enter any three integers"
> * Read three integers and store them in a, b, c
> * Compute avg = (a + b + c) / 3.0
> * Display "The average is: avg"
> * End

**Pseudocode:**

Pseudocode is a way of writing the logic of a program using plain, everyday English, instead of real programming syntax. It helps a programmer plan the logic before worrying about a specific language's rules.

*Example:* Pseudocode to check pass/fail based on average marks.

> * Input a set of 4 marks
> * Calculate their average by summing and dividing by 4
> * If average is below 50
> * print "Fail"
> * else
> * print "Pass"

**Flowchart:**

A flowchart is a picture (diagram) that shows an algorithm's steps and their order, using standard shapes connected by arrows.

*Why flowcharts are useful:*

* They make it easier to understand a program's logic at a glance.
* Different shapes represent different types of actions, so the flow of the program is easy to follow visually.

*Standard flowchart symbols:*

| Symbol Name | Actual Visual Shape | Purpose / Description |
| :--- | :---: | :--- |
| **Flow Lines** | ➡️ ⬇️ | Connects symbols and shows direction. |
| **Terminal Symbol** | 🛑 *(Oval)* | Indicates the **Start** or **End** of a flowchart. |
| **Input / Output** | ▰ *(Parallelogram)* | Used for reading inputs (`Read`) or printing outputs (`Print`). |
| **Process Symbol** | ▭ *(Rectangle)* | Used for calculations and operations (e.g., `a = b + c`). |
| **Decision Symbol** | 🔷 *(Diamond)* | Represents a true/false or yes/no question. |
| **Connectors** | ⚪ *(Circle)* | Connects different parts of a long flowchart together. |
----

[⬅️ Previous Topic:04-advantages-disadvantages.md](./04-advantages-disadvantages.md) |

 [➡️ Next Topic:06-compiler-setup.md](./06-compiler-setup.md)
