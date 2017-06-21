| Topic | Defining Method/Definitions in Scala Class/Object |
| :--- | :--- |
| Git sample | [MethodTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/MethodTest.scala) & [SomeNoneOptionTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/SomeNoneOptionTest.scala)|

---

* Scala provides keyword `def`for creating methods or definitions

```scala
/* A definition using 'def' */
def incrementDef = (x: Int) => x + 1 
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

* Open program `com.inbravo.lang.MethodTest.scala` [MethodTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/MethodTest.scala)

* You can also call a method with variable number of arguments, with the help of star \(`*`\) 

```scala
/* Method which accepts anu number of Int type of arguments */
def sum(args: Int*) = {  

 var result = 0  

 for (arg <- args) result += arg  
  result  
 }
}

/* Multiple valid method calls */
sum(1,2)
sum(1,2,3,4)
```

* You can define local functions as well in scala just like local fields, and these will be visible in only their enclosing block 

* Scala supports named arguments. Each argument is preceded by a parameter name and an equals sign

```scala
/* Method definition */
def speed(time : float, distance : float)

/* Method calls with argument names */
speed(distance = 100, time = 10)
```

##	Use `None` instead of `null`

*	While it was habit in Java to initialize values to null, Scala provides an Option type for the same purpose

*	In Java, `null` is often used as a placeholder to denote a nonfatal error as a return value or to denote that a variable isn’t yet initialized

*	In Scala, one can denote this through the None subclass of `scala.Option`

*	Class `scala.Option` can prevent unintended null pointer exceptions when using Scala

*	Now Java has also followed Scala and Introduced `java.util.Optional`


