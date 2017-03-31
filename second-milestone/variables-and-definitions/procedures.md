| Topic | Procesures |
| :--- | :--- |
| Time Required | 10 minutes |
| Benefit realized | How procedure is different from definition |
| Git sample | [ProcedureTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ProcedureTest.scala) |

---

* A procedure is a definition which returns no value

* Open program`com.inbravo.lang.ProcedureTest.scala`\[[ProcedureTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ProcedureTest.scala)\] in Eclipse and run...

```scala
package com.inbravo.lang

/**
 * A function without a return type
 * amit.dixit
 */
object ProcedureTest {

  def main(args: Array[String]): Unit = {

    hello; box("I am a poor human")
  }

  /* A function without a Return Type is called Procedure. Look carefully: there is no '=' */
  def box(s: String) {

    val border = "-" * s.length + "--\n"
    println(border + "|" + s + "|\n" + border)
  }

  /* A function without a Return Type is called Procedure. Just print a 'Hello' */
  def hello = print("Hello")
}
```

* Because the procedure doesn’t return any value, you can avoid the = symbol

```scala
/* Look carefully: there is no '=' */
def box(s : String) { 

    val border = "-" * s.length + "--\n"
    println(border + "|" + s + "|\n" + border)
}
```

* If the function body is enclosed in braces without a preceding = symbol, then the return type is `Unit`
* Best is to always use `Unit`in cases where no return type

```scala
def box(s : String): Unit = {

}
```



