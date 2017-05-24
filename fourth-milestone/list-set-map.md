| Topic | List and Set|
| :--- | :--- |
| Time required | 30 minutes |
| Benefit | How to use Scala List |

---

#### **List**

Scala List is immutable sequence of objects that contains the same type of objects, while in java List can be mutable. List are designed to enable functional style of Scala.

`val oneTwoThree = List(1, 2, 3) // Creating and initialised List`

`oneTwoThree(2) //returns the element at index 2(zero based), while is equal to oneTwoThree.apply(2)`

Common operations on List are `:::` to concatenate lists and `::` \(cons operator\) to insert an element at starting, these operations will always result in new List, as List are immutable objects in Scala.

Scala use`:+`to append operation, but this rarely used, as the time to append a new element increases with the size of list while prepending \(`::`\) always take constant time.

`List()` or `Nil`  used to create empty List.


#### Set

`var jetSet = Set("Boeing", "Airbus")      
 //Create and initilize Immutable Set with 2 Strings.`

`jetSet += "Lear"      
 // reassign the jetSet var with a      
 new set containing "Boeing", "Airbus", and "Lear`

`println(jetSet.contains("Cessna"))`

In case of mutable Set

`import scala.collection.mutable.Set`

`val movieSet = Set("Hitch", "Poltergeist")      
 //Create mutable Set`

`movieSet += "Shrek"      
 // Add Shrek to movieSet`

`println(movieSet)`

#### Map

Maps are collection of key/value pairs. In Scala, a map is a collection of pairs.In scala Map can be hash table or balanced tree, depending upon the implementation. By default it would be hash table. . A pair is simply a grouping of two values,  
not necessarily of the same type, such as \("Alice", 10\).You can construct map like :

`val scores = Map("Alice" -> 10, "Bob" -> 3, "Cindy" -> 8)` OR

`val scores = Map(("Alice", 10), ("Bob", 3), ("Cindy", 8))`

above is an example of immutable Map\[String, Int\], whose content can't be change. To make mutable map, please use:

`val scores = scala.collection.mutable.Map("Alice" -> 10, "Bob" -> 3, "Cindy" -> 8)`

To create blank map :

`val scores = new scala.collection.mutable.HashMap[String, Int]`

You can access values from Map as :

`scores("Bob")`  // =3 , Like scores.get\("Bob"\) in Java, it will throw exception if value for the requested key not present in Map. you can use

`val bobsScore = if (scores.contains("Bob")) scores("Bob") else 0` Or

`val bobsScore = scores.getOrElse("Bob", 0)`

you can add/update value in map using \(\) :

scores\("Bob"\) = 5 //if Bob present, it will update value for Bob, otherwise add new pair.

you can also use += or -= to add deleted pairs from Map.

To iterate Map :

`for ((k, v) <- map)`

To visit only keys you can use `scores.keySet`  or to iterate values `for (v <- scores.values)`

To get an immutable tree map instead of a hash map, use

`val scores = scala.collection.immutable.SortedMap("Alice" -> 10,        
"Fred" -> 7, "Bob" -> 3, "Cindy" -> 8)`

To map Java map into Scala you can use conversion utility by importing

`import scala.collection.JavaConversions.mapAsScalaMap.` To use scala map into java you can use

`import scala.collection.JavaConversions.mapAsJavaMap`