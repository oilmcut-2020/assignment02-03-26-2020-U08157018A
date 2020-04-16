
**Chapter : 02 Introduction to Java Applications ; Input/Output & Operators**

Java is a high-level programming language originally developed by Sun Microsystems and released in 1995.Java runs on a variety of platforms, such as Windows, Mac OS, and the various versions of UNIX. 
# Your First Program in Java: Printing a Line of Text

A Java application is a computer program that executes when you use the java command to launch the Java Virtual Machine (JVM).First we consider a simple application that displays a line of text.

Program :
INPUT:

```
// Text-printing program.

public class Welcome1
{
// main method begins execution of Java application
public static void main(String[] args)
{
System.out.println("Welcome to Java Programming!");
} // end method main
} // end class Welcome1
```
OUTPUT :
```
Welcome to Java Programming!
```

### Commenting Your Programs

We insert comments to document programs and improve their readability. The Java com-
piler ignores comments, so they do not cause the computer to perform any action when the
program is run.
Comments can be used to explain Java code, and to make it more readable. It can also be used to prevent execution when testing alternative code.
Single-line comments start with two forward slashes (//).
Any text between // and the end of the line is ignored by Java (will not be executed).
This example uses a single-line comment before a line of code:

    // This is a comment
    System.out.println("Hello World");
    
 ### Java Multi-line Comments
Java also has traditional comments. Multi-line comments start with /* and ends with */.
These begin and end with delimiters, /* and */. The compiler ignores all text between the
delimiters. Java incorporated traditional comments and end-of-line comments from the C
and C++ programming languages, respectively. We prefer using // comments
This example uses a multi-line comment (a comment block) to explain the code:

    /* The code below will print the words Hello World
    to the screen, and it is amazing */
    System.out.println("Hello World");
 
 Java provides comments of a third type— **Javadoc comments**. These are delimited by
/** and */ . The compiler ignores all text between the delimiters. Javadoc comments
enable you to embed program documentation directly in your programs. Such comments
are the preferred Java documenting format in industry. 

### Declaring a Class
```
public class Welcome1
```
begins a class declaration for class Welcome1 . Every Java program consists of at least one class that you (the programmer) define. The class keyword introduces a class declaration and is immediately followed by the class name ( Welcome1 ). Keywords (sometimes called reserved words) are reserved for use by Java and are always spelled with all lowercase letters.

### Declaring a Method
```
// main method begins execution of Java application
```
Is an end-of-line comment indicating the purpose of lines 7–10 of the program.
```
public static void main(String[] args)
```
is the starting point of every Java application. The parentheses after the identifier main indicate that it’s a program building block called a **method.**

### Performing Output with System.out.println

```
System.out.println("Welcome to Java Programming!");
```
The System.out object—which is predefined for you—is known as the standard output object. It allows a Java application to display information in the command window from which it executes. Method System.out.println displays (or prints) a line of text in the command window. The entire line 9, including System.out.println , the argument "Welcome to Java
Programming!" in the parentheses and the **semicolon ( ; )**, is called a **statement**. A method typically contains one or more statements that perform its task. Most statements end with a semicolon. When the statement in line 9 executes, it displays Welcome to Java Programming! in the command window.

### Displaying Multiple Lines of Text with a Single Statement
A single statement can display multiple lines by using newline characters, which indicate to System.out ’s print and println methods when to position the output cursor at the beginning of the next line in the command window.

INPUT:

```
// Printing multiple lines of text with a single statement.

public class Welcome3
{
// main method begins execution of Java application
public static void main(String[] args)
{
System.out.println("Welcome \n to \n Java \n Programming!");
} // end method main
} // end class Welcome3
```
OUTPUT:
```
Welcome
to
Java
Programming!
```
In line 8 : 
        
        System.out.println("Welcome\nto\nJava\nProgramming!");
        
displays four lines of text in the command window. Normally, the characters in a string are displayed exactly as they appear in the double quotes.  The backslash ( \ ) is an escape character, which has special meaning to System.out ’s print and println methods. When a backslash appears in a string, Java combines it with the next character to form an escape sequence— \n represents the newline character.

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-2%20Java%20Applications/comments.png">
</p>

# Displaying Text with printf

The System.out.printf method ( f means “formatted”) displays formatted data. It uses this method to output on two lines the strings "Welcome to" and "Java Programming!

INPUT :
```
// Displaying multiple lines with method System.out.printf.

public class Welcome4
{
// main method begins execution of Java application
public static void main(String[] args)
{
System.out.printf("%s%n%s%n",
"Welcome to", "Java Programming!");
} // end method main
} // end class Welcome4
```
OUTPUT :
```
Welcome to
Java Programming!
```
In line 8-9 

```
System.out.printf("%s%n%s%n",
"Welcome to", "Java Programming!");
```
call method System.out.printf to display the program’s output. The method call specifies three arguments. When a method requires multiple arguments, they’re placed in a **comma-separated list**. Calling a method is also referred to as invoking a method.
Format specifiers begin with a percent sign ( % ) followed by a character that represents the data type. For example, the format specifier %s is a placeholder for a string.

# Operators 

Programs remember numbers and other data in the computer’s memory and access that data through program elements called variables.
INPUT :

```
// Addition program that inputs two numbers then displays their sum.

import java.util.Scanner; // program uses class Scanner
public class Addition
{
// main method begins execution of Java application
public static void main(String[] args)
{
// create a Scanner to obtain input from the command window
Scanner input = new Scanner(System.in);

int number1; // first number to add
int number2; // second number to add
int sum; // sum of number1 and number2

System.out.print("Enter first integer: "); // prompt
number1 = input.nextInt(); // read first number from user
System.out.print("Enter second integer: "); // prompt
number2 = input.nextInt(); // read second number from user

sum = number1 + number2; // add numbers, then store total in sum
System.out.printf("Sum is %d%n", sum); // display sum
} // end method main
} // end class Addition
```

OUTPUT :
```
Enter first integer: 45
Enter second integer: 72
Sum is 117
```

# Import Declarations
These classes are grouped into packages—named groups of related classes—and are collectively referred to as the Java class library, or the Java Application Programming Interface (Java API).

    import java.util.Scanner; // program uses class Scanner
    
is an import declaration that helps the compiler locate a class that’s used in this program. It indicates that the program uses the predefined Scanner class (discussed shortly) from the package named java.util .

### Declaring and Creating a Scanner to Obtain User Input from the Keyboard
       
A variable is a location in the computer’s memory where a value can be stored for use later in a program. All Java variables must be declared with a name and a type before they can be used. A variable’s name enables the program to access the value of the variable in memory.      

    Scanner input = new Scanner(System.in);
    
is a **variable declaration** statement that specifies the name ( input ) and type ( Scanner ) of a variable that’s used in this program. A **Scanner** enables a program to read data (e.g., numbers and strings) for use in a program. The standard input object, System.in , enables applications to read bytes of data typed by the user. The Scanner translates these bytes into types (like int s) that can be used in a program. 

### Declaring Variables to Store Integers

The variable declaration statements in lines:
```    
  int number1; // first number to add
  int number2; // second number to add
  int sum; // sum of number1 and number2
```

The types int , float , double and char are called primitive types. Primitive-type names are keywords and must appear in all lowercase letters.

# Memory Concepts

Variable names such as number1 , number2 and sum actually correspond to locations in the computer’s memory. Every variable has a **name, a type, a size (in bytes) and a value.**

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-2%20Java%20Applications/memory.png">
</p>

    number1 = input.nextInt(); // read first number from user
    number2 = input.nextInt(); // read second number from user
    
    sum = number1 + number2; // add numbers, then store total in sum  
    
The values of number1 and number2 appear exactly as they did before they were used in the calculation of sum . These values were used, but not destroyed, as the computer performed the calculation. When a value is read from a memory location, the process is **non destructive.**

# Arithmetic

- The arithmetic operators (p. 51) are + (addition), - (subtraction), * (multiplication), / (division)
and % (remainder).

- Integer division  yields an integer quotient.

- The remainder operator,% yields the remainder after division.

- Arithmetic expressions must be written in straight-line form.

- If an expression contains nested parentheses, the innermost set is evaluated first.

- Java applies the operators in arithmetic expressions in a precise sequence determined by the rules
of operator precedence.

- When we say that operators are applied from left to right, we’re referring to their associativity.Some operators associate from right to left.

- Redundant parentheses can make an expression clearer.

<p align="center">
  <img src="https://github.com/oilmcut-2020/JavaClass/blob/master/Chapter-2%20Java%20Applications/arithmetic.png">
</p>

# Decision Making: Equality and Relational Operators

- The if statement (p. 54) makes a decision based on a condition’s value (true or false).

- Conditions in if statements can be formed by using the equality ( == and != ) and relational ( > ,< , >= and <= ) operators 

- An if statement begins with keyword if followed by a condition in parentheses and expects one tatement in its body.

- The empty statement (p. 57) is a statement that does not perform a task.

 



