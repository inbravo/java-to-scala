| Topic | Input and Output |
| :--- | :--- |
| Time required | 10 mins |
| Benefit | How to send or recieve data from console |
| Git sample |  |

---

* To print the value on console you can use print : `print("What is your age? ")`

* To print the value on console in a new line you can use println  `println("what is your age?")`

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
* These methods assume that the next input line contains a single
   number, without leading or trailing whitespace. Otherwise, a
   NumberFormatException occurs.
* To Read from file you need to`import scala.io.Source`



