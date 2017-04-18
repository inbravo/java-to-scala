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
  class Employee(val name: String, val age: Int) {

  }
```

* Parameters of the primary constructor turn into fields that are initialized with the construction parameters



