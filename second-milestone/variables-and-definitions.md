|  |  |
| :--- | :--- |
|  |  |

---

* **Variable or Value as function: **thanks to functional nature of Scala

* Focus on following two lines from program. You will see a `var`, `val` and `def`, actually doing same job

```scala
  /* A variable, value and definition, doing same jobs (increment of integer value) */
  var incrementVar = (x: Int) => x + 1 /* A definition using 'var' */
  val incrementVal = (x: Int) => x + 1 /* A definition using 'val' */
  def incrementDef = (x: Int) => x + 1 /* A definition using 'def' */
```



