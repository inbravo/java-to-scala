| Topic | Operator Overloading |
| :--- | :--- |
| Git sample | [OperatorsAreMethods.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/OperatorsAreMethods.scala) |

---

* Unlike Java, you can overload operators in Scala

* Every value in Scala is an **Object** and every operation is a **Method Call**. For example, when you say `1 + 2` in Scala, you are actually invoking a method named `+` defined in class Int, and 1 and 2 are objects we are passing to this method

* All operators do the usual work \(`+ - * / % & | ^ >> <<`\), but these operators are methods, which is owing to operator overloading feature of Scala

* **`a + b`**  is a shorthand for **`a.+(b)`**

* If a & b are type of Int, method **'+'** of Int class will applied on operation: **`a.+(b)`**

* Open program [OperatorsAreMethods.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/OperatorsAreMethods.scala%29)
