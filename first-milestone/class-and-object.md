| Topic | Trait, Class and Object |
| :--- | :--- |
| Time required | 10 minutes |
| Benefit realized | Trait, Class and Object in Scala |
| Git sample | [ClassObjectTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ClassObjectTest.scala) |

---

* Java has got `interface`, likewise Scala has got `trait`

```scala
/* A simple trait, which is like Java interface */
trait Printer {

  /* A method contract only without definition */
  def print(statement: String): Unit
}
```

* Scala provides two ways of defining a program, using either keword `class` or `object`
* Scala keyword `class`is used in similar fashion, the way used in Java

```scala
/* Definition of CLASSA, which is extending CLASSB */
class CLASSA extends CLASSB {

  /* Method returns nothing but calls super class method */
  def print: Unit = super.print("Hello")
}

/* Definition of CLASSB */
class CLASSB extends Printer {

  /* Method returns nothing but prints the statement */
  def print(statement: String): Unit = println(statement)
}
```

* Declaration in above example: Declares two classes `CLASSA`& `CLASSB`

* You can think of Scala keyword `object`as creating a [singleton](http://en.wikipedia.org/wiki/Singleton_pattern) object of a class that is defined implicitly. Example

```scala
object OBJECTA extends CLASSA {

  def main(args: Array[String]): Unit = {

    /* Call printHello. Point to be noted here is that it sounds like a Java static method call */
    OBJECTA.printHello
  }

  /* Method returns nothing but prints string 'Hello' */
  def printHello: Unit = super.print
}
```

* Declaration in above example,

  * Declares an anonymous \(inaccessible\) class `OBJECTA`

  * Creates a single instance of this class named `OBJECTA`

* Class is the **Blueprint **for objects

* Object is the **Entry Point** of a program

* One difference between classes and singleton objects is that singleton   objects cannot take parameters, whereas classes can. Because you can’t instantiate   a singleton object with the new keyword, you have no way to pass   parameters to it.

* Scala provides a trait, scala.Application, which u can extends by writing "extend Application" after the singleton object, and you can directly write the code under { }, without main def.

* Read more from [StackOverflow](http://stackoverflow.com/questions/1755345/difference-between-object-and-class-in-scala)



