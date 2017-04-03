| Topic | Stack |
| :--- | :--- |
| Time required | 30 minutes |
| Benefit realized | Writing a Scala program |
| Git samples | [Stack.java](https://github.com/inbravo/java-src/blob/master/src/com/inbravo/ds/stack/Stack.java) and [Stack.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/ds/stack/Stack.scala) |

---

* Open Java program `com.inbravo.ds.stack.Stack.java` \[[Stack.java](https://github.com/inbravo/java-src/blob/master/src/com/inbravo/ds/stack/Stack.java)\] in Java Eclipse and run...

* Open Scala program`com.inbravo.ds.stack.Stack.scala`\[[Stack.scala](https://github.com/inbravo/scala-src/blob/master/src/main/scala/com/inbravo/ds/stack/Stack.scala)\] in Scala Eclipse and run...

* You will notice that both Scala & Java programs are doing same function

```scala
package com.inbravo.ds.stack

import java.util.concurrent.atomic.AtomicInteger
import scala.collection.mutable.ArrayBuffer

/**
 * amit.dixit
 * Stack class with primary constructor
 */
final class Stack(maxSize: Int) {

  /* Dummy auxiliary constructor */
  def this(maxSize: Int, currentIndex: Int) {

    /* Compilation error if call to primary constructor is not present */
    this(maxSize)
  }

  /* Array for local storage */
  private var storage = new Array[Long](maxSize)

  /* Current index stack */
  private var currentIndex = new AtomicInteger(-1)

  /* Push elements in stack */
  def push(value: Long) = this.storage(this.currentIndex.incrementAndGet()) = value

  /* Pop elements from stack */
  def pop(): Long = return this.storage(this.currentIndex.getAndDecrement())

  /* See what is at top of stack */
  def peek(): Long = return this.storage(this.currentIndex.get())

  /* Check if stack is full */
  def isFull(): Boolean = return (this.currentIndex.get() == (this.storage.length - 1))

  /* Check if stack is empty */
  def isEmpty(): Boolean = return (this.currentIndex.get() == -1)

  /* Print current state of stack */
  override def toString(): String = return (java.util.Arrays.toString(this.storage))
}
```



