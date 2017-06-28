| Topic | Common types in Scala |
| :--- | :--- |
| Git sample | [ValuesTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ValuesTest.scala) <br/> [AnyValTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/AnyValTest.scala)  |
| References | [docs.scala-lang.org](http://docs.scala-lang.org/tutorials/tour/unified-types.html) <br/> [ktoso.github.io](http://ktoso.github.io/scala-types-of-types) |

---
  
* As Scala is also an object oriented language, each and every value in Scala is an object. Every Scala data type is an object

* Class `Any`is the root of the Scala class hierarchy. Every class in a Scala execution environment inherits directly or indirectly from this class. Class `Any`has two direct subclasses: `AnyRef` and `AnyVal`

  ![](/assets/m-2/types.png)

* From the above Image `AnyVal` is extended by all numeric types. All types reside in package `scala`

* Scala has 7 numeric types  
  1. **Byte**       : 8 bits  :   `val maxByteValue: Byte = Byte.MaxValue`  
  2. **Char**       : 16 bits :   `val maxCharValue: Char = Char.MaxValue`  
  3. **Short**      : 16 bits :   `val maxShortValue: Short = Short.MaxValue`  
  4. **Int**        : 32 bits :   `val maxIntValue: Int = Int.MaxValue`  
  5. **Long**       : 64 bits :   `val maxLongValue: Long = Long.MaxValue`  
  6. **Float**      : 32 bits :   `val maxFloatValue: Float = Float.MaxValue`  
  7. **Double**     : 64 bits :   `val maxDoubleValue: Double = Double.MaxValue`

* Type `Unit`is similar to `void`in Java. If you remember the Hello World program, `Unit` is the return type of `main`method

```scala
def main(args: Array[String]): Unit = { .... }
```

* Scala also has got a type **Boolean** :    `val trueBoolean: Boolean = true`

* **String** is a sequence of Chars, alike a Java String

```scala
/* Two strings */
val stringOne = "stringOne"
val stringTwo = "stringTwo"

val contactOperationOne = stringOne + stringTwo
val contactOperationTwo = stringOne ++ stringTwo

/* Both values are same */
if (contactOperationOne.equals(contactOperationTwo)) {
  println("Both operations ('+' & '++') performs similar on strings")
} else {
  println("Both operations ('+' & '++') performs differently on strings")
}

```

* In Scala the Bottom Types are - Nothing and Null

```scala
val intThing: Int =
  if (test) {
  
    /* Int(AnyVal) */
    11                             
  }
  else {
  
    /* Nothing */ 
    throw new Exception("Nothing!") 
  }
    
val stringThing: String =
  if (test) {
  
    /* String(AnyRef) */
    "Yay!"  
  }
  else {
  
     /* Null */ 
  	null    
  }
```
* Type inference always looks for the common type of both branches in an `if` stamement, so if the other branch is a Type that extends everything, the infered type will automatically be the Type from the first branch

```scala
Nothing -> [Int] -> ... -> AnyVal -> Any : infered type: Int
Null -> [String] -> AnyRef -> Any : infered type: String
```

* In Scala `Null` is an object, `Null` corresponds to `Null` value or empty reference

* No one can create object like `Nothing` in scala, this is used to denote empty collection or abnormal termination

* `AnyRef` is the **Object World** of the Scala, it corresponds to `java.lang.Object` in Java, and is the supertype of all objects

* `AnyVal` on the other hand represents the **Value World** of Scala, such as int and other JVM primitives

```scala
/* A dummy class */
class Person

/* A buffer which can store 'Any' */
val allThings = ArrayBuffer[Any]()

/* Int, kept as low-level 'int' during runtime */
val myInt = 10

/* Add an Int (extends AnyVal). boxed (!) -> becomes java.lang.Integer in the collection */
allThings += myInt

/* Person (extends AnyRef), no magic here */
allThings += new Person
 ```
