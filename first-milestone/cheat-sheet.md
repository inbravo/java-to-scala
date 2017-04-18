1. Scala also provides another easy mechanism of executing the programs, using a comand prompt. This facility in programming is called [REPL \(Read Evaludate Print Loop\)](http://docs.scala-lang.org/overviews/repl/overview.html)

2. The interactive shell for Scala is simply called scala. You use it by typing scala at a command prompt. It starts an interactive shell, which is also called Scala interpreter, reads an expression, evaluates it, prints it, and reads the next expression. This is called the read-eval-print loop, or **REPL**

3. you can import java Classes library in Scala program same as you can do in Java

   ```
            import java.math.BigInteger
   ```

4. Every value in Scala is an object and every operation is a method call. For example, when you say 1 + 2 in Scala, you are actually invoking a method named + defined in class Int, and 1 and 2 are objects we are passing to this method.

5. Scala’s syntax avoids some of the boilerplate that burdens Java programs.

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

