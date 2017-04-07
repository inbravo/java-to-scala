| Topic | Common types in Scala |
| :--- | :--- |
| Time required | 15 minutes |
| Benefit realized | Understanding of Scala Basic types |
| Git sample | [ValuesTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ValuesTest.scala) |

---

* As Scala is pure object oriented language, each and every value in Scala is an object. Even all of the primitive data types of Scala are the objects.

* Class `Any`is the root of the Scala class hierarchy. Every class in a Scala execution environment inherits directly or indirectly from this class. Class `Any`has two direct subclasses: `AnyRef`and `AnyVal`

  ![](/assets/types.png)

* From the above Image `AnyVal`is extended by all numeric types. All types reside in package `scala`

* Scala has 7 numeric types  
  1. **Byte **  **  :**   `val maxByteValue: Byte = Byte.MaxValue   : 8 bits`  
  2. **Char **  **  :**   `val maxCharValue: Char = Char.MaxValue : 16 bits `  
  3. **Short **  ** :**   `val maxShortValue: Short = Short.MaxValue : 16 bits `  
  4. **Int **  **      :**   `val maxIntValue: Int = Int.MaxValue : 32 bits`  
  5. **Long **  **  :**   `val maxLongValue: Long = Long.MaxValue  : 64 bits`  
  6. **Float **  **  :**   `val maxFloatValue: Float = Float.MaxValue : 32 bits `  
  7. **Double  :**   `val maxDoubleValue: Double = Double.MaxValue  : 64 bits`

* Type `Unit`is similar to `void`in Java. If you remember the Hello World program, `Unit`was the return type of `main`method

```scala
def main(args: Array[String]): Unit = { .... }
```

* Scala also has got a type **Boolean **:    `val trueBoolean: Boolean = true`

* In Scala `Null `is also an object, Null corresponds to Null value or empty reference.  

* No one can create object like `Nothing `in scala, this is used to denote empty collection or abnormal termination. 

* Open program `com.inbravo.lang.ValuesTest.scala` \[[ValuesTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ValuesTest.scala)\] in Eclipse and run...

```scala
package com.inbravo.lang

/**
 * Following program helps in undersanding the various Scala types
 *
 * amit.dixit
 */
object ValuesTest extends App {

  /* Different Scala types, initialized with their maximum value and with their types (NAME:TYPE e.g. val maxByteValue: Byte) */
  val maxByteValue: Byte = Byte.MaxValue
  val maxCharValue: Char = Char.MaxValue
  val maxShortValue: Short = Short.MaxValue
  val maxIntValue: Int = Int.MaxValue
  val maxLongValue: Long = Long.MaxValue
  val maxFloatValue: Float = Float.MaxValue
  val maxDoubleValue: Double = Double.MaxValue

  /* Print values */
  println("Byte Max Value: " + maxByteValue)

  /* Trick is used to convert a Char to yeild numeric value */
  println("Char Max Value: " + (maxCharValue + 0))
  println("Short Max Value: " + maxShortValue)
  println("Int Max Value: " + maxIntValue)
  println("Long Max Value: " + maxLongValue)
  println("Float Max Value: " + maxFloatValue)

  /* Method print does not ends with a new line */
  print("Double Max Value: " + maxDoubleValue)

  /* Different Scala types, initialized with their minimum value and without their types */
  val minByteValueWithoutType = Byte.MinValue
  val minCharValueWithoutType = Char.MinValue
  val minShortValueWithoutType = Short.MinValue
  val minIntValueWithoutType = Int.MinValue
  val minLongValueWithoutType = Long.MinValue
  val minFloatValueWithoutType = Float.MinValue
  val minDoubleValueWithoutType = Double.MinValue

  /* Print values */
  println("Byte Min Value: " + minByteValueWithoutType)

  /* Trick is used to convert a Char to yeild numeric value */
  println("Char Min Value: " + (minCharValueWithoutType + 0))
  println("Short Min Value: " + minShortValueWithoutType)
  println("Int Min Value: " + minIntValueWithoutType)
  println("Long Min Value: " + minLongValueWithoutType)
  println("Float Min Value: " + minFloatValueWithoutType)

  /* Method print does not ends with a new line */
  print("Double Min Value: " + minDoubleValueWithoutType)

  /* Boolean values */
  val trueBoolean: Boolean = true
  val falseBoolean: Boolean = false
}
```



