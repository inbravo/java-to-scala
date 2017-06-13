| Topic | Values and variables |
| :--- | :--- |
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

* In Scala, the word constant does not just mean val. Even
   though a val does remain constant after it is initialized, it is still a variable.
   For example, method parameters are vals, but each time the method is called
   those vals can hold different values. A constant is more permanent.
* Scala convention is to use camel case for constants, such as XOffset. 
* In Scala you can define the variables of the same name in different scope.  



