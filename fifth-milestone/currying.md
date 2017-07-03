| Topic | Common types in Scala |
| :--- | :--- |
| Git sample | [CurryingTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/CurryingTest.scala)	|
| References | [docs.scala-lang.org](http://docs.scala-lang.org/tutorials/tour/currying.html)	 |

---

* Currying, invented by Moses Schönfinkel and Gottlob Frege, is the technique of transforming a **Function of Multiple Arguments** into a **Function of Single Argument** (other arguments having been specified by the curry)

*	When a method is called with a fewer number of parameter lists, then this will yield a function taking the missing parameter lists as its arguments

```scala
object CurryingTest extends App {

  /* 	A method without currying	*/
  def sum(x: Int, y: Int) = x + y

  println("Sum : " + sum(1, 2))
  println("Sum : " + sum(1, 3))

  /* 	A method using currying	*/
  /* 	Redefines the sum method so that it takes only a single 'Int' as a parameter and returns a 'Clozure' as a result	*/
  /*	Main program calls this 'Closure', and passes second 'parameter'. This 'Clozure' computes the value and returns the final result	*/
  def curriedSum(x: Int) = { (y: Int) => x + y }

  println("CurriedSum: " + curriedSum(1)(2))
  println("CurriedSum: " + curriedSum(1)(3))

  /* Clarification how 'Clozure', returned by 'curriedSum' works */
  val clozure = curriedSum(1)

  println("Clozure: " + clozure(2))
  println("Clozure: " + clozure(3))

  /* 	Another improved method using currying	*/
  def anotherCurriedSum(x: Int)(y: Int) = x + y

  println("anotherCurriedSum: " + anotherCurriedSum(1)(2))
  println("anotherCurriedSum: " + anotherCurriedSum(1)(3))
}
```



