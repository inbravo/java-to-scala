| Topic | Hello World |
| :--- | :--- |
| Time required | 5 minutes |
| Benefits realized | First program execution in Scala |
| Git sample | [HelloWorld.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/HelloWorld.scala) |

---

* Open Scala program `com.inbravo.lang.HelloWorld.scala` in your Eclipse. 
* Right click on program --&gt; Run As --&gt; Scala Application. Program will print '**Hello World' **on console.

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



