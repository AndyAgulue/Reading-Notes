# Java Basics [The Java Tutorials](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/index.html)

## Variables

The Java programming language uses both "fields" and "variables" as part of its terminology. Instance variables (non-static fields) are unique to each instance of a class. Class variables (static fields) are fields declared with the static modifier; there is exactly one copy of a class variable, regardless of how many times the class has been instantiated. Local variables store temporary state inside a method. Parameters are variables that provide extra information to a method; both local variables and parameters are always classified as "variables" (not "fields"). When naming your fields or variables, there are rules and conventions that you should (or must) follow.

The eight primitive data types are: byte, short, int, long, float, double, boolean, and char. The java.lang.String class represents character strings. The compiler will assign a reasonable default value for fields of the above types; for local variables, a default value is never assigned. A literal is the source code representation of a fixed value. An array is a container object that holds a fixed number of values of a single type. The length of an array is established when the array is created. After creation, its length is fixed.

## Operators

### Simple Assignment Operator

**=**       Simple assignment operator

### Arithmetic Operators

**+** Additive operator (also used for String concatenation)

**-** Subtraction operator

**       Multiplication operator

**/**       Division operator

**%**       Remainder operator

### Unary Operators

**+**       Unary plus operator; indicates positive value (numbers are positive without this, however)       
        
**-**       Unary minus operator; negates an expression
        
**++**      Increment operator; increments a value by 1
        
**--**      Decrement operator; decrements a value by 1
        
**!**       Logical complement operator; inverts the value of a boolean
        
### Equality and Relational Operators

**==**      Equal to
**!=**      Not equal to
**>**      Greater than
**>=**      Greater than or equal to
**<**       Less than
**<=**      Less than or equal to

### Conditional Operators

**&&**      Conditional-AND
**||**     Conditional-OR
**?:**      Ternary (shorthand for if-then-else statement)
        
### Type Comparison Operator

**instanceof**      Compares an object to  a specified type 
               
### Bitwise and Bit Shift Operators

**~**       Unary bitwise complement

**<<**      Signed left shift

**>>**      Signed right shift

**>>>**     Unsigned right shift

**&**       Bitwise AND

**^**       Bitwise exclusive OR

**|**       Bitwise inclusive OR

## Control Flow Statements

The if-then statement is the most basic of all the control flow statements. It tells your program to execute a certain section of code only if a particular test evaluates to true. The if-then-else statement provides a secondary path of execution when an "if" clause evaluates to false. Unlike if-then and if-then-else, the switch statement allows for any number of possible execution paths. The while and do-while statements continually execute a block of statements while a particular condition is true. The difference between do-while and while is that do-while evaluates its expression at the bottom of the loop instead of the top. Therefore, the statements within the do block are always executed at least once. The for statement provides a compact way to iterate over a range of values. It has two forms, one of which was designed for looping through collections and arrays.