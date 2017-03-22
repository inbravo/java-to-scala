| Topic | Common types in Scala |
| :--- | :--- |
| Time required | 5 minutes |
| Benefit realized | Understanding of Scala Basic types |
| Git sample | [ValuesTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ValuesTest.scala) |

---

* Scala has seven numeric types 
  1. **Byte**
  2. **Char**
  3. **Short**
  4. **Int**
  5. **Long**
  6. **Float**
  7. **Double**
* Scala also has a **Boolean **type 
* There is no distinction between Primitive types and Class types in Scala. Unlike Java, all Scala types are Classes
* Now run this complete sample and understand every method, by its comments. Open program com.inbravo.lang.ValuesTest.scala \[[ValuesTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ValuesTest.scala)\] in Eclipse and run...

  * ```scala
    /**
     * Following program helps in undersanding the various Scala types
     *
     * amit.dixit
     */
    object ValuesTest extends App {

      /* Different Scala types, initialized with their maximum value */
      val maxByteValue: Byte = Byte.MaxValue
      val maxCharValue: Char = Char.MinValue
      val maxShortValue: Short = Short.MaxValue
      val maxIntValue: Int = Int.MaxValue
      val maxLongValue: Long = Long.MaxValue
      val maxLloatValue: Float = Float.MaxValue
      val maxDoubleValue: Double = Double.MaxValue

      /* Print values. For Char minimum value, which is '\uFFFF', which is not a printable character by definition, so a trick is used */
      println("Byte Max Value: " + maxByteValue + ", Char Max Value: " + (maxCharValue + 0) + ", Short Max Value: " + maxShortValue)
      println("Int Max Value: " + maxIntValue + ", Long Max Value: " + maxLongValue)
      print("Float Max Value: " + maxLloatValue + ", Double Value: " + maxDoubleValue)
    }
    ```



