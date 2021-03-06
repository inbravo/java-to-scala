| Topic | Type Bounds In scala |
| :--- | :--- |
| Git sample | [TypeBoundTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/TypeBoundTest.scala) <br/> [ViewBoundTest.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/lang/ViewBoundTest.scala) |
| References | [docs.scala-lang.org](http://docs.scala-lang.org/tutorials/tour/upper-type-bounds.html) <br/> [docs.scala-lang.org](http://docs.scala-lang.org/tutorials/tour/lower-type-bounds.html) <br/> [journaldev.com](http://www.journaldev.com/9609/scala-typebounds-upper-lower-and-view-bounds) <br/> [stackoverflow.com](https://stackoverflow.com/questions/4465948/what-are-scala-context-and-view-bounds) |

---

*	Methods in Scala can be parameterized by type as well as value. The syntax is similar to that of generic classes of Java

*	Type parameters are declared within a pair of brackets while value parameters are enclosed in a pair of parentheses

```scala
def listOfDuplicates[A](x: A, length: Int): List[A] = {
if (length < 1)
    Nil
else
    x :: listOfDuplicates(x, length - 1)
}

println(listOfDuplicates[Int](3, 4))  // List(3, 3, 3, 3)
println(listOfDuplicates("La", 8))  // List(La, La, La, La, La, La, La, La)
```
    
*	In Scala, type bounds are restrictions on type parameters or type variable. By using type bounds, we can define the limits of a type variable

*	Scala type bounds helps in **Type-Safe** application development

*	Scala supports following type bounds
	*	Upper bounds :	it limits a type to a **Subtype** of another type e.g. `[T <: Ordered[T]]`
	*	Lower bounds : it limits a type to be a **Supertype** of another type e.g. e.g. `[T >: Ordered[T]]`
	*	View bounds	: use implicit conversions automatically
	
*	**Upper bounds** 
	*	 An upper type bound term `T <: A` expresses that type variable `T` refers to a Subtype of type `A` 

*	**Lower bounds** 	
	*	A lower type bounds term `T >: A` expresses that the type variable `T` refers to a Supertype of type `A`
	
```scala
object TypeBoundTest extends App {

  val animal = new Animal
  val dog = new Dog
  val puppy = new Puppy

  val animalCarer = new AnimalCarer

  /* Compilation Error : 'type mismatch; found : com.inbravo.lang.Animal required: T' */
  /* animalCarer.display(animal) */
  animalCarer.upperBoundBasedMethod(dog)
  animalCarer.upperBoundBasedMethod(puppy)
  
  /* Method 'feed' can accept all supertypes of 'Puppy' class not not any subtypes of 'Puppy' class */
  animalCarer.lowerBoundBasedMethod(animal)
  animalCarer.lowerBoundBasedMethod(dog)
  animalCarer.lowerBoundBasedMethod(puppy)
}

/* Top most generalization */
class Animal

/*  Specific 'Animal' types */
class Dog extends Animal
class Puppy extends Dog
class LabradorPuppy extends Puppy

class AnimalCarer {

  /* This method accepts only either Dog class object or subclass type (i.e. Puppy) of Dog Class */
  /* Type bound expression [T <: Dog] says that 'T' can only be a subtype of 'Dog' */
  /* Upper bound is applied */
  def upperBoundBasedMethod[T <: Dog](t: T) = println(t)

  /* This method accepts only either Puppy class object or superclass type (i.e. LabradorPuppy) of Puppy Class */
  /* Type bound expression [T >: Puppy] says that 'T' can only be a supertype of 'Puppy' */
  /* Lower bound is applied */
  def lowerBoundBasedMethod[T >: Puppy](t: T) = println(t)
}
```

*	**View bounds** 	
	*	Please be aware that [view bounds are deprecated](https://github.com/scala/scala/pull/2909)
	*	A view bounds term `[T <% Ordered[T]` expresses that `T` should have an implicit conversion to `Ordered[T]`, so that one can call `T` methods on an object of type `Ordered[T]` 

```scala
/* Scala’s View Bound operator '<%' */
object ViewBoundTest extends App {

  val p1 = new Person("A", "D")
  val p2 = new Person("E", "A")
  val p3 = new Person("G", "A")

  println(p1.greater)
  println(p2.greater)
  println(p3.greater)
}

/* Scala’s View Bound operator '<%' means that 'T' should have an implicit conversion to 'Ordered[T]' available */
class Person[T <% Ordered[T]](val firstName: T, val lastName: T) {

  def greater = if (firstName > lastName) firstName else lastName
}
```
