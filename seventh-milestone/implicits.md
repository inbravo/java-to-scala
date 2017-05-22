| Topic | Using implicits to write expressive code |
| :--- | :--- |
| Git sample | [ImplicitParamTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ImplicitParamTest.scala) & [ImplicitFuncTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ImplicitFuncTest.scala) & [ImplicitClassTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ImplicitClassTest.scala) |

---

*	Scala provides an `implicit` keyword that can be used in three ways: 
	*	Implicit parameters: implicit values will be taken from the context and passed in implicit methods
	```scala
	object ImplicitParamTest {

		implicit val value = 2

		/* Method 'square' call does not provides any parameter of type Int as desired in definition */
		/* If variable is 'implicit', compiler will look for a variable of type Int in the implicit scope */
		/* Compiler will find 'implicit val value = 2' and will pass value '2' while calling 'square' method */
		def main(args: Array[String]): Unit = println(square)

		def square(implicit value: Int) = value * value
	}
	```
	*	Implicit class: Add new functions to closed classes. Example below adds a new method `sayHello` to String class
	```scala
	object ImplicitClassTest {

	  def main(args: Array[String]): Unit = {

		/* Create new variable 'name' */
		val name = "InBravo"

		/* Call method 'sayHello' using implicit method call */
		/* See carefully that 'sayHello' does not belong to original Predef.String. With the help of implicit, it sounds like addition to String class */
		println(name.sayHello)
	  }

	  /* Implicit class with a method 'sayHello' */
	  implicit class Greeter(val name: String) {

		def sayHello = "Hello " + name;
	  }
	}
	```
	*	Implicit conversions using functions:
