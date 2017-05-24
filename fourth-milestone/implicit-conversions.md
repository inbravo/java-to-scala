| Topic | Implicit Type Conversions |
| :--- | :--- |
|  |  |

---

*	There's a fundamental difference between your own code and libraries of other people: You can change or extend your own code, but if you want to use some other libraries you have to take them as they are
*	A number of constructs have sprung up in programming languages to alleviate this problem. Smalltalk has meta classes, Ruby has modules. These are very powerful, but also dangerous, in that you modify the behavior of a class for an entire application, some parts of which you might not know. C# 3.0 has method extensions, which are more local, but also more restrictive in that you can only add methods, not fields or interfaces to a class
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
