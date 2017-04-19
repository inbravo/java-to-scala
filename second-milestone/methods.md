| Topic | Methods |
| :--- | :--- |
| Time required | 30 minutes |
| Benefit realized | Ability to define properties and fields |
| Git sample | [MethodTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/MethodTest.scala) \(Need to update this class to \) |

---

* Scala provides keyword `def`for creating methods or definitions

```scala
def incrementDef = (x: Int) => x + 1 /* A definition using 'def' */
```

* Declare a method which takes no parameter and returns nothing but prints 'Hello''

```scala
def print = println(value)
```

* Notice that unlike Java, you can ignore curly brackets \(`{ ... }`\) while defining Scala methods

```scala
def print = { println(value) }
```

* Declare a method which take a parameter and returns nothing but prints the passed `Int` value

```scala
def printIt(value: Int) = println(value)
```

* Declare a method which take no parameter and returns something

```scala
/* Method returns Int value '1' */
def returnInt = 1

/* Method returns Float value '1.0' */
def returnFloat = 1.0

/* Another way to explicitly define return type (method-name:type) for methods */
def returnInt: Int = return 1
def returnFloat: Float = return 1.0F
```

* Open program `com.inbravo.lang.MethodTest.scala`\[[MethodTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/MethodTest.scala%29%29\)\] in Eclipse and run...

* You can also call a method with variable number of arguments, with the help of star \(`*`\)  and call using `sum (1,2,3,4)`

```scala
def sum(args: Int*) = {  

 var result = 0  
 
 for (arg <- args) result += arg  
  result  
 }
}
```



