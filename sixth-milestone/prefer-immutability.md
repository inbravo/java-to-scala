| Topic | Prefer Immutability|
| :--- | :--- |
| Git sample |  |

---
*	Most of the mainstream languages, including object-oriented programming languages such as C#, Visual Basic, C++, and Java, were designed to primarily support Imperative (procedural) Programming
*	Imperative code tends to be made of statements, not expressions
*	Objects are created with an initial state. Then statements are executed that Mutate or Change the state of an object
*	Immutability, in programming, refers to the unchanging state of objects after construction. Scala prefers immutability in design, making it the default in many cases
*	Defining a variable as a val means that it’s an **Immutable** reference
*	All method parameters are **Immutable** references and class arguments default to being **Immutable** references
*	**The only way to create a mutable variable is through the `var` syntax**
