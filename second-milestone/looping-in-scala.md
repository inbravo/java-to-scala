| Topic | Looping |
| :--- | :--- |
| Time Required |  |
|  |  |
|  | LoopTest.scala |

Scala If Else structure is same as Java if else. If Else in Scala is used as an expression rather than a control structure because if..else in Scala returns a value.

`var maxoftwo = if(x>y) x else y`

if "else" part if not defined in if-else statement, return type would be `Any`.

`val result = if(a%2) return "even"`

`//here else not defined so the return type would be "Any".`

`val result = if(a%2) return "even" else "odd"`

`//here return type  would be Java.lang.String`

The if statement without an else is equivalent to

`if (x > 0) 1 else ()`

Scala has same control structure like Java as while, do-while, for. Syntax for while and do-while in scala is same is Java.

```
while(condition){ 
    statement(s)
    }
```

```
do{    
    statement(s)
  }while(condition)
```

Syntax for for is different in scala in compare to java

```
for(variable <- list) statement

//OR
for(variable <- range) statement

//OR
for(variable <- [range or list] if condition; if condition; ...) statement
```

```
e.g.
var list = List(1,2,3,4,5,6,7,8,9,10)
//print odd number in list except 7
for(element <- list if element%2 != 0; if element!= 7) println("Element of list is : " + element)
```



