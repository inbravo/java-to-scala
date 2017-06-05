| Topic | What is the result of Scala class compilation |
| :--- | :--- |
| Git sample | [ListOperationsTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ListOperationsTest.scala)|


##	Scala code compilation

*	Program below creates an object named `ListOperationsTest`
	```scala
	object ListOperationsTest {
	
		  /* Average method uses left folding technique */
		def avg(values: List[Double]) = {
			val sum = values.foldLeft(0.0) { _ + _ }
			sum / values.size.toDouble
		}
	}
	```
*	Compilation of above object results into following 3 classes: 
	*	`ListOperationsTest$$anonfun$1.class` 		: 	The anonymous closure (`{ _ + _ }`) got compiled into it
	*	`ListOperationsTest.class`		      	:	Class with static method forwarded to `ListOperationsTest$`
		```java
		public final class ListOperationsTest
		{
		  public static double avg(List<Object> paramList)
		  {
		    return ListOperationsTest..MODULE$.avg(paramList);
		  }
		}
		```
	*	`ListOperationsTest$.class`
		```java
		public final class ListOperationsTest$ {
		  
		  public static final  MODULE$;

		  static { new ();
		  }

		  public double avg(List<Object> values) { 
		  double sum = scala.runtime.BoxesRunTime.unboxToDouble(values.foldLeft(scala.runtime.BoxesRunTime.boxToDouble(0.0D), new ListOperationsTest..anonfun.1()));
		  return sum / values.size(); 
		  }

		  private ListOperationsTest$() { MODULE$ = this; }
		}
		```
*	This is the mechanism Scala uses for **singleton objects** to ensure that they’re true objects but look similar to static method invocations to Java
