1. Scala provides an interactive shell, called **Scala Interpreter,** which reads an expression, evaluates it, prints it, and reads the next expression. This is called [REPL \(Read Evaludate Print Loop\)](http://docs.scala-lang.org/overviews/repl/overview.html). Refer [here ](http://alvinalexander.com/scala/getting-started-scala-repl-command-line-shell-options)to explore, will be helpfull in learning

2. Scala program [HelloWorld.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/HelloWorld.scala), which uses`main()`

3. Scala program [HelloWorldWithoutMain.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/HelloWorldWithoutMain.scala), which is without`main()`

4. Scala program [ClassObjectTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ClassObjectTest.scala) helps in understanding,

   1. A Scala trait is equivalant to Java interface

   2. A Scala class is equivalent to Java class

   3. A Scala object is equivalent to Singleton Java Class

5. Class import in Scala program is similar to Java. You are free to import any Java class in your Scala program

6. Program[ ImportTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ImportTest.scala) describes class imports in Scala

7. Program [PrimaryConstructorTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/PrimaryConstructorTest.scala) describes passing values using constructors in Scala

8. Scala dont have static, which is very popular in Java. Scala program [CompanionObjectTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/CompanionObjectTest.scala) helps in understanding how Companion Objects can help in replicating static in Scala

9. Scala syntax avoids some of the boilerplate that burdens Java programs. In Scala, you can define a class using `class Employee(name: String, age: String){}`. Same in Java requires...

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



