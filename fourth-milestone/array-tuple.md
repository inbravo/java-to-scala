| Topic | Array and Tuple |
| :--- | :--- |
| Benefits |  |
| Git sample |  |

`Array` item used for fix length array in Scala. array of integers initialized by 0, while array of string initialized with null. we should use \(\) to access the elements of Array.

`val nums = new Array[Int](10)`

`val s = Array("Hello", "World")`

`s(0) = "Goodbye" // this is equivalent to s.update(0,"Goodbye") as all oparations are method call in scala`

In Scala `ArrayBuffer`used for variable length array. which is implemented in`scala.collection.mutable.ArrayBuffer`

`val b = ArrayBuffer[Int]()`

`// Or new ArrayBuffer[Int]`

This will create an empty Array buffer, in which we can add Integers.

to add elements :

`b+ = (1,2,3,4)`

`b.insert(2, 6)`

`//insert before index 2.`

We can also use `insert`or `remove`to add/delete.

\***Yield **: The for \(...\) yield loop creates a new collection of the same type as the original  
 collection.

\***guard :** an if inside the  
 for.To process the elements from an Array which match the particular conditions.

`for (elem <- a if a % 2 == 0) yield 2 * elem`

On Arrays you can directly use `sum, min, max, sorted` methods.

**Multidimensional Arrays**

As in Java, Scala also supports multidimensional array as arrays of arrays.

`val matrix = Array.ofDim[Double](3, 4) //Array of three rows, four columns of Double type.`

To access the element :

`matrix(row)(column)`

Scala arrays are implemented as Java arrays, you can pass them back and  
 forth between Java and Scala.

#### Tuple

Tuples are also immutable like list, but it can contains elements of different types. so a List can be either List\[Int\] or List\[String\], while tuple can be combination of both. So mostly in Java we used JavaBean like class to hold  multiple return values, while in scala we can do that by using tuples.

`val pair = (99, "Luftballons")                 
 // to create and initilized tuple of type Tuple2[Int, String] i.e. Tuple of length 2, we just need to place the objects into parenthesis seprated by commas`

`println(pair._1)//to access the elements of tuple you can use ._and index of element in tuple.`

`println(pair._2)`

The type of \('u', 'r', "the", 1, 4, "me"\) is  
 Tuple6\[Char, Char, String, Int, Int, String\]. Although conceptually you could create tuples of any length, currently the Scala library  
 only defines them up to Tuple22 .

\*Note : you can not use pair\(0\) to access the element of tuple same as list, because that call apply method, and apply always return same type of element, while tuples support elements of diffrent type.





