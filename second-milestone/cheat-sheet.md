*   There is no native operator available in Scala. Instead, Scala uses a corresponding method which look like an operator.

*   In Scala, you are encouraged to use a val unless you really need to change the contents.

*   In Scala, the type of a variable or function is always written after the  
    name of the variable or function.

*   In scala it is optional to declare the type of val or var, It is evaluated from  
    the type of the expression with which you initialize it.

*   In scala semicolons ; are optional and only required if you have multiple statements on the same line.

*   In scala multiple variables or values can be declare and initialized together as :  
    var height, width = 100 // Sets both height and width to 100.

*   If the function is recursive, it is required to write return type, otherwise it's optional.

*   Avoid using return in a function.

*   If return statement is not there, value of the function is considered to be the return statement.

*   Every method parameter must be followed by type annotation.

*   Method names can contain characters like ‘.’ OR ‘\*’ OR ‘+’ as Scala doesn’t have any native operators \(all operators of Scala are methods\).

*   Scala re-uses Java’s types, and also “dresses them up” to make them nicer.

*   Method without parameters can be called without parentheses and method with one parameter can be call with . operator and without parenthesis.

*   We can call parameter less method with or without \(\), its always a good practise to use \(\) with a mutator methods\(methods which make change in object state\), and drop \(\) for accessor method \(method which does not change object state\).

*   Exceptions work just like in Java or C++, but you use a “pattern matching” syntax for catch. Scala has no checked exceptions.

*   Scala has no switch statement.

*   Scala has no break or continue statements, to break out of a loop, instead you can use some boolean flag  or use the break method in the Breaks object

*   Any parameters to a method can be used inside the method. One important characteristic of method parameters in Scala is that they are 'val', and not 'var'. so you can not reassign them. 

*   Auxiliary constructors in Scala start with def this\(...\). and every auxiliary constructor must invoke another constructor of
    the same class as its first action, The invoked constructor is either the primary constructor, or another auxiliary constructor. Thus the primary constructor is the single point of entry of a class
*   Camel-case names of fields, method parameters, local variables, and functions should start with lower case letter, for example: length, flatMap, and s.Although underscores are legal in identifiers, they are not used that often in Scala programs
*   Camel-case names of classes and traits should start with an upper case letter, for example: BigInt, List, and UnbalancedTreeMap.
*   The Scala convention is to use camel case for constants, such as XOffset, where first letter is capital. 
*   In any method invocation in Scala in which you’re passing in exactly one argument, you can opt to use curly braces to surround  the argument instead of parentheses.
