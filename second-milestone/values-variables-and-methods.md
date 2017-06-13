| Topic | Values and variables |
| :--- | :--- |
| Git sample\(s\) | [VarAndValTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/VarAndValTest.scala) & [LazyValTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/LazyValTest.scala) |

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

* All `val` type variables are initialized before utilization. A Scala `val`is a `public static final` in Java

* If you want to defer this process of initiailization untill actuall utlization, use `lazy val`

```scala
/* Lazy value without type */
lazy val lazyValue = 100

/* Lazy value with type */
lazy val lazyValueWithType: Int = 100
```

* Scala provides keyword `def` for creating methods or definitions

```scala
def incrementDef = (x: Int) => x + 1 /* A definition using 'def' */
```

* In Scala `val` does not mean only a constant, even though a `val` remains constant after its initialization, it is still a variable. For example, method parameters are `val`, but each time the method is called those `val` can hold different values

