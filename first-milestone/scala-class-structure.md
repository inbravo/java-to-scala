| Topic | What is the result of Scala class compilation |
| :--- | :--- |
| Git sample | |


##	Scala code compilation

*	Program below creates an object named `Average`
	```scala
	object Average {
	
		/* Average method uses a  */
		def avg(values: List[Double]) = {
			val sum = values.foldLeft(0.0) { _ + _ }
			sum / values.size.toDouble
		}
	}
	```
*	Compilation of above object results into following 3 classes: 
	*	`Average$$anonfun$1.class` 	: 	The anonymous closure (`{ _ + _ }`) got compiled into it
	*	`Average.class`		
	*	`Average$.class`			:	The `Average` object gets compiled into it
*	The `Average` object gets compiled into the `Average$` with the `Average` class having the static method forwarded to the `Average$` object. 
*	This is the mechanism Scala uses for **singleton objects** to ensure that they’re true objects but look similar to static method invocations to Java
