| Topic | Variables as Definitions |
| :--- | :--- |
| Time required | 10 minutes |
| Benefit realized | How a Variable can also be used for creating a definition |
| Git sample | [VarAndValTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/VarAndValTest.scala) |

---

* **Variable or Value as function: **thanks to functional nature of Scala

* Open program`com.inbravo.lang.VarAndValTest.scala`\[[VarAndValTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/VarAndValTest.scala)\] in Eclipse and run...

* Focus on following three lines from program. You will see a `var`, `val` and `def`, actually doing same job

```scala
  /* A variable, value and definition, doing same jobs (increment of integer value) */
  var incrementVar = (x: Int) => x + 1 /* A definition using 'var' */
  val incrementVal = (x: Int) => x + 1 /* A definition using 'val' */
  def incrementDef = (x: Int) => x + 1 /* A definition using 'def' */

  /* Everyone will print '2' */
  println(incrementVar(1))
  println(incrementVal(1))
  println(incrementDef(1))
```



