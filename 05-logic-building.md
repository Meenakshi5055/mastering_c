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

| Symbol Name | Visual Shape | Purpose / Description |
| :--- | :--- | :--- |
| **Flow Lines** | `→` `←` `↑` `↓` | Connects symbols and shows direction of flow. |
| **Terminal Symbol** | `([ Start / End ])` | Represents the start or end point of a process. |
| **Input / Output Symbol** | `[/ Read / Write /]` | Represents inputting data or outputting results. |
| **Process Symbol** | `[ Calculations ]` | Represents calculations and variable initializations. |
| **Decision Symbol** | `{ Yes / No ? }` | Represents a decision point (branching paths). |
| **Connectors** | `(( O ))` | Connects different sections of a flowchart. |

---

### Interactive Flowchart Diagram: Even or Odd Check

> *GitHub automatically renders the diagram below into visual shapes and arrows:*

```mermaid
flowchart TD
    A([Start]) --> B[/Read num/]
    B --> C{num % 2 == 0}
    C -- Yes --> D[/Print num is Even/]
    C -- No --> E[/Print num is Odd/]
    D --> F([End])
    E --> F([End])
