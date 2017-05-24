| Topic | Using implicits to write expressive code |
| :--- | :--- |
| Git sample | [ImplicitParamTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ImplicitParamTest.scala) & [ImplicitFuncTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ImplicitFuncTest.scala) & [ImplicitClassTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ImplicitClassTest.scala) |

---

*	Scala `implicit` provides ability to write classes and methods that can be reused anytime they’re needed
*	An `implicit` keyword can be used in three ways 
	*	**Implicit Parameters**: Example below shows how method 'square' takes context bound implicit Int value '2' from the context
	```scala
	object ImplicitParamTest {

		 /* Compiler will bind 'implicit val value = 2' to the context in which they are called */
		implicit val value = 2

		/* Method 'square' call does not provides any parameter of type Int as desired in definition */
		/* If variable is 'implicit', compiler will look for a variable of type Int in the implicit scope */
		/* Compiler will find 'implicit val value = 2' and will pass value '2' while calling 'square' method */
		def main(args: Array[String]): Unit = println(square)

		def square(implicit value: Int) = value * value
	}
	```
	*	**Implicit Conversions with Classes**: Example below adds a new method `sayHello` to String class
	```scala
	object ImplicitClassTest {

	  def main(args: Array[String]): Unit = {

		/* Create new variable 'name' */
		val name = "InBravo"

		/* See carefully that 'sayHello' does not belong to original Predef.String */
		println(name.sayHello)
	  }

	  /* Implicit class with a method 'sayHello'. A constructor parameter is must for any implicit class */
	  implicit class Greeter(val name: String) {

		/* All the methods of any implicit class are bound to context */
		def sayHello = "Hello " + name;
	  }
	}
	```
	*	**Implicit conversions using functions**:	
