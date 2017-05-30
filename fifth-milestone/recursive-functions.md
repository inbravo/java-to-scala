| Topic | Recursive Functions |
| :--- | :--- |
| Benefits realized | How Recursive Functions works in Scala  	|
| Git sample 		| [FirstClassFuncTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/FirstClassFuncTest.scala)	|

---

*	A recursive function is a function which calls itself. Example of a simple function,
```scala
def standardSum(a: Int, b: Int): Int = {
    if (a > b) 0
    else {
        var result = 0
        for (number <- a to b)
            result += number
        result
    }
}

/* Call to standard sum method */ 
standardSum(0, 10)
```

*	Example of a recursive function performing same task,
```scala
def recursiveSum(a: Int, b: Int): Int = {
    if (a > b) 0
    else {
        a + recursiveSum(a+1, b)
    }
}

/* Call to recursive sum method */ 
recursiveSum(0, 10)
```