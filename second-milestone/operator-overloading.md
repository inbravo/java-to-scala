| Topic | Operator Overloading |
| :--- | :--- |
| Time required | 10 minutes |
| Benefit realized | Benefit of operator overloading in Scala |
| Git sample | [OperatorsAreMethods.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/OperatorsAreMethods.scala) |

---

* Unlike Java, you can overload operators in Scala

* Every value in Scala is an **object **and every operation is a **Method Call**. For example, when you say `1 + 2` in Scala, you are actually invoking a method named `+` defined in class Int, and 1 and 2 are objects we are passing to this method

All operators do the usual work \(`+ - * / % & | ^ >> <<`\), but these operators are methods, which is owing to operator overloading feature of Scala

* `a + b`  is a shorthand for `a.+(b)`
* If a & b are type of Int, method '**+'** of Int class will applied on operation: `a.+(b)`

* Any method can be an operator.   In Scala operators are not special language syntax: any method can   be an operator. What makes a method an operator is how you use it.  When you write “s.indexOf\('o'\)”, indexOf is not an operator. But   when you write “s indexOf 'o'”, indexOf is an operator, because   you’re using it in operator notation.

* Open program `com.inbravo.lang.OperatorsAreMethods.scala`\[[OperatorsAreMethods.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/OperatorsAreMethods.scala%29\)\] in Eclipse and run...



