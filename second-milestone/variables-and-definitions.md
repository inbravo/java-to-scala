| Topic | Variables as Definitions |
| :--- | :--- |
| Time required | 10 minutes |
| Benefit realized | How a Variable can also be used for creating a definition |
| Git sample | [VarAndValTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/VarAndValTest.scala)  |

---

* **Variable or Value as function: **thanks to functional nature of Scala

* Focus on following two lines from program. You will see a `var`, `val` and `def`, actually doing same job

```scala
  /* A variable, value and definition, doing same jobs (increment of integer value) */
  var incrementVar = (x: Int) => x + 1 /* A definition using 'var' */
  val incrementVal = (x: Int) => x + 1 /* A definition using 'val' */
  def incrementDef = (x: Int) => x + 1 /* A definition using 'def' */
```



