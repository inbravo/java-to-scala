| Topic | Values and variables |
| :--- | :--- |
| Time required | 15 minutes |
| Benefit realized | Ability to define properties and fields |
| Git sample\(s\) | [VarAndValTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/VarAndValTest.scala) & [LazyValTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/LazyValTest.scala) |

---

* Open program`com.inbravo.lang.VarAndValTest.scala`\[[VarAndValTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/VarAndValTest.scala)\] in Eclipse and run...

* To declare a variable, use `var`

```scala
/* Without type */
var variable = 0

/* With type */
var variableWithType: Int = 10
```

* To declare a constant, use `val`

```scala
/* Without type */
val value= 8 * 5 + 2

/* With type */
val valueWithType: Int = 10 * 5 + 2
```

* All **val **type variables are initialized before utilization. A Scala `val`is a `public static final` in Java

* If you want to defer this process of initiailization untill actuall utlization, use `lazy val`

```scala
/* Lazy value without type */
lazy val lazyValue = 100

/* Lazy value with type */
lazy val lazyValueWithType: Int = 100
```

* Open program `com.inbravo.lang.LazyValTest.scala`\[[LazyValTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/LazyValTest.scala)\] in Eclipse and run...

* Scala provides keyword `def`for creating methods or definitions

```scala
def incrementDef = (x: Int) => x + 1 /* A definition using 'def' */
```

* **Variable or Value as function: **thanks to functional nature of Scala

* Focus on following two lines from program. You will see a `var`, `val` and `def`, actually doing same job

```scala
  /* A variable, value and definition, doing same jobs (increment of integer value) */
  var incrementVar = (x: Int) => x + 1 /* A definition using 'var' */
  val incrementVal = (x: Int) => x + 1 /* A definition using 'val' */
  def incrementDef = (x: Int) => x + 1 /* A definition using 'def' */
```



