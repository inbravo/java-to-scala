| Topic | Operator as Functions and Object as Functions |
| :--- | :--- |
| Git sample | [OperatorsAreMethods.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/OperatorsAreMethods.scala) <br/> [ObjectExtractorTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ObjectExtractorTest.scala) |
| References | [docs.scala-lang.org](http://docs.scala-lang.org/tutorials/tour/extractor-objects.html) <br/> [java-lang.org](http://www.scala-lang.org/old/node/112) <br/> [blog.jayway.com](https://blog.jayway.com/2011/10/11/injectors-and-extractors-in-scala) |

---

## Operators as Functions

*	Unlike Java, you can treat operators as functions (operator overloading) in Scala

*	Every value in Scala is an **Object** and every operation is a **Method Call**. For example, when you say `1 + 2` in Scala, you are actually invoking a method named `+` defined in class Int, and 1 and 2 are objects we are passing to this method

*	All operators do the usual work \(`+ - * / % & | ^ >> <<`\), but these operators are methods, which is owing to operator overloading feature of Scala

*	**`a + b`**  is a shorthand for **`a.+(b)`**

*	If a & b are type of Int, method **'+'** of Int class will applied on operation: **`a.+(b)`**

## Objects as Functions with the help of `apply` and `unapply` methods

*	Scala provides `apply` and `unapply`. Methods `apply` and `unapply` are not opposites of each other. Indeed, if you define one on a class/object, you don't have to define the other

*	Method `apply` is probably the easier to explain. When you treat your object like a function, apply is called, so Scala turns `obj(a, b, c)` to `obj.apply(a, b, c)`

```scala
/* Various ways to create customer id from customer name */
object CustomerId {

  /* Apply method helps in constructor calls */
  def apply(name: String) = "ID-" + name
  def apply(id: Int) = id
  def apply(id: Long) = id.intValue
  def apply(id: Double) = id.intValue
}

  /* Object as function */
  /* Will call 'apply(name: String)' */
  println(CustomerId("Amit"))

  /* Will call 'apply(id: Int)' */
  println(CustomerId(100))

  /* Will call 'apply(id: Long)' */
  println(CustomerId(100L))

  /* Will call 'apply(id: Double)' */
  println(CustomerId(1000.0)
```

* The `apply` method takes some arguments and yields an element of a given set. This method is called an **Injector**
*	The `unapply` method is called **Extractor** because it takes an element of the same set and extracts some of its parts

```scala
object IPAddress {

  /* The 'apply' method takes some arguments and yields an element of a given set. This method is called an injection */
  def apply(a: String, b: String, c: String, d: String): String = a + "." + b + "." + c + "." + d

  /* The 'unapply' method is called extractor because it takes an element of the same set and extracts some of its parts */
  def unapply(ip: String): Option[(String, String, String, String)] = {

    val tokens = ip split "\\."
    if (tokens.length == 4 && isValid(tokens)) Some(tokens(0), tokens(1), tokens(2), tokens(3)) else None
  }
}

object ObjectExtractorTest extends App {

  /* Different types of ip addresses */
  val ip = "127.0.0.1"
  val nonIP = "128.-112.ABC."

  /* Pattern matching calls 'IPAddress.unapply(ip)' */
  ip match {
    case IPAddress(_, _, _, a) => println(a)
    case _                     => println("Invalid ip address")
  }

  /* Pattern matching calls 'IPAddress.unapply(nonIP)' */
  nonIP match {
    case IPAddress(_, _, _, a) => println(a)
    case _                     => println("Invalid ip address")
  }
}
```

* For more information
