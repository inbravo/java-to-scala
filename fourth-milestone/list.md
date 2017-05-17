| Topic | List |
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

#### 



