| Topic | Expression Oriented Programming |
| :--- | :--- |
| Git sample | [AvoidReturnTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/AvoidReturnTest.scala) |

---
*	**STATEMENT VERSUS EXPRESSION**:  A statement is something that executes; an expression is something that evaluates to a value
*	**NO RETURN STATEMENT**: An expression evaluates to a value, so there’s no need to return
*	In Java, there is a practice of using keyword `return` at the end of a method. You can do the same in Scala, Example below shows it
	```scala
	  def getErrorMessageWithReturn(errorCode: Int): String = {

		/* Variable initializaed the default value using uderscore '_' */
		var result: String = "Unknown Error"

		errorCode match {
		  case 1 => result = "TCP Socket Failure"
		  case 2 => result = "UDP Failure"
		  case 3 => result = "Unknown Error"
		}
		return result
	  }
	```
*	Scala code above can be improved with the help of expression-oriented syntax, Below given Scala code show how 'match' returns `result`
	```scala
	  def getErrorMessageWithExplicitReturn(errorCode: Int): String = {

		val result = errorCode match {
		  case 1 => "TCP Socket Failure"
		  case 2 => "UDP Failure"
		  case 3 => "Unknown Error"
		}
		return result
	  }
	```
*	Scala code can be improved further, by completely removing `return` keyword
	```scala
	  def getErrorMessageWithoutReturn(errorCode: Int): String = {

		/* Control structure 'match' is the last statement in this method and 'match' is returning a String */
		errorCode match {
		  case 1 => "TCP Socket Failure"
		  case 2 => "UDP Failure"
		  case 3 => "Unknown Error"
		}
	  }
	```
*	Open program [AvoidReturnTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/AvoidReturnTest.scala) and run