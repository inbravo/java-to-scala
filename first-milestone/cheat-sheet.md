1. The interactive shell for Scala is simply called scala. You use it by typing `scala`at a command prompt. It starts an interactive shell, which is called **Scala Interpreter,** which reads an expression, evaluates it, prints it, and reads the next expression. This is called [REPL \(Read Evaludate Print Loop\)](http://docs.scala-lang.org/overviews/repl/overview.html)

2. Scala program [HelloWorld.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/HelloWorld.scala), which uses`main()`

3. Scala program [HelloWorldWithoutMain.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/HelloWorldWithoutMain.scala), which is without` main()`

4. Class import  in Scala program is similar to Java. You are free to import any Java class in your Scala program

5. Scala’s syntax avoids some of the boilerplate that burdens Java programs. In Scala, you can define a class using `class Employee(name: String, age: String){}`. Same in Java requires...

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



