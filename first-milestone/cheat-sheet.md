1.  The interactive shell for Scala is simply called scala. You use it by typing scala at a command prompt. Scala interpreter \(interactive “shell”\) reads an expression, evaluates it, prints it,and reads the next expression. This is called the read-eval-print loop, or **REPL**

2. you can import java Classes library in Scala program same as you can do in Java

   ```
            import java.math.BigInteger
   ```

3. Every value in Scala is an object and every operation is a method call. For example, when you say 1 + 2 in Scala, you are actually invoking a method named + defined in class Int, and 1 and 2 are objects we are passing to this method.

4. Scala’s syntax avoids some of the boilerplate that burdens Java programs.

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

