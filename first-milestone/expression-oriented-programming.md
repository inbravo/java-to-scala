| Topic | Expression Oriented Programming |
| :--- | :--- |
| Git sample | [AvoidReturnTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/AvoidReturnTest.scala) |

---

##	Avoid `return` Statements
*	**STATEMENT VS EXPRESSION**: A Statement **Executes** while An Expression **Evaluates** to a **Value**
*	In Java, there is a practice of using keyword `return` at the end of a method. You can do the same in Scala, Example below shows it
	```scala
	  /* Scala code below resembles Java */
	  def getErrorMessageWithReturnFirst(errorCode: Int): String = {

		/* A variable ('var') type which can change after declaration */
		var result: String = "Unknown Error"

		errorCode match {
		  case 1 => result = "TCP Socket Failure"
		  case 2 => result = "UDP Failure"
		  case 3 => result = "Unknown Error"
		}

		/* Return the result */
		return result
	  }
	```
*	Scala code above can be improved with the help of expression-oriented syntax, Below given Scala code shows how `match` returns `result`
	```scala
	  /* Scala code below still resembles Java */
	  def getErrorMessageWithExplicitReturnSecond(errorCode: Int): String = {

		/* A value ('val') type which can't change after declaration */
		val result = errorCode match {
		  case 1 => "TCP Socket Failure"
		  case 2 => "UDP Failure"
		  case 3 => "Unknown Error"
		}

		/* Return the result */
		return result
	  }
	```
*	Scala code can be improved further, by removing `val result` declaration
	```scala
	  /* Scala code below somewhat resembles Java */
	  def getErrorMessageWithExplicitReturnThird(errorCode: Int): String = {

		/* Control structure 'match' is returning a String */
		return errorCode match { case 1 => "TCP Socket Failure" case 2 => "UDP Failure" case 3 => "Unknown Error" }
	  }
	```
*	**NO RETURN STATEMENT**: An expression evaluates to a value, so there’s no need of `return`
	```scala
	 /* Scala code below rarely resembles Java */
	  def getErrorMessageWithoutReturn(errorCode: Int): String = {

		/* Control structure 'match' is the last statement in this method; automatically taken as return value */
		errorCode match { case 1 => "TCP Socket Failure" case 2 => "UDP Failure" case 3 => "Unknown Error" }
	  }
	```
*	Avoid return statement and prefer to have the last expression be the return value
## Prefer Immutability

*	Most of the mainstream languages, including object-oriented programming languages such as C#, Visual Basic, C++, and Java, were designed to primarily support Imperative (procedural) Programming
*	Imperative code tends to be made of statements, not expressions
*	Objects are created with an initial state. Then statements are executed that Mutate or Change the state of an object
*	Immutability, in programming, refers to the unchanging state of objects after construction. Scala prefers immutability in design, making it the default in many cases
*	Defining a variable as a val means that it’s an **Immutable** reference
*	All method parameters are **Immutable** references and class arguments default to being **Immutable** references
*	**The only way to create a mutable variable is through the `var` syntax**