# Java Fundamentals Notes
## Object Oriented Development with Java  
### Semester 1 Reference Notes

---

## Table of Contents

1. [1. Java Program Structure](#1-java-program-structure)
2. [2. Variables](#2-variables)
3. [3. Data Types](#3-data-types)
4. [4. Operators](#4-operators)
5. [5. Conditional Statements](#5-conditional-statements)
6. [6. Loops](#6-loops)
7. [7. Classes and Objects](#7-classes-and-objects)
8. [8. Constructors](#8-constructors)
9. [9. Access Modifiers and Encapsulation](#9-access-modifiers-and-encapsulation)
10. [10. Program Errors](#10-program-errors)

---

# 1. Java Program Structure

## 1.1 Definition

A Java program organizes instructions into **classes** and **methods**.  
Program execution begins from the **main method**.

The Java compiler converts source code into **bytecode**, which runs inside the **Java Virtual Machine (JVM)**.

## 1.2 Purpose

The structure provides:

- **Code organization**
- **Better readability**
- **Platform independence**

Programs compiled into bytecode run on any system that has a JVM.

## 1.3 Example

```java
public class HelloWorld {

    public static void main(String[] args) {

        System.out.println("Hello World");

    }

}
```

## 1.4 Explanation

**public**  
Defines the access level of the class.

**class**  
Defines the blueprint of the program.

**main()**  
Entry point of program execution.

**System.out.println()**  
Displays output on the console.

---

# 2. Variables

## 2.1 Definition

A **variable** is a named storage location in memory used to store data during program execution.

## 2.2 Purpose

Variables allow programs to:

- store user input
- store calculation results
- maintain program state

## 2.3 Example

```java
public class VariableExample {

    public static void main(String[] args) {

        int age = 20;
        String name = "Ali";
        double price = 10.50;

        System.out.println(name);
        System.out.println(age);
        System.out.println(price);

    }

}
```

## 2.4 Explanation

**int age** stores a whole number.

**String name** stores text.

**double price** stores decimal numbers.

Variables store information which can change during program execution.

---

# 3. Data Types

## 3.1 Definition

A **data type** specifies the type of value stored in a variable.

## 3.2 Purpose

Data types help Java determine:

- how much memory is required
- what operations are allowed
- how the value is interpreted

## 3.3 Primitive Data Types

| Data Type | Description |
|-----------|-------------|
| int | Whole numbers |
| double | Decimal numbers |
| char | Single character |
| boolean | True or False |

## 3.4 Example

```java
public class DataTypeExample {

    public static void main(String[] args) {

        int number = 10;
        double price = 19.99;
        char grade = 'A';
        boolean passed = true;

        System.out.println(number);
        System.out.println(price);
        System.out.println(grade);
        System.out.println(passed);

    }

}
```

---

# 4. Operators

## 4.1 Definition

Operators perform calculations and logical comparisons.

## 4.2 Purpose

Operators allow programs to:

- perform arithmetic calculations
- compare values
- control program logic

## 4.3 Arithmetic Operators

| Operator | Function |
|---------|---------|
| + | Addition |
| - | Subtraction |
| * | Multiplication |
| / | Division |
| % | Modulus |

## 4.4 Example

```java
public class OperatorExample {

    public static void main(String[] args) {

        int a = 10;
        int b = 3;

        int sum = a + b;
        int difference = a - b;
        int product = a * b;
        int division = a / b;
        int remainder = a % b;

        System.out.println(sum);
        System.out.println(difference);
        System.out.println(product);
        System.out.println(division);
        System.out.println(remainder);

    }

}
```

---

# 5. Conditional Statements

## 5.1 Definition

Conditional statements allow the program to make decisions based on conditions.

## 5.2 Purpose

Programs often need to perform different actions depending on a situation.

Conditional statements evaluate conditions and determine which code block runs.

## 5.3 Example

```java
public class ConditionalExample {

    public static void main(String[] args) {

        int score = 60;

        if (score >= 50) {
            System.out.println("Pass");
        }
        else {
            System.out.println("Fail");
        }

    }

}
```

## 5.4 Explanation

**if statement** checks whether a condition is true.

If true, the program executes the first block.

If false, the program executes the **else block**.

---

# 6. Loops

## 6.1 Definition

A **loop** repeatedly executes a block of code while a condition remains true.

## 6.2 Purpose

Loops help perform repetitive tasks efficiently.

Without loops, the same code would need to be written multiple times.

## 6.3 Example

```java
public class LoopExample {

    public static void main(String[] args) {

        for (int i = 0; i < 5; i++) {

            System.out.println(i);

        }

    }

}
```

## 6.4 Explanation

The loop starts with **i = 0**.

The loop continues while **i < 5**.

After each iteration, **i increases by 1**.

---

# 7. Classes and Objects

## 7.1 Definition

A **class** acts as a blueprint.

An **object** represents an instance created from a class.

## 7.2 Purpose

Classes organize data and behavior into reusable structures.

Objects represent real-world entities.

## 7.3 Example

```java
class Student {

    String name;
    int age;

}

public class Main {

    public static void main(String[] args) {

        Student s1 = new Student();

        s1.name = "Ali";
        s1.age = 20;

        System.out.println(s1.name);
        System.out.println(s1.age);

    }

}
```

---

# 8. Constructors

## 8.1 Definition

A **constructor** initializes an object when it is created.

## 8.2 Purpose

Constructors ensure that objects start with proper values.

## 8.3 Example

```java
class Student {

    String name;
    int age;

    Student(String n, int a) {

        name = n;
        age = a;

    }

}

public class Main {

    public static void main(String[] args) {

        Student s1 = new Student("Ali", 20);

        System.out.println(s1.name);
        System.out.println(s1.age);

    }

}
```

---

# 9. Access Modifiers and Encapsulation

## 9.1 Definition

Access modifiers control visibility of variables and methods.

Encapsulation protects data by restricting direct access.

## 9.2 Access Modifiers

| Modifier | Access |
|--------|--------|
| public | Accessible everywhere |
| private | Accessible only inside the class |
| protected | Accessible in same package and subclasses |

## 9.3 Example

```java
class Student {

    private int age;

    public void setAge(int a) {
        age = a;
    }

    public int getAge() {
        return age;
    }

}

public class Main {

    public static void main(String[] args) {

        Student s1 = new Student();

        s1.setAge(20);

        System.out.println(s1.getAge());

    }

}
```

---

# 10. Program Errors

## 10.1 Compile Time Error

Errors detected by the compiler before execution.

Example

```java
public class ErrorExample {

    public static void main(String[] args) {

        System.out.println("Hello World")

    }

}
```

Missing semicolon causes a compile error.

---

## 10.2 Runtime Error

Errors occurring during execution.

Example

```java
public class RuntimeExample {

    public static void main(String[] args) {

        int number = 10 / 0;

        System.out.println(number);

    }

}
```

Division by zero produces an **ArithmeticException**.

---

## 10.3 Logical Error

The program runs but produces incorrect results.

Example

```java
public class LogicalErrorExample {

    public static void main(String[] args) {

        int score = 50;

        if (score > 50) {
            System.out.println("Pass");
        }

    }

}
```

The condition should be **>= 50**.

---

## 11. Conclusion

These notes introduced the fundamental concepts of Java programming, including program structure, variables, data types, operators, conditional statements, and loops, which form the basic logic of a program. The material also covered key object oriented concepts such as classes, objects, constructors, and encapsulation, explaining how Java organizes data and behavior into structured and reusable components. In addition, different types of program errors, including compile time errors, runtime errors, and logical errors, were discussed to highlight common issues that occur during program development. Together, these concepts provide a foundational understanding of Java programming and prepare learners for more advanced object oriented programming topics.














---
