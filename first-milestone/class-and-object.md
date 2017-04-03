| Topic | Class and Object |
| :--- | :--- |
| Time required | 10 minutes |
| Benefit realized | Benefits of Object in Scala |
| Git sample |  |

---

* You can think of the `object`keyword as creating a [singleton](http://en.wikipedia.org/wiki/Singleton_pattern) object of a class that is defined implicitly. Example

```scala
object A extends B with C {
  def f(x: Any): Any = ???
}
```

* Declaration in above example,

  * declares an anonymous \(inaccessible\) class `A` that extends both `B`and `C` and

  * creates a single instance of this class named `A`

* Class is the **Blueprint **for objects 
* Object is the **Entry Point** of a program



