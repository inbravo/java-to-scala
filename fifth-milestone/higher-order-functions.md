| Topic | High Order Functions |
| :--- | :--- |
| Benefits realized | How High Order Functions works in Scala  	|
| Git sample 		| [HighOrderFunctionTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/HighOrderFunctionTest.scala)	|
| References		| [docs.scala-lang.org](http://docs.scala-lang.org/tutorials/tour/higher-order-functions.html)	|

---

*	A Higher-Order function is a function that does at least one of the following:
	*	Takes one or more functions as an input
    *	Outputs a function

*	In example below, there is a function: `apply` which takes another function `f` and a value `v` and applies function `f` to `v`

*	Function: `apply` consumes an `Int` and returns a `String` : `Int => String`

*	In example below, method `decorator.layout` is coerced automatically to a value of type `Int => String` as required by method `apply`

```scala

object HighOrderFunctionTest extends App {

  /* Method `apply` has two params: function `f` & value `v` and it applies `f` to `v` */
  def apply(f: Int => String, v: Int) = f(v)

  /* Create a new 'Decorator' object */
  val decorator = new Decorator("[", "]")

  /* Pass 'decorator.layout' to 'apply' */
  val layoutOutput = apply(decorator.layout, 7)

  println(layoutOutput)
}

class Decorator(left: String, right: String) {

  /* Method is bound to type 'A' */
  def layout[A](x: A) = left + x.toString() + right
}
```


