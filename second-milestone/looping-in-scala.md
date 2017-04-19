| Topic | Looping |
| :--- | :--- |
| Time Required | 10 mins |
| Benefit realized | How looping works in Scala |
| Git sample | [LoopTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/LoopTest.scala) |

---

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

* Scala has slighlty different approach for looping through `for`

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



