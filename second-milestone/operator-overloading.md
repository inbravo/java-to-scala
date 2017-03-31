| Topic | Operator Overloading |
| :--- | :--- |
| Time required | 10 minutes |
| Benefit realized | Benefit of operator overloading in Scala |
| Git sample | [OperatorsAreMethods.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/OperatorsAreMethods.scala) |

---

* Unlike Java, you can overload operators in Scala
* All operators do the usual work \(`+ - * / % & | ^ >> <<`\), but these operators are methods, which is owing to operator overloading feature of Scala

  * `a + b`  is a shorthand for `a.+(b)`
  * If a & b are type of Int, method '**+'** of Int class will applied on operation: `a.+(b)`

* Open program `com.inbravo.lang.OperatorsAreMethods.scala`\[[OperatorsAreMethods.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/OperatorsAreMethods.scala%29\)\] in Eclipse and run...

```scala
/**
 * The + - * / % operators do their usual job, as do the bit operators & | ^ >> <<. There
 * is just one surprising aspect: These operators are actually methods : Quote from 'Scala for the Impatient'
 *
 * amit.dixit
 */
object OperatorsAreMethods {

  def main(args: Array[String]): Unit = {

    val a = "a"
    val b = "b"

    /* '+' is nothing but just a method implemented in String class */
    println(a.+(b))

    /* a + b == a.+(b) */
    println(a + b)

    println(OperatorsAreMethods.+)
    println(OperatorsAreMethods.++)

    /* Both calls to same method */
    println(OperatorsAreMethods.+(1))
    println(OperatorsAreMethods + 1)

    /* Both calls to same method */
    println(OperatorsAreMethods.++(1))
    println(OperatorsAreMethods ++ 1)
  }

  def +() {
    println("+")
  }

  def +(param: Int) {
    println(param + "+")
  }

  def ++() {
    println("++")
  }

  def ++(param: Int) {
    println(param + "++")
  }
}
```



