| Topic | Implicit Type Conversions |
| :--- | :--- |
| Git sample |  |

---
*	There's a fundamental difference between your own code and other libraries. You can update or extend your own code, but you can't do the same with other libraries
*	Scala has implicit parameters and conversions. They can make existing libraries much more pleasant to deal with
*	Say you have a value `x` of type `Array[int]` and you want to assign this value to some variable of type `String`	
	```scala
	var v: String = x
	```
*	Line above would give a type error, because `Array[int]` does not confirm to `String`. However a conversion from `Array` to `String` can help
	```scala
	implicit def array2string[T](x: Array[T]) = x.toString
	```
*	The conversion is automatically inserted by using `implicit` method `array2string`
	```scala
	var v: String = array2string(x)
	```
