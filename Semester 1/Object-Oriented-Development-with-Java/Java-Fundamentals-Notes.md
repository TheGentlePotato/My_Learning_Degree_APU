Java Fundamentals Notes
1. Java Program Structure
What this concept means

A Java program organizes instructions inside classes and methods. The program starts execution from the main method. The Java compiler translates source code into bytecode which runs on the Java Virtual Machine.

Why programmers use this structure

The structure organizes code clearly and allows large programs to remain readable and maintainable. The JVM allows the same program to run across operating systems.

When programmers use this

Every Java application requires a class and a main method when execution begins from a standalone program.

Example
public class HelloWorld {

    public static void main(String[] args) {
        System.out.println("Hello World");
    }

}
Common errors

Missing class name
Missing main method
Incorrect method syntax
Missing braces

Example compile error

System.out.println("Hello World")

The semicolon is missing.

2. Variables
What a variable means

A variable stores a value which a program reads or modifies during execution.

Why programmers use variables

Programs require memory storage for data such as numbers, text, or results of calculations.

Situations where variables appear

Storing user input
Storing calculation results
Saving object attributes
Loop counters

Example
int age = 20;
String name = "Ali";
double price = 10.5;
Common errors

Using a variable before declaration

age = 20;

Correct version

int age = 20;

Another error occurs when assigning the wrong type.

int age = "20";
3. Data Types
What data types represent

A data type defines the type of value stored inside a variable.

Why data types exist

Different data types allow the program to manage memory efficiently and perform operations correctly.

Situations where data types matter

Numeric calculations
Character processing
Logical decision making

Primitive data types

int
Stores whole numbers.

double
Stores decimal numbers.

char
Stores a single character.

boolean
Stores logical values.

Example
int number = 10;
double price = 19.99;
char grade = 'A';
boolean passed = true;
Common errors

Incorrect data type assignment.

int price = 19.99;

Correct version

double price = 19.99;
4. Operators
What operators represent

Operators perform operations on values or variables.

Why programmers use operators

Programs require mathematical calculations, comparisons, and logical decisions.

Situations where operators appear

Calculations
Conditions
Loop control
Logical decision making

Arithmetic operators

Addition

int sum = a + b;

Subtraction

int result = a - b;

Multiplication

int product = a * b;

Division

int division = a / b;
Comparison operators

Used for decision making.

Example

if (age >= 18)
Logical operators

Combine multiple conditions.

Example

if (age > 18 && age < 30)
Common errors

Division by zero
Incorrect comparison operator
Assignment used instead of comparison

Incorrect

if (age = 18)

Correct

if (age == 18)
5. Conditional Statements
What conditional statements represent

Conditional statements control program flow based on conditions.

Why programmers use conditional logic

Programs must make decisions depending on input or program state.

Situations where conditions appear

Age verification
Login validation
Score grading
Menu selection

Example
int age = 18;

if (age >= 18) {
    System.out.println("Adult");
}
If else structure
if (score >= 50) {
    System.out.println("Pass");
} else {
    System.out.println("Fail");
}
Common errors

Missing braces
Wrong comparison operator
Incorrect logic conditions

6. Loops
What loops represent

Loops repeat a block of code multiple times.

Why programmers use loops

Programs often repeat actions such as processing lists, printing data, or performing calculations.

Situations where loops appear

Iterating through arrays
Repeating calculations
Processing user input

For loop

Used when the number of repetitions is known.

for (int i = 0; i < 5; i++) {
    System.out.println(i);
}
While loop

Used when repetition depends on a condition.

int i = 0;

while (i < 5) {
    System.out.println(i);
    i++;
}
Do while loop

Runs at least once before checking the condition.

int i = 0;

do {
    System.out.println(i);
    i++;
} while (i < 5);
Common errors

Infinite loop

while (true)

Missing loop update

while (i < 5) {
    System.out.println(i);
}
7. Classes
What a class represents

A class defines a blueprint for objects. It describes properties and behaviors.

Why programmers use classes

Classes organize complex programs and support object oriented programming.

Situations where classes appear

Student systems
Bank account systems
Game character objects

Example
class Student {

    String name;
    int age;

}
8. Objects
What an object represents

An object is an instance created from a class.

Why programmers use objects

Objects represent real world entities and allow programs to manage data in structured ways.

Situations where objects appear

User accounts
Students
Products

Example
Student s1 = new Student();

s1.name = "Ali";
s1.age = 20;
9. Constructors
What a constructor represents

A constructor initializes an object when it is created.

Why programmers use constructors

Constructors ensure objects receive initial values when creation occurs.

Example
class Student {

    String name;
    int age;

    Student(String n, int a) {

        name = n;
        age = a;

    }

}

Create object

Student s1 = new Student("Ali", 20);
10. Access Modifiers
What access modifiers represent

Access modifiers control which parts of the program access variables and methods.

Why programmers use access control

Encapsulation protects data and prevents unauthorized modification.

Types

public
private
protected

Example
class Student {

    private int age;

    public void setAge(int a) {
        age = a;
    }

    public int getAge() {
        return age;
    }

}
Summary

Java fundamentals include program structure, variables, data types, operators, conditional statements, loops, classes, objects, constructors, and access modifiers. These concepts form the foundation for object oriented programming and software development.
