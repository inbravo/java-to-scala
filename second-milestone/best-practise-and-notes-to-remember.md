1. There is no native operator available in Scala. Instead, Scala uses a corresponding method which look like an operator.

2. In Scala, you are encouraged to use a val unless you really need to change the contents.

3. In Scala, the type of a variable or function is always written after the  
    name of the variable or function.

4. In scala it is optional to declare the type of val or var, It is evaluated from  
    the type of the expression with which you initialize it.

5. In scala semicolons ; are optional and only required if you have multiple statements on the same line.

6. In scala multiple variables or values can be declare and initialized together as :  
    var height, width = 100 // Sets both height and width to 100.

7. if the function is recursive, it is required to write return type, otherwise it's optional.

8. Avoid using return in a function.

9. if return statement is not there, value of the function is considered to be the return statement.

10. Every method parameter must be followed by type annotation.

11. Method names can contain characters like ‘.’ OR ‘\*’ OR ‘+’ as Scala doesn’t have any native operators \(all operators of Scala are methods\).

12. Scala re-uses Java’s types, and also “dresses them up” to make them nicer.

13. Method without parameters can be called without parentheses and method with one parameter can be call with . operator and without parenthesis. 
14. We can call parameter less method with or without \(\), its always a good practise to use \(\) with a mutator methods\(methods which make change in object state\), and drop \(\) for accessor method \(method which does not change object state\).
15. Exceptions work just like in Java or C++, but you use a “pattern matching” syntax for catch. Scala has no checked exceptions.
16. Scala has no switch statement.
17. Scala has no break or continue statements, to break out of a loop, instead you can use some boolean flag  or use the break method in the Breaks object
18. Any parameters to a method can be used inside the method. One important     characteristic of method parameters in Scala is that they are vals,     not vars. so you can not reassign them. 



