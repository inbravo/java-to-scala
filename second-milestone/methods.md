| Topic | Methods |
| :--- | :--- |
| Time required | 30 minutes |
| Benefit realized | Ability to define properties and fields |
| Git sample | [MethodTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/MethodTest.scala) |

---

* Scala provides keyword `def`for creating methods or definitions

```scala
def incrementDef = (x: Int) => x + 1 /* A definition using 'def' */
```

* Declare a method which takes no parameter and returns nothing but prints 'Hello''

```scala
def print = println(value)
```

* Notice that unlike Java, you can ignore curly brackets \(`{ ... }`\) while defining Scala methods

```scala
def print = { println(value) }
```

* Declare a method which take a parameter and returns nothing but prints the passed `Int` value

```scala
def printIt(value: Int) = println(value)
```

* Declare a method which take no parameter and returns something

```scala
/* Method returns Int value '1' */
def returnInt = 1

/* Method returns Float value '1.0' */
def returnFloat = 1.0

/* Another way to explicitly define return type (method-name:type) for methods */
def returnInt: Int = return 1
def returnFloat: Float = return 1.0F
```

* Open program `com.inbravo.lang.MethodTest.scala`\[[MethodTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/MethodTest.scala%29%29\)\] in Eclipse and run...

```scala
/**
 * A complete example to understand; how to define methods in Scala
 *
 * amit.dixit
 */
object MethodTest extends App {

  /* Anonymous method; this does not require an explicit calls but will be automatically called */
  print("Hello")

  /* A method with a name, without any parameter passed, with curly brackets ('{}'); which prints something */
  def printHelloWithCurlyBrackets = { print("Hello") }

  /* A method with a name, without any parameter passed, without curly brackets ('{}'); which prints something */
  def printHello = print("Hello")

  /* A method with a name but without curly brackets ('{}'); which prints something */
  def printIt(value: Int) = print(value)

  /* A method which returns an Int value */
  def returnInt: Int = return 1

  /* A method which returns an Int value without using 'return' keyword */
  def returnIntWithoutTypeDefinition = 1

  /* A method which returns a Float value */
  def returnFloat: Float = return 1.0F

  /* A method which returns a Float value without using 'return' keyword */
  def returnFloatWithoutTypeDefinition = 1.0F

  /* Run all methods */
  print(printHelloWithCurlyBrackets)
  print(printHello)
  print(returnInt)
  print(returnIntWithoutTypeDefinition)
  print(returnFloat)
  print(returnFloatWithoutTypeDefinition)

  /* Watch parenthesis '()' is only required where a method parameter need to be passed */
  print(printIt(1))
}
```



