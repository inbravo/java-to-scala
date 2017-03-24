| Topic | Values and variables |
| :--- | :--- |
| Time required | 15 minutes |
| Benefit realized | Ability to define properties and fields |
| Git sample\(s\) | VarAndValTest.scala & [LazyValTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/LazyValTest.scala) |

---

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

* **Variables as functions: **thanks to functional nature of Scala.

* Open program`com.inbravo.lang.FirstClassFuncTest.scala`\[[FirstClassFuncTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/FirstClassFuncTest.scala%29\)\] in Eclipse and run...

* Focus on following two lines from program. You will see a variable and a function; doing same job,

```scala
/* Anonymous First-class function as a variable */
var incrementVariable = (x: Int) => x + 1

/* First-class function as a definition */
def incrementFunction = (x: Int) => x + 1
```



