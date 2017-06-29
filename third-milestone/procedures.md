| Topic | Procedures and partially applied function |
| :--- | :--- |
| Git sample | [ProcedureTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ProcedureTest.scala) </br> [PartialAppliedFuncTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/PartialAppliedFuncTest.scala) |
| References | [alvinalexander.com](http://alvinalexander.com/scala/how-to-use-partially-applied-functions-in-scala-syntax-examples) |

---

## Procedures: methods with no return types

* A procedure is a Scala method or definition which **Returns No Value**. Because the procedure doesn’t return any value, It lacks equal(`=`) symbol

```scala
/* Look carefully: there is no '=' */
def box(s : String) { 

    val border = "-" * s.length + "--\n"
    println(border + "|" + s + "|\n" + border)
}
```

* If the function body is enclosed in braces without a preceding = symbol, then the return type is `Unit`

* Best is to always use `Unit`in cases where no return type

```scala
def box(s : String): Unit = {

}
```

## Partial functions

*   In Java all the parameters are passed to the function. In Scala you can give only a subset of the parameters to the function, the result of the expression is a partially applied function

```scala
def aFunction(one: Int, two: Int, three: Int) = one + two + three

/* A completly applied function */
val returnedValue = aFunction(1, 2, 3)
println(returnedValue)

/* A partial applied function */
val partialAppliedFunc = aFunction(1, _: Int, _: Int)
println(partialAppliedFunc)

/* A partial applied function */
val secondPartialAppliedFunc = aFunction(1, 2, _: Int)
println(secondPartialAppliedFunc)

/* A partial applied function */
val thirdPartialAppliedFunc = aFunction(1, _: Int, 3)
println(thirdPartialAppliedFunc)

/* Now apply all these functions on more variables */
println(partialAppliedFunc(2, 3))
println(secondPartialAppliedFunc(3))
println(thirdPartialAppliedFunc(2))
```
