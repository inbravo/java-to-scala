| Topic | Common types in Scala |
| :--- | :--- |
| Time required | 15 minutes |
| Benefit realized | Understanding of Scala Basic types |
| Git sample | [ValuesTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ValuesTest.scala) |

---

* As Scala is also an object oriented language, each and every value in Scala is an object. Every Scala data type is an object

* Class `Any`is the root of the Scala class hierarchy. Every class in a Scala execution environment inherits directly or indirectly from this class. Class `Any`has two direct subclasses: `AnyRef`and `AnyVal`

  ![](/assets/types.png)

* From the above Image `AnyVal`is extended by all numeric types. All types reside in package `scala`

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

* Scala includes a special syntax for String. Enclose any string within three double quotation, marked in a row \("""\). Enclosed string may contain any characters whatsoever, including newlines, quotation marks, and special characters

```scala
println("""Welcome to Scala Training. Type "HELP" for help.""")
```

* In Scala `Null` is an object, `Null` corresponds to `Null` value or empty reference

* No one can create object like `Nothing`in scala, this is used to denote empty collection or abnormal termination

* Open program `com.inbravo.lang.ValuesTest.scala` [ValuesTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ValuesTest.scala)



