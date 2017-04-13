| Topic |  |
| :--- | :--- |
| Benefits |  |
|  |  |

#### **List**

Scala List is immutable sequence of objects that contains the same type of objects, while in java List can be mutable. List are designed to enable functional style of Scala.

`val oneTwoThree = List(1, 2, 3) // Creating and initialised List`

Common operations on List are `:::` to concatenate lists and `::` \(cons operator\) to insert an element at starting, these operations will always result in new List, as List are immutable objects in Scala.

Scala use`:+`to append operation, but this rarely used, as the time to append a new element increases with the size of list while prepending \(`::`\) always take constant time.

`List()` or `Nil`  used to create empty List.

#### Tuples

Tuples are also immutable like list, but it can contains elements of different types. so a List can be either List\[Int\] or List\[String\], while tuple can be combination of both. So mostly in Java we used JavaBean like class to hold  multiple return values, while in scala we can do that by using tuples.

`val pair = (99, "Luftballons")       
 // to create and initilized tuple of type Tuple2[Int, String] i.e. Tuple of length 2, we just need to place the objects into parenthesis seprated by commas`

`println(pair._1)//to access the elements of tuple you can use ._and index of element in tuple.`

`println(pair._2)`

The type of \('u', 'r', "the", 1, 4, "me"\) is Tuple6\[Char, Char, String, Int, Int, String\]. Although conceptually you could create tuples of any length, currently the Scala library only defines them up to Tuple22 .

