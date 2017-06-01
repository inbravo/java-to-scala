| Topic | Procedures |
| :--- | :--- |
| Git sample | [ProcedureTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ProcedureTest.scala) |

---

* Open program [ProcedureTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ProcedureTest.scala)

```scala
/* Look carefully: there is no '=' */
def box(s : String) { 

    val border = "-" * s.length + "--\n"
    println(border + "|" + s + "|\n" + border)
}
```
* A procedure is a Scala method or definition which **Returns No Value**. Because the procedure doesn’t return any value, It lacks equal(`=`) symbol

* If the function body is enclosed in braces without a preceding = symbol, then the return type is `Unit`

* Best is to always use `Unit`in cases where no return type

```scala
def box(s : String): Unit = {

}
```
