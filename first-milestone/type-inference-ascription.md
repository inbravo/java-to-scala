| Topic | Type Inference and Type Ascription In scala |
| :--- | :--- |
| Git sample | [TypeAscriptionInferenceTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/TypeAscriptionInferenceTest.scala) |

---
*	Scala has **Type Inference**, which means that we can skip telling the type of something in the source code

```scala

/* A dummy triat */
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
