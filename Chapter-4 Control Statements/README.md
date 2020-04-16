Chapter : 04 Control Statements
Part 1 : Assigments, ++ and -- Operators

# 4.1) Introduction:
When writing a program, you also should understand the available building blocks and employ proven program construction techniques.We will discuss Java’s if statement in ad ditional detail, and introduce the if ... else and while statements—all of these building blocks allow you to specify the logic required for methods to perform their tasks.

# 4.2) Algorithm 
Any computing problem can be solved by executing a series of actions in a specific order.
A *procedure* for solving a problem in terms of
1. the actions to execute and
2. the order in which these actions execute
is called an **algorithm.**

# 4.3) Pseudocode
Pseudocode is an informal language that helps you develop algorithms without having to worry about the strict details of Java language syntax. The style of pseudocode we present consists purely of characters, so you can type pseudocode conveniently, using any text-editor program. Pseudocode normally describes only statements representing the actions that occur after you convert a program from pseudocode to Java and the program is run on a computer. Such actions might include input, output or calculations. In our pseudocode, we typically do not include variable declarations, but some programmers choose to list variables and mention their purposes.

# 4.4) Control Statements
Normally, statements in a program are executed one after the other in the order in which they’re written. This process is called sequential execution.

**[Note: Java does not have a goto statement; however, the word goto is reserved by Java and should not be used as an identifier in programs.]**

All programs could be written in terms of only three control structures—the sequence structure, the selection structure and the repetition structure.

*Sequence Structure in Java*

The sequence structure is built into Java.the computer executes Java statements one after the other in the order in which they’re written—that is, in sequence. The activity diagram illustrates a typical sequence structure in which
two calculations are performed in order. Java lets you have as many actions as you want in a sequence structure.

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-4%20Control%20Statements/sequence-structure.png">
</p>

A UML activity diagram models the workflow (also called the activity) of a portion of a software system. Activity diagrams are composed of symbols, such as action-state symbols (rectangles with their left and right sides replaced with outward arcs), diamonds and small circles. These symbols are connected by transition arrows, which represent the flow of the activity that is, the order in which the actions should occur.

*Selection Statements in Java*

Java has three types of selection statements.The if statement either performs (selects) an action, if a condition is true, or skips it, if the condition is false. The if ... else statement performs an action if a condition is true and performs a different action if the condition is false. The switch statement performs one of many different actions, depending on the value of an expression.

*Repetition Statements in Java*

Java provides three repetition statements (also called iteration statements or looping statements) that enable programs to perform statements repeatedly as long as a condition (called the loop-continuation condition) remains true.

# 4.4) if Single-Selection Statement
Programs use selection statements to choose among alternative courses of action. For example, suppose that the passing grade on an exam is 60. The pseudocode statement:
```
        If student’s grade is greater than or equal to 60
        Print “Passed”
```
determines whether the condition “student’s grade is greater than or equal to 60” is true. If so, “Passed” is printed, and the next pseudocode statement in order is “performed.”
The preceding pseudocode If statement may be written in Java as
```
        if (studentGrade >= 60)
        System.out.println("Passed");
```

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-4%20Control%20Statements/single-selection.png">
</p>

# 4.5) if ... else Double-Selection Statement

The if single-selection statement performs an indicated action only when the condition is true ; otherwise, the action is skipped. The if ... else double-selection statement allows you to specify an action to perform when the condition is true and another action when the condition is false. For example, the pseudocode statement:

```
        If student’s grade is greater than or equal to 60
        Print “Passed”
        Else
        Print “Failed”
```
prints “Passed” if the student’s grade is greater than or equal to 60, but prints “Failed” if it’s less than 60. In either case, after printing occurs, the next pseudocode statement in sequence is “performed.” The preceding If...Else pseudocode statement can be written in Java as:

```
        if (grade >= 60)
        System.out.println("Passed");
        else
        System.out.println("Failed");
```

*Nested if ... else Statements*
A program can test multiple cases by placing if ... else statements inside other if ... else statements to create nested if ... else statements.
```
        If student’s grade is greater than or equal to 90
            Print “A”
        else
            If student’s grade is greater than or equal to 80
            Print “B”
        else
            If student’s grade is greater than or equal to 70
            Print “C”
        else
            If student’s grade is greater than or equal to 60
            Print “D”
        else
            Print “F”
```
This pseudocode may be written in Java as:

```
        if (studentGrade >= 90)
            System.out.println("A");
        else
            if (studentGrade >= 80)
                System.out.println("B");
           else
                if (studentGrade >= 70)
                    System.out.println("C");
                else
                    if (studentGrade >= 60)
                        System.out.println("D");
                       else
                          System.out.println("F");
```


*Dangling- else Problem*
The Java compiler always associates an else with the immediately preceding if unless told to do otherwise by the placement of braces ( { and } ). This behavior can lead to what is referred to as the dangling- else problem. For example,

``` 
        if (x > 5)
             if (y > 5)
                 System.out.println("x and y are > 5");
            else
                System.out.println("x is <= 5");
```

appears to indicate that if x is greater than 5 , the nested if statement determines whether is also greater than 5 . If so, the string "x and y are > 5" is output. Otherwise, it appears y that if x is not greater than 5 , the else part of the if ... else outputs the string "x is <= 5" . Beware! This nested if ... else statement does not execute as it appears. The compiler actually interprets the statement as

```
        if (x > 5)
        if (y > 5)
            System.out.println("x and y are > 5");
        else
            System.out.println("x is <= 5");
```

*Conditional Operator ( ?: )*

Java provides the **conditional operator ( ?: )** that can be used in place of an if ... else statement. This can make your code shorter and clearer. The conditional operator is Java’s only **ternary operator** (i.e., an operator that takes three operands). Together, the operands and the ?: symbol form a **conditional expression.** The first operand (to the left of the ? ) is a **boolean expression** (i.e., a condition that evaluates to a boolean value— **true or false** ), the second operand (between the ? and : ) is the value of the conditional expression if the boolean expression is true and the third operand (to the right of the : ) is the value of the conditional expression if the boolean expression evaluates to false . For ex-
ample, the statement.

```
        System.out.println(studentGrade >= 60 ? "Passed" : "Failed");
```

# 4.6) Compound Assignment Operators
The compound assignment operators abbreviate assignment expressions. Statements like:

        variable = variable operator expression ;
where operator is one of the binary operators + , - , * , / or % (or others we discuss later in
the text) can be written in the form  

        variable operator = expression ;
For example, you can abbreviate the statement    

        c = c + 3;
with the **addition compound assignment operator**, += , as    

        c += 3;
The += operator adds the value of the expression on its right to the value of the variable on its left and stores the result in the variable on the left of the operator. Thus, the assignment expression c += 3 adds 3 to c .    

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-4%20Control%20Statements/arithmetic-compund.png">
</p>

# 4.7) Increment and Decrement Operators
Java provides two unary operators for adding 1 to or subtracting 1 from the value of a numeric variable. These are the unary increment operator, ++ , and the unary **decrement operator,** -- . A program can increment by 1 the value of a variable
called c using the **increment operator,** ++ , rather than the expression c = c + 1 or c += 1 . An increment or decrement operator that’s prefixed to (placed before) a variable is referred to as the **prefix increment** or **prefix decrement operator,** respectively. An increment or decrement operator that’s postfixed to (placed after) a variable is referred to as the **postfix increment** or **postfix decrement operator,** respectively.

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-4%20Control%20Statements/increment-decrement.png">
</p>

# 4.8) Operator Precedence and Associativity

Figure shows the precedence and associativity of the operators we’ve introduced. They’re shown from top to bottom in decreasing order of precedence. The second column describes the associativity of the operators at each level of precedence. The conditional operator ( ?: ); the unary operators increment ( ++ ), decrement ( -- ), plus ( + ) and minus ( - );
the cast operators and the assignment operators = , += , -= , *= , /= and %= associate from right to left. All the other operators in the operator precedence chart in  associate from left to right. The third column lists the type of each group of operators.

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-4%20Control%20Statements/precedence.png">
</p>

# 4.9) Primitive Types

Like its predecessor languages C and C++, Java requires all variables to have a type. For this reason, Java is referred
to as a **strongly typed language.**
In C and C++, programmers frequently have to write separate versions of programs to support different computer platforms, because the primitive types are not guaranteed to be identical from computer to computer. For example, an int on one machine might be represented by 16 bits (2 bytes) of memory, on a second machine by 32 bits (4 bytes), and on another machine by 64 bits (8 bytes). In Java, int values are always 32 bits (4 bytes).

The variables of primitive types declared outside of a method as instance variables of a class are automatically assigned default values unless explicitly initialized. Instance variables of types char , byte , short , int , long , float and double are all given the value 0 by default. Instance variables of type boolean are given the value false
by default. Reference-type instance variables are initialized by default to the value null .
