| Topic | Hello World |
| :--- | :--- |
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
* To print the value on console you can use print : `print("Hello World")`

* To print the value on console in a new line you can use println  `println("Hello World")`

* To print the formatted value use `printf` \(like C\) `printf("Hello, %s! You are %d years old.\n", "John", 32)`

* Read a line of input from the console with the `readLine`function.

* To read a specific value, use specific methods in Scala class [scala.io.StdIn](http://www.scala-lang.org/api/current/scala/io/StdIn$.html)

```scala
  scala.io.StdIn.readInt
  scala.io.StdIn.readChar
  scala.io.StdIn.readBoolean
  scala.io.StdIn.readDouble
  scala.io.StdIn.readFloat
  scala.io.StdIn.readLong
  scala.io.StdIn.readShort
```

* With `readLine`method you can pass string before input: `val name = scala.io.StdIn.readLine("Your name: ")`

* These methods assume, next input line as a single number, without leading or trailing whitespace, else NumberFormatException occurs
