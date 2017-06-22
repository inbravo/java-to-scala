| Topic | Type Inference, Type Ascription and Type Aliasing In scala |
| :--- | :--- |
| Git sample | [TypeAscriptionInferenceTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/TypeAscriptionInferenceTest.scala) & [TypeAliasTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/TypeAliasTest.scala)|

---
*	Scala has **Type Inference**, which means that we can skip telling the type of something in the source code

```scala

/* A dummy trait */
trait Thing

/* Instance of new trait is created */
def getThing = new Thing { }

/* Without Type Ascription, the type is infered to be 'Thing' */ 
val infered = getThing

/* With Type Ascription */ 
val thing: Thing = getThing
```

*	Leaving out the **Type Ascription** is OK. That’s a good idea, in order to make the code more self-documenting

*	**Early Member Definitions** solve issues that occur when a `trait` defines an abstract value

```scala
/* Trait with some property and definitions */
trait TraitWithProperty {

	/* Abstract value */
	val name: String

	override val toString = "TraitWithProperty(" + name + ")"
}

/* 'traitWithProperty' is a subclass of 'TraitWithProperty' now */
val traitWithProperty = new TraitWithProperty { override val name = "DOMAIN" }

/* Implicit call to 'toString' will print TraitWithProperty(null). Why value of property 'name' is 'null'? */
/* When the toString method looks for the value of name, it hasn’t been initialized yet, so it finds the value 'null' */
println(traitWithProperty)

/* Another implemetation to avoid initialization issue */
/* Before the TraitWithProperty trait, there is an anonymous block containing the early member definition */
class AnotherTraitWithProperty extends { val name = "HI" } with TraitWithProperty

/* Now anonymous block (early member definitions) will provide preinitialized value of name property and toString will print 'TraitWithProperty(HI)' */
/* Early member definitions solve issues that occur when a trait defines an abstract value */
println(new AnotherTraitWithProperty)
```

*	How to pass an object into a method. Just saying obj: ExampleObj won’t work because that’s already referring to the instance, so there’s a member called type which should be used in such cases

```scala
object ExampleObj

def takeAnObject(obj: ExampleObj.type) = {}

takeAnObject(ExampleObj)
```

*	**Type Alias** will make the code more readable. It makes sense for the future reader of this class. See the below example

```scala 
/* Two different types */
type User = String
type Age = Int

/* Call goes to Predef.immutable.Map[A, B]. which creates a map[String => Int] */
var data: Map[User, Age] = Map.empty
```

*	Type Aliases are like Abstract Type Members. Allowing to define templates but instead of using the class `Clazz[A]` syntax,  name them inside the class. Java folks will use generics in similar fashion e.g. SimplestContainer<A>

```scala 
/* In Java : SimplestContainer<A> */
trait SimplestContainer {
  type A      // Abstract Type Member

  def value: A
}

/* 'SimplestContainer' instance can be created without implementing the type member 'A' */
/* Type of 'A' is actualy just a shorthand for type A >: Nothing <: Any, which means 'Anything' */
val someObjectOfSimplestContainer = new SimplestContainer 

/* An object implementing 'SimplestContainer' and providing type information of 'A' */
object IntContainer extends SimplestContainer {

  type A = Int
  def value = 42
}
```
