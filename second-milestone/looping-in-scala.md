| Topic | Scala Control Structure |
| :--- | :--- |
| Time Required | 10 mins |
| Benefit realized | How control structures works in Scala |
| Git sample | [LoopTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/LoopTest.scala) |

---

* The only control structures
   in Scala are if, while, for, try, match, and function calls.
* Almost all of Scala’s control structures
   result in some value, as per the functional approch of Scala. 
* Scala `if-else` logic is almost similar with Java

  * Scala `if-else` statements returns a value, which is different from Java. Example`var maxoftwo = if(x>y) x else`

  * In cases, where `else` part if not defined in `if-else` statement, return type would be `Any`

    ```scala
    /* In below statement 'else' is not defined so the return type would be 'Any' */
    val result = if(a%2) return "even"

    /* Return type will be Java.lang.String */
    val result = if(a%2) return "even" else "odd"
    ```

  * An `if` statement without an `else`is  equivalent to `if (x > 0) 1 else ()`

* Scala looping is almost similar to Java while using `while`and `do-while`

```scala
while(condition){ 
    statement(s)
}
```

```scala
do{    
    statement(s)
}while(condition)
```

* Scala has slightly different approach for looping through `for` , you can filter \(if condition\) in for loop.

```scala
for(variable <- list) statement

/* OR */
for(variable <- range) statement

/* OR */
for(variable <- [range or list] if condition; if condition; ...) statement
```

```scala
var list = List(1,2,3,4,5,6,7,8,9,10)

/* Print odd number in list except 7 */
for(element <- list if element%2 != 0; if element!= 7) println("Element of list is : " + element)
```

* you can use "to" or "until"\(to exclude upper bound\) for iteration with "for". 
* match - case use in scala same as switch in other language. 



