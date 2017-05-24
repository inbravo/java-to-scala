| Topic | Implicit Type Conversions |
| :--- | :--- |
|  |  |

---

*	There's a fundamental difference between your own code and other libraries. You can update or extend your own code, but you can do the same with other libraries
*	Scala has implicit parameters and conversions. They can make existing libraries much more pleasant to deal with
*	Say you have a value x of type Array[int] and you want to assign this value to some variable of type String:	
	```scala
	var v: String = x
	```
*	'Array[int]' does not conform to String, so normally this would give a type error. However, you can define a conversion function from arrays of arbitrary element type T to String, like this:
	```scala
	implicit def array2string[T](x: Array[T]) = x.toString
	```
*	The conversion is automatically inserted. So the above assignment would be expanded to:
	```scala
	var v: String = array2string(x)
	```
