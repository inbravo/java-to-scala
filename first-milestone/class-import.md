| Topic | Import and Packages |
| :--- | :--- |
| Time required | 10 mins |
| Benefits realized | How class import in Scala works |
| Git sample | [ImportTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ImportTest.scala) |

---

* Scala program[ ImportTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ImportTest.scala) describes all possible class imports in Scala, which is slightly different from Java

* In Java you dont need to import classes or interfaces from package `java.lang.*`

* Similarly Scala packages  \(`scala.* , scala.Predef.*`\) along with Java lang package \(`java.lang.*`\) are not required to be explicitely imported in a Scala class

```scala
/* These imports are not required to be added explicitly */
import _root_.java.lang._
import _root_.scala._
import _root_.scala.Predef._
```

* Import some classes in Scala, using curly brackets \(`{}`\)

```scala
/* Import some classes */
import java.util.concurrent.atomic.{ AtomicInteger, AtomicLong }
```

* Import all classes of a package in Scala, using underscope character \(`_`\). Java used star character \(`*`\) for this purpose

```scala
/* Both imports are same. top package can be ignored */
import scala.math._
import math._
```

* Import statements can be anywhere inside the Scala program. Unlike Java, where imports are only allowed at top of class. The   scope of the import statement extends until the end of the enclosing block.



