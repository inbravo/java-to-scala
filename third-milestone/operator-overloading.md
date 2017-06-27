| Topic | Operator as Functions and Object as Functions |
| :--- | :--- |
| Git sample | [OperatorsAreMethods.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/OperatorsAreMethods.scala) & [ApplyMethodTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ApplyMethodTest.scala) |

---

## Operators as Functions

*	Unlike Java, you can treat operators as functions (operator overloading) in Scala

*	Every value in Scala is an **Object** and every operation is a **Method Call**. For example, when you say `1 + 2` in Scala, you are actually invoking a method named `+` defined in class Int, and 1 and 2 are objects we are passing to this method

*	All operators do the usual work \(`+ - * / % & | ^ >> <<`\), but these operators are methods, which is owing to operator overloading feature of Scala

*	**`a + b`**  is a shorthand for **`a.+(b)`**

*	If a & b are type of Int, method **'+'** of Int class will applied on operation: **`a.+(b)`**

## Objects as Functions

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

*	Method `unapply` is a bit more complicated. It is used in Scala's pattern matching mechanism and its most common use is in **Extractor Objects**

```scala
object UserIdToEmail {

  /* Apply method helps in constructor like calls */
  def apply(id: String) = if (!id.contains("@")) id + "@inbravo-org.com" else id

  /* Apply method helps in constructor like calls */
  def apply(id: String, domain: String) = id + "@" + domain

  /* 'unapply' method helps in removing any sugar coating */
  def unapply(id: String): Option[(String)] = {

    /* Split the email id in two parts */
    val parts = id split "@"

    /* Length of resultive array shouuld be 2  */
    if (parts.length == 2) Some(parts(0)) else None
  }

  /* 'unapply' method helps in removing any sugar coating */
  def unapply(id: String, domain: String): Option[(String)] = {

    /* 'Id' should not contain '@' */
    if (!id.contains("@")) Some(id) else None
  }
}

  var defaultEmail = UserIdToEmail("inbravo")
  var perfectEmail = UserIdToEmail("inbravo@inbravo-org.com")
  var splittedEmail = UserIdToEmail("inbravo", "inbravo-org.com")

  defaultEmail = defaultEmail match {
    case UserIdToEmail(userId) => userId
    case _                     => throw new scala.MatchError(defaultEmail)
  }
```

*	Let's suppose `emailString = inbravo`. Then what happens? In this case `UserIdToEmail.unapply(id: String)` gets called, and as you can see, will return `Some("inbravo")`. The contents of the `Option` will get assigned to `userId` so in the end, the above pattern match will print out "inbravo"

*	But what if `myInt = 1`? Then `Foo.unapply(1)` returns `None` so the corresponding expression for that pattern does not get called

*	In the case of assignments, like `val Foo(str) = x` this is syntactic sugar for:

```scala
val str : String = Foo.unapply(x) match {
  case Some(s) => s
  case None    => throw new scala.MatchError(x)
}
```

* For more information [refer](http://www.scala-lang.org/old/node/112)
