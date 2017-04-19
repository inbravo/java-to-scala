| Topic | Looping |
| :--- | :--- |
| Time Required | 10 mins |
| Benefit realized | How looping works in Scala |
| Git sample | LoopTest.scala |

---

* Scala `if-else` logic is almost similar with Java

* Scala `if-else` statements returns a value, which is different from Java. Example`var maxoftwo = if(x>y) x else y`

* In cases, where `else` part if not defined in `if-else` statement, return type would be `Any`

```scala
/* In below statement else is not defined so the return type would be 'Any' */
val result = if(a%2) return "even"

/* Return type will be Java.lang.String */
val result = if(a%2) return "even" else "odd"
```

* A `if` statement without an `else`is  equivalent to `if (x > 0) 1 else ()`

* Scala has similar control structure like Java for looping using `while `and `do-while`

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

* Scala has slighlty different approach for looping through `for `

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



