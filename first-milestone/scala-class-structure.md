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
	*	`ListOperationsTest.class`		
	*	`ListOperationsTest$.class`			:	The `Average` object gets compiled into it
*	The `ListOperationsTest` object gets compiled into the `ListOperationsTest$` with the `ListOperationsTest` class having the static method forwarded to the `ListOperationsTest$` object. 
*	This is the mechanism Scala uses for **singleton objects** to ensure that they’re true objects but look similar to static method invocations to Java
