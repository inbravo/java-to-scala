| Topic | Using Properties/Fields as Method/Definitions in Scala Class/Object |
| :--- | :--- |
| Git sample | [VarAndValTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/VarAndValTest.scala) |

---

* Thanks to functional nature of Scala : **`var` or `val` can be used as a `def`** 

* Focus on following three lines from program. You will see a `var`, a `val` and a `def`, actually doing same job

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



