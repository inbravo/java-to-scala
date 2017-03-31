| Topic | Anagram Test |
| :--- | :--- |
| Time required | 10 minutes |
| Benefit realized | Writing a simple Scala program |
| Git sample | [Anagram.java](https://github.com/inbravo/java-src/blob/master/src/com/inbravo/string/Anagram.java) and [Anagram.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/string/Anagram.scala) |

---

* Open Java program [Anagram.java](https://github.com/inbravo/java-src/blob/master/src/com/inbravo/string/Anagram.java)
* Open Scala program`com.inbravo.string.Anagram.scala`\[[Anagram.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/string/Anagram.scala)\] in Eclipse and run...
* You will notice that both Scala & Java programs are same

```scala
package com.inbravo.string

/**
 * A simple program to test, if two given strings are anagram
 * amit.dixit
 */
object Anagram {

  def main(args: Array[String]): Unit = {

    val firstString = "KATAK";
    val secondString = "TAKAK";

    println("firstString.type : " + firstString.isInstanceOf[String] + ", secondString.type : " + secondString.isInstanceOf[Int]);

    /* Check if both strings are anagram */
    if (checkIfAnagram(firstString, secondString)) {

      println("Strings '" + firstString + "' & '" + secondString + "' are Anagrams");
    } else {

      println("Strings '" + firstString + "' & '" + secondString + "' are not Anagrams");
    }
  }

  /**
   * O(2n log n) using Quick Sort
   *
   * @param firstString
   * @param secondString
   * @return
   */
  private def checkIfAnagram(firstString: String, secondString: String): Boolean = {

    /* Sort all chars in both string */
    var firstStringChars = firstString.toLowerCase.toCharArray;
    var secondStringChars = secondString.toLowerCase.toCharArray;

    /* Apply quick sort */
    scala.util.Sorting.quickSort(firstStringChars)
    scala.util.Sorting.quickSort(secondStringChars);

    /* Check if same */
    if (String.valueOf(firstStringChars).equals(String.valueOf(secondStringChars))) {

      return true;
    } else {

      return false;
    }
  }
}
```



