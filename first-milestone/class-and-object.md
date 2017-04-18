| Topic | Class and Object |
| :--- | :--- |
| Time required | 10 minutes |
| Benefit realized | What  is keyword object in Scala and its purpose |
| Git sample |  |

---

* Scala provides two ways of defining a program `class `and `object`
* Scala keyword `class `is used in similar fashion, the way used in Java
* You can think of Scala keyword `object`as creating a [singleton](http://en.wikipedia.org/wiki/Singleton_pattern) object of a class that is defined implicitly. Example

```scala
object A extends B with C {
  def f(x: Any): Any = ???
}
```

* Declaration in above example,

  * Declares an anonymous \(inaccessible\) class `A` that extends both `B`and `C` and

  * Creates a single instance of this class named `A`

* Class is the **Blueprint **for objects

* Object is the **Entry Point** of a program

* Read more from [StackOverflow](http://stackoverflow.com/questions/1755345/difference-between-object-and-class-in-scala)



