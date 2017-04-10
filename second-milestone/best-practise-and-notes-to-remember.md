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
13. In Scala, arrays are zero based, and you can access an element by specifying  index in parentheses. So the first element in a Scala array named arg is arg\(0\), not arg\[0\], as in Java.
14. Method without parameters can be called without parentheses and method with one parameter can be call with . oprator and without parenthesis. 
15. Exceptions work just like in Java or C++, but you use a “pattern matching”
    syntax for catch. Scala has no checked exceptions.



