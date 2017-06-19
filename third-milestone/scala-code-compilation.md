| Topic | Scala code compilation |
| :--- | :--- |
| Git sample | [ListOperationsTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ListOperationsTest.scala)|


##	Scala class compilation

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
	*	`ListOperationsTest$$anonfun$1.class` 		: 	The anonymous Closure (`{ _ + _ }`) got compiled into it. Every Scala Closure results into an anonymous class, similar to a Java Lambda
	*	`ListOperationsTest.class`		      	:	Actual call is forwarded to `ListOperationsTest$`
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

*	Porgram above are Java programs, decompiled from scala byte code
*	Scala uses **Singleton Objects** mechanism, to ensure that they’re true objects but look similar to static method invocations to Java

##	Scala switch statement compilation
*	Scala uses the **tableswitch** optimization. The tableswitch instruction is made up of mappings of integer values to bytecode instruction labels. Following Scala class is compiled into tableswitch statement
	```scala
	def unannotated(x: Int) = x match {
		case 1 => "One"
		case 2 => "Two!"
		case z => z + "?"
	}
	```
	```java
	/* Equivalent bytecode of above Scala method */
	public java.lang.String unannotated(int);
		Code:
		0: iload_1
		
		1: tableswitch{ 
			/* Mappings of integer values to bytecode instruction labels (or line numbers) */
			1: 51;
			2: 46;
			default: 24
		}
	...	
	```
