| Topic | Constructors |
| :--- | :--- |
| Time required | 10 mins |
| Benefit realized | How Scala constructors works |
| Git sample | [PrimaryConstructorTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/PrimaryConstructorTest.scala) |

---

* Scala is brief, thanks to its functional nature
* Scala allows you to pass field variables along with class definition statement
* Open program [PrimaryConstructorTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/PrimaryConstructorTest.scala) in your Eclipse and run...

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



