| Topic | Maps and Tuples |
| :--- | :--- |
| Time Required |  |
| Benefits |  |
| Git Sample |  |

Maps are collection of key/value pairs. in Scala you can construct map like :

`val scores = Map("Alice" -> 10, "Bob" -> 3, "Cindy" -> 8)`

above is an example of immutable Map\[String, Int\], whose content can't be change. To make mutable map, please use: 

` val scores = scala.collection.mutable.Map("Alice" -> 10, "Bob" -> 3, "Cindy" -> 8)`

To create blank map :

`val scores = new scala.collection.mutable.HashMap[String, Int]`

