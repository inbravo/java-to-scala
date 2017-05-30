| Topic | High Order Functions |
| :--- | :--- |
| Benefits realized | How High Order Functions works in Scala  	|
| Git sample 		| [FirstClassFuncTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/FirstClassFuncTest.scala)	|

---

*	A Pure Function has no side effects on system resource
	*	Compiler can discard or optimize out the return value if it was not used in an expression
    *	The same result is returned for same parameters i.e. one-to-one correspondence or mapping. This can enable caching optimizations such as memoization
    *	Two independent functions can be evaluated out of order, or in parallel without worrying about side-effects
    *	Same strategy can be applied by the compiler if the entire program has many independent functions i.e. many parts of the whole program can run in parrallel, withoug baking-in any paralleism logic!



