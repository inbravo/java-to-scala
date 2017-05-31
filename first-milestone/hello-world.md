| Topic | Hello World |
| :--- | :--- |
| Time required | 10 minutes |
| Benefits realized | First program execution in Scala |
| Git sample | [HelloWorld.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/HelloWorld.scala) & [HelloWorldWithoutMain.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/HelloWorldWithoutMain.scala) |

---

**HelloWorld With** `main()` **Method**

* Open Scala program [HelloWorld.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/HelloWorld.scala)

```scala
object HelloWorld {

  /**
   *  Entry point of program : equivalent of Java main method
   *  Parameter passed : 'scala.Array' of 'Predef.String'
   *  Property 'scala.Predef.String' eventually calls 'java.lang.String'
   *  Scala object 'scala.Predef' is a placeholder for mostly used Scala classes
   */
  def main(args: Array[String]): Unit = {

    /* Control flow : scala.Predef.println --> scala.Console.println --> java.io.PrintStream.println */
    println("Hello World")
  }
}
```

**HelloWorld Without** `main` **Method**

* Scala provides `scala.App` class to avoid `main` method

* Open Scala program [HelloWorldWithoutMain.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/HelloWorldWithoutMain.scala)

```scala
object HelloWorldWithoutMain extends App {

  /* Control flow : scala.Predef.println --> scala.Console.println --> java.io.PrintStream.println */
  println("Hello World")
}
```



