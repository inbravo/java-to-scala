| Topic | Array |
| :--- | :--- |
| Time Required | 30 mins |
| Benefits |  |
| Git sample |  |

`Array` item used for fix length array in Scala. array of integers initialized by 0, while array of string initialized with null. we should use \(\) to access the elements of Array.

`val nums = new Array[Int](10)`

`val s = Array("Hello", "World")`

`s(0) = "Goodbye" // this is equivalent to s.update(0,"Goodbye")`

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

