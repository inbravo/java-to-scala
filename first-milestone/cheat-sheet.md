1. The interactive shell for Scala is simply called scala. You use it by typing `scala`at a command prompt. It starts an interactive shell, which is called **Scala Interpreter,** which reads an expression, evaluates it, prints it, and reads the next expression. This is called [REPL \(Read Evaludate Print Loop\)](http://docs.scala-lang.org/overviews/repl/overview.html)

2. Class import  in Scala program is similar to Java. You are free to import any Java class in your Scala program

   ```scala
   import java.math.BigInteger
   ```

3. Scala’s syntax avoids some of the boilerplate that burdens Java programs.

   // this is Java class

`MyClass {`

`private int index;`

`private String name;`

`public MyClass(int index, String name) {`

`this.index = index; this.name = name;`

`}`

`}`

In Scala, you would likely write this instead:

`class MyClass(index: Int, name: String)`

