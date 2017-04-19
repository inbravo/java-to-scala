| Topic | Reasoning with if-else |
| :--- | :--- |
| Time required | 10 mins |
| Benefit | How logical if-else statements used in Scala |
| Git sample |  |

---

* Scala `if-else` logic is almost similar with Java

* Scala `if-else` statements returns a value, which is different from Java. Example`var maxoftwo = if(x>y) x else`

* In cases, where `else` part if not defined in `if-else` statement, return type would be `Any`

  ```scala
  /* In below statement 'else' is not defined so the return type would be 'Any' */
  val result = if(a%2) return "even"

  /* Return type will be Java.lang.String */
  val result = if(a%2) return "even" else "odd"
  ```

* An `if` statement without an `else`is  equivalent to `if (x > 0) 1 else ()`



