| Topic | Handle `null` using `scala.Option` class|
| :--- | :--- |
| Git sample | [SomeNoneOptionTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/SomeNoneOptionTest.scala)|


##	Use `None` instead of `null`

*	While it was habit in Java to initialize values to null, Scala provides an Option type for the same purpose
*	In Java, `null` is often used as a placeholder to denote a nonfatal error as a return value or to denote that a variable isn’t yet initialized
*	In Scala, one can denote this through the None subclass of `scala.Option`
*	Class `scala.Option` can prevent unintended null pointer exceptions when using Scala
*	Now Java has also followed Scala and Introduced `java.util.Optional`

