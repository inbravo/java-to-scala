| Topic | High Order Functions |
| :--- | :--- |
| Git sample 		| N/A	|
| References		| [alvinalexander.com](http://alvinalexander.com/scala/fp-book/pure-functions-and-io-input-output)	|

---

*	A pure function is a function that depends only on its declared input parameters and its algorithm to produce its output

*	It does not read any other values from the world outside of the function’s scope and it does not modify any values in the outside world

*	A Pure Function has no side effects on system resource
	*	Compiler can discard or optimize out the return value if it was not used in an expression
    *	The same result is returned for same parameters i.e. one-to-one correspondence or mapping. This can enable caching optimizations such as memoization
    *	Two independent functions can be evaluated out of order, or in parallel without worrying about side-effects
    *	Same strategy can be applied by the compiler if the entire program has many independent functions i.e. many parts of the whole program can run in parrallel, withoug baking-in any paralleism logic!

*	A mantra for writing pure functions : **Output depends only on input**

*	Mathematical functions (`scala.math._`) are great examples of pure functions because their output depends only on input
    *	`abs`
    *	`ceil`
    *	`max`
    *	`min`

*	Because a Scala String is immutable, every method available to a String is a pure function, including:
	*	`charAt`
	*	`isEmpty`
    *	`length`
    *	`substring`

*	Many methods that are available on Scala’s collections’ classes fit the definition of a pure function, including:
	*	`drop`
    *	`filter`
    *	`map`
    *	`reduce`

*	Conversely, the collections’ classes, the foreach method is impure. foreach is used only for its side effects: `def foreach(f: (A) => Unit): Unit`

*	Date and time related methods like `getDayOfWeek`, `getHour`, and `getMinute` are all impure because their output depends on something other than their inputs. Their results rely on some form of hidden I/O

*	Methods on the `scala.util.Random` class like nextInt are also impure because their output depends on something other than their inputs



	





