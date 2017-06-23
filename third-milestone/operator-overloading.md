| Topic | Operator as Functions and Object as Functions |
| :--- | :--- |
| Git sample | [OperatorsAreMethods.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/OperatorsAreMethods.scala) & [ApplyMethodTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ApplyMethodTest.scala) |

---

*	Unlike Java, you can treat operators as functions (operator overloading) in Scala

*	Every value in Scala is an **Object** and every operation is a **Method Call**. For example, when you say `1 + 2` in Scala, you are actually invoking a method named `+` defined in class Int, and 1 and 2 are objects we are passing to this method

*	All operators do the usual work \(`+ - * / % & | ^ >> <<`\), but these operators are methods, which is owing to operator overloading feature of Scala

*	**`a + b`**  is a shorthand for **`a.+(b)`**

*	If a & b are type of Int, method **'+'** of Int class will applied on operation: **`a.+(b)`**

*	Scala provides `apply` and `unapply`

*	Methods `apply` and `unapply` are not opposites of each other. Indeed, if you define one on a class/object, you don't have to define the other

*	Method `apply` is probably the easier to explain. When you treat your object like a function, apply is called, so Scala turns `obj(a, b, c)` to `obj.apply(a, b, c)`

```scala
/* Various ways to create customer id from customer name */
object CustomerId {

  /* Apply method helps in constructor calls */
  def apply(name: String) = "ID-" + name
  def apply(id: Int) = id
  def apply(id: Long) = id.intValue
  def apply(id: Double) = id.intValue
}

  /* Object as function */
  /* Will call 'apply(name: String)' */
  println(CustomerId("Amit"))

  /* Will call 'apply(id: Int)' */
  println(CustomerId(100))

  /* Will call 'apply(id: Long)' */
  println(CustomerId(100L))

  /* Will call 'apply(id: Double)' */
  println(CustomerId(1000.0)
```

*	Method `unapply` is a bit more complicated. It is used in Scala's pattern matching mechanism and its most common use is in [Extractor Objects](http://www.scala-lang.org/old/node/112)

```scala
object Foo {
  def unapply(x : Int) : Option[String] = 
    if(x == 0) Some("Hello, World") else None
}

/* So now, if you use this is in a pattern match like so: */
myInt match {
    case Foo(str) => println(str)
}
```

*	Let's suppose `myInt = 0`. Then what happens? In this case `Foo.unapply(0)` gets called, and as you can see, will return `Some("Hello, World")`. The contents of the `Option` will get assigned to `str` so in the end, the above pattern match will print out "Hello, world"

*	But what if `myInt = 1`? Then `Foo.unapply(1)` returns `None` so the corresponding expression for that pattern does not get called

*	In the case of assignments, like `val Foo(str) = x` this is syntactic sugar for:

```scala
val str : String = Foo.unapply(x) match {
  case Some(s) => s
  case None    => throw new scala.MatchError(x)
}
```

* For more information [refer](http://www.scala-lang.org/old/node/112)
