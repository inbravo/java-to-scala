| Topic | Trait, Class and Object |
| :--- | :--- |
| Git sample | [ClassObjectTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ClassObjectTest.scala) & [PrimaryConstructorTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/PrimaryConstructorTest.scala) & [ImportTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ImportTest.scala) & [ObjectPrivateAccess.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ObjectPrivateAccess.scala)|

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

* Class is the **Blueprint **for objects and Object is the **Entry Point** of a program

* Read more from [StackOverflow](http://stackoverflow.com/questions/1755345/difference-between-object-and-class-in-scala)

* Scala allows you to pass field variables along with constructor
* Open program [PrimaryConstructorTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/PrimaryConstructorTest.scala) and run

```scala
/* Params of the constructor turn into fields and initialized with the construction parameters */
class Employee(val name: String, val age: Int) {/* Do something */}
```

* Above Scala program is equivalent to below given Java program. You can see how much verbose Java is,

```java
/* Equivalent Java class */
class Employee { 

      private String name;
      private int age;

      public Person(String name, int age) {

          this.name = name;
          this.age = age;
      }

      public String name() { 
          return this.name; 
      }

      public int age() { 
          return this.age; 
     }
}
```

* Scala program [ImportTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ImportTest.scala) describes all possible class imports in Scala, which is slightly different from Java

* In Java you dont need to import classes or interfaces from package `java.lang.*`. Similarly Scala packages  \(`scala.* , scala.Predef.*`\) along with Java lang package \(`java.lang.*`\) are not required to be explicitely imported in a Scala class

```scala
/* These imports are not required to be added explicitly */
import _root_.java.lang._
import _root_.scala._
import _root_.scala.Predef._
```

* Import some classes in Scala, using curly brackets \(`{}`\)

```scala
/* Import some classes */
import java.util.concurrent.atomic.{ AtomicInteger, AtomicLong }
```

* Import all classes of a package in Scala, using underscope character \(`_`\). Java used star character \(`*`\) for this purpose

```scala
/* Both imports are same. top package can be ignored */
import scala.math._
import math._
```

* Import statements can be anywhere inside the Scala program. Unlike Java, where imports are only allowed at top of class. The scope of the import statement extends until the end of the enclosing block.

* Access modifiers in Scala can be augmented with qualifiers. A modifier  of the form `private\[X\]` or `protected\[X\]` means that access is private or protected up-to X, where X designates some enclosing package, class or singleton object

* Difference between `private` and `private[this]` 

```scala
class EmployeeManager(employeeManager: EmployeeManager) {

    /* Only accesible to 'this' */
    private[this] val privateEmployeeManagerValue = 2

    println(this.privateEmployeeManagerValue)
    
    /* This line will give compilation error */
    //  println(employeeManager.privateEmployeeManagerValue) 
  }
```

* If you have some helper method you’d like to be in scope for an entire package, go ahead and put it right at the top level of the
   package. These are called `_package` `objects._`
