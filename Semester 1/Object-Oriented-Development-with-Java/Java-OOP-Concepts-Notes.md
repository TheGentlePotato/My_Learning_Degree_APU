# Java Object Oriented Programming Revision Notes
## Comprehensive OOP Study Notes for Exam Revision

---

## Table of Contents

1. [Java Program Structure](#1-java-program-structure)
2. [Classes and Objects](#2-classes-and-objects)
3. [Methods](#3-methods)
4. [Constructors](#4-constructors)
5. [Access Modifiers and Encapsulation](#5-access-modifiers-and-encapsulation)
6. [Inheritance](#6-inheritance)
7. [Polymorphism](#7-polymorphism)
8. [Abstract Classes](#8-abstract-classes)
9. [Interfaces](#9-interfaces)
10. [Exception Handling](#10-exception-handling)
11. [Arrays](#11-arrays)
12. [Parameter Passing](#12-parameter-passing)
13. [Compilation Errors and Code Analysis](#13-compilation-errors-and-code-analysis)

---

# 1. Java Program Structure

## 1.1 Definition

A Java program is organized into classes, methods, and statements. Every Java application begins execution from the `main` method. The `main` method is the entry point of the program.

Java source code is written in `.java` files. The Java compiler converts source code into bytecode. This bytecode is executed by the Java Virtual Machine, which allows Java programs to run on different platforms.

## 1.2 Purpose

Java program structure provides:

- clear code organization
- easier reading and maintenance
- a standard way for the compiler and JVM to understand the program
- platform independence through bytecode and JVM execution

## 1.3 Main Components

A basic Java program usually contains:

- package declaration, if used
- class declaration
- fields or variables
- methods
- main method
- statements inside methods

## 1.4 Example

```java
public class HelloWorld {

    public static void main(String[] args) {

        System.out.println("Hello World");

    }

}
```

## 1.5 Explanation

`public`  
Access modifier. It allows the class or method to be accessible from outside the class.

`class`  
Defines a class, which acts as a blueprint.

`HelloWorld`  
Class name. If the class is public, the file name must be `HelloWorld.java`.

`public static void main(String[] args)`  
The exact method signature for the entry point of a Java application.

`System.out.println()`  
Prints output to the console.

## 1.6 Important Rules

- All Java code must be inside a class.
- Program execution starts from `main`.
- `String` must use uppercase `S`.
- `main` must be `public static void`.
- If a class is public, the file name must match the class name exactly.

## 1.7 Common Exam Traps

- writing code outside a class
- wrong `main` method syntax
- using `string[] args` instead of `String[] args`
- forgetting `static`
- public class name not matching file name

---

# 2. Classes and Objects

## 2.1 Definition

A class is a blueprint used to define data and behavior.

An object is an instance created from a class.

A class tells Java what properties and actions an object should have. An object is the real entity created from the class.

## 2.2 Purpose

Classes and objects allow programs to model real world entities in a structured way.

Examples:

- `Student`
- `Car`
- `BankAccount`
- `Book`

## 2.3 Class Components

A class may contain:

- fields
- methods
- constructors

## 2.4 Fields

Fields are variables declared inside the class but outside methods. They store object data.

## 2.5 Methods

Methods define actions the object can perform.

## 2.6 Constructors

Constructors initialize object values when the object is created.

## 2.7 Example

```java
class Student {

    String name;
    int age;

}
```

## 2.8 Creating an Object

```java
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

## 2.9 Explanation

`Student`  
Class name.

`String name` and `int age`  
Fields of the class.

`Student s1`  
Reference variable.

`new Student()`  
Creates a new object in memory.

`s1.name = "Ali"`  
Stores a value in the object's field.

## 2.10 Important Rules

- A class is not an object.
- `new` creates an object.
- Each object gets its own copy of instance variables.
- Reference variables point to objects.

## 2.11 Instance Variables

Instance variables belong to each object.

Example:

```java
class Student {

    String name;

}
```

```java
Student s1 = new Student();
Student s2 = new Student();

s1.name = "Ali";
s2.name = "John";
```

Here, `s1` and `s2` are different objects. Each object has its own `name`.

## 2.12 Common Exam Traps

- confusing fields with local variables
- thinking `Student s1` creates the object, when only `new Student()` does
- thinking all objects share one copy of instance variables

---

# 3. Methods

## 3.1 Definition

A method is a block of code that performs a specific task.

Methods improve code organization, reuse, and readability.

## 3.2 Basic Structure

A method declaration contains:

- access modifier
- optional keyword such as `static`
- return type
- method name
- parameter list
- method body

## 3.3 General Syntax

```java
accessModifier returnType methodName(parameters) {

    // method body

}
```

## 3.4 Example

```java
public class MathExample {

    public static int add(int a, int b) {

        return a + b;

    }

    public static void main(String[] args) {

        int result = add(5, 3);

        System.out.println(result);

    }

}
```

## 3.5 Explanation

`public`  
Access modifier.

`static`  
Method belongs to the class, not an object.

`int`  
Return type.

`add`  
Method name.

`int a, int b`  
Parameters.

`return a + b`  
Returns a value.

## 3.6 Return Type

The return type states what value the method sends back.

Examples:

- `int`
- `double`
- `String`
- `boolean`
- `void`

`void` means the method does not return a value.

## 3.7 Parameters and Arguments

Parameters are variables in the method declaration.

Arguments are the actual values passed during the method call.

Example:

```java
public static int add(int a, int b) {
    return a + b;
}
```

```java
add(5, 3);
```

Here:

- `a` and `b` are parameters
- `5` and `3` are arguments

## 3.8 Method Overloading

Method overloading means multiple methods have the same name but different parameter lists.

This is compile time polymorphism.

```java
class MathUtil {

    int add(int a, int b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }

    double add(double a, double b) {
        return a + b;
    }

}
```

## 3.9 Rules of Overloading

- method name must be the same
- parameter list must differ
- return type alone cannot create an overload

Invalid example:

```java
class Test {

    int add(int a, int b) {
        return a + b;
    }

    double add(int a, int b) {
        return a + b;
    }

}
```

This causes a compile error because only the return type changed.

## 3.10 Static Methods

Static methods belong to the class, not to objects.

```java
class Tool {

    static void show() {
        System.out.println("Static method");
    }

}
```

Call:

```java
Tool.show();
```

## 3.11 Static Method Rules

- can be called using the class name
- can be called without creating an object
- cannot directly access instance members without an object

## 3.12 Common Exam Traps

- confusing return type and method name
- forgetting parentheses in method calls
- mismatch between method declaration and method call
- trying to call instance methods directly from a static method
- thinking parameter names affect overloading, when only parameter types and count matter

---

# 4. Constructors

## 4.1 Definition

A constructor is a special member used to initialize an object when it is created.

It runs automatically when `new` is used.

## 4.2 Constructor Rules

- constructor name must match the class name
- constructor has no return type, not even `void`
- constructor runs automatically during object creation

## 4.3 Basic Example

```java
class Car {

    String brand;

    Car() {
        brand = "Toyota";
    }

}
```

```java
Car c = new Car();
System.out.println(c.brand);
```

Output:

```text
Toyota
```

## 4.4 Purpose

Constructors are used to:

- assign default values
- assign user provided values
- ensure objects start in a valid state

## 4.5 Default Constructor

If no constructor is written, Java provides a default no argument constructor automatically.

Example:

```java
class Student {

    String name;

}
```

This class can still do:

```java
Student s = new Student();
```

Java provides:

```java
Student() {
}
```

## 4.6 Important Rule

If you write any constructor, Java does not provide the default constructor automatically.

Example:

```java
class Car {

    Car(int speed) {
    }

}
```

This works:

```java
Car c = new Car(100);
```

This does not work:

```java
Car c = new Car();
```

## 4.7 Parameterized Constructor

A parameterized constructor receives values during object creation.

```java
class Student {

    String name;
    int age;

    Student(String n, int a) {
        name = n;
        age = a;
    }

}
```

```java
Student s = new Student("Ali", 20);
```

## 4.8 Using `this`

When parameter names are the same as field names, `this` is used to refer to the current object's field.

```java
class Student {

    String name;

    Student(String name) {
        this.name = name;
    }

}
```

Without `this`, the assignment would affect the parameter, not the field.

## 4.9 Constructor Overloading

A class can have multiple constructors with different parameter lists.

```java
class Car {

    String brand;
    int speed;

    Car() {
        brand = "Unknown";
        speed = 0;
    }

    Car(String brand) {
        this.brand = brand;
        speed = 50;
    }

    Car(String brand, int speed) {
        this.brand = brand;
        this.speed = speed;
    }

}
```

## 4.10 Constructor and Inheritance

Constructors are not inherited, but parent constructors run before child constructors.

```java
class A {

    A() {
        System.out.println("A constructor");
    }

}

class B extends A {

    B() {
        System.out.println("B constructor");
    }

}
```

```java
B obj = new B();
```

Output:

```text
A constructor
B constructor
```

## 4.11 `super()` in Constructors

`super()` calls the parent constructor.

```java
class A {

    A(int x) {
        System.out.println("Parent constructor with x");
    }

}

class B extends A {

    B() {
        super(5);
        System.out.println("Child constructor");
    }

}
```

## 4.12 Common Exam Traps

- writing a return type in a constructor
- constructor name not matching class name
- forgetting that parent constructor runs first
- assuming default constructor exists after writing a parameterized constructor
- misunderstanding `this.name = name`

---

# 5. Access Modifiers and Encapsulation

## 5.1 Definition

Access modifiers control the visibility of fields, methods, and classes.

Encapsulation is the process of protecting object data by restricting direct access and using methods to control it.

## 5.2 Main Access Modifiers

| Modifier | Access Level |
|----------|--------------|
| public | Accessible everywhere |
| protected | Accessible in the same package and subclasses |
| private | Accessible only inside the same class |
| default | Accessible only in the same package |

## 5.3 public

`public` members can be accessed from any class.

```java
class A {

    public int x = 10;

}
```

```java
A obj = new A();
System.out.println(obj.x);
```

## 5.4 private

`private` members can only be used inside the class where they are declared.

```java
class A {

    private int x = 10;

}
```

This causes a compile error outside the class:

```java
A obj = new A();
System.out.println(obj.x);
```

## 5.5 protected

`protected` members are accessible:

- in the same package
- in subclasses

## 5.6 Encapsulation

Encapsulation hides internal data using private fields and public getter and setter methods.

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
```

## 5.7 Why Encapsulation Is Important

Encapsulation:

- protects data from direct modification
- allows validation before storing values
- improves program maintainability

Example with validation:

```java
class Student {

    private int age;

    public void setAge(int a) {
        if (a > 0) {
            age = a;
        }
    }

    public int getAge() {
        return age;
    }

}
```

## 5.8 Important Rules

- private fields cannot be accessed directly outside the class
- getters read values
- setters modify values
- encapsulation is a common exam topic in compile error questions

## 5.9 Common Exam Traps

- accessing private fields directly
- forgetting to use getters and setters
- assuming `protected` means only child class access, when same package access also exists
- confusing `public` access with good design, when encapsulation is often preferred

---

# 6. Inheritance

## 6.1 Definition

Inheritance allows one class to acquire the fields and methods of another class.

The class being inherited from is the parent or superclass.

The inheriting class is the child or subclass.

## 6.2 Purpose

Inheritance supports code reuse and creates class hierarchies.

## 6.3 Basic Syntax

```java
class Parent {
}

class Child extends Parent {
}
```

## 6.4 Example

```java
class Animal {

    void eat() {
        System.out.println("Animal eating");
    }

}

class Dog extends Animal {

    void bark() {
        System.out.println("Dog barking");
    }

}
```

```java
Dog d = new Dog();
d.eat();
d.bark();
```

## 6.5 Explanation

`Dog` inherits `eat()` from `Animal`.

`Dog` also defines its own method `bark()`.

## 6.6 The `extends` Keyword

`extends` tells Java that one class is inheriting from another.

## 6.7 The `super` Keyword

`super` refers to the parent class.

It is used to:

- access parent fields
- call parent methods
- call parent constructors

Example using parent method:

```java
class A {

    void show() {
        System.out.println("A");
    }

}

class B extends A {

    void show() {
        super.show();
        System.out.println("B");
    }

}
```

Output:

```text
A
B
```

## 6.8 Field Hiding

A child class can declare a field with the same name as the parent field.

```java
class A {

    int x = 5;

}

class B extends A {

    int x = 10;

}
```

Inside `B`:

- `x` refers to `B.x`
- `super.x` refers to `A.x`

## 6.9 Constructor Chaining

When a child object is created, parent constructors execute first.

```java
class A {

    A() {
        System.out.println("A");
    }

}

class B extends A {

    B() {
        System.out.println("B");
    }

}

class C extends B {

    C() {
        System.out.println("C");
    }

}
```

```java
C obj = new C();
```

Output:

```text
A
B
C
```

## 6.10 Important Rules

- child classes inherit accessible fields and methods
- constructors are not inherited
- parent constructors run before child constructors
- `super()` must be the first statement in a constructor if used

## 6.11 Common Exam Traps

- thinking constructors are inherited
- forgetting parent constructor execution order
- confusing field hiding with method overriding
- assuming private members are inherited in a directly usable way, when they are not accessible in child class code

---

# 7. Polymorphism

## 7.1 Definition

Polymorphism allows one method name to behave differently depending on the context.

Java mainly uses two forms:

- compile time polymorphism
- runtime polymorphism

## 7.2 Compile Time Polymorphism

Compile time polymorphism is method overloading.

It is resolved by the compiler based on method signatures.

### Example

```java
class MathUtil {

    int add(int a, int b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }

    double add(double a, double b) {
        return a + b;
    }

}
```

### Rules of Overloading

- method name must be the same
- parameter list must differ
- return type alone is not enough

## 7.3 Runtime Polymorphism

Runtime polymorphism is method overriding.

It is resolved during execution based on the actual object type.

### Example

```java
class A {

    void show() {
        System.out.println("A");
    }

}

class B extends A {

    void show() {
        System.out.println("B");
    }

}
```

```java
A obj = new B();
obj.show();
```

Output:

```text
B
```

## 7.4 Reference Type vs Object Type

This is the most important polymorphism rule.

Example:

```java
A obj = new B();
```

- Reference type is `A`
- Object type is `B`

### Rule 1

Reference type decides which methods are allowed to be called.

### Rule 2

Object type decides which overridden method runs.

## 7.5 Method Search Rule

For overridden methods:

1. Java checks the actual object type
2. It searches upward in the inheritance chain
3. The first matching implementation is executed

## 7.6 Example

```java
class A {

    void show() {
        System.out.println("A");
    }

}

class B extends A {

    void show() {
        System.out.println("B");
    }

}

class C extends B {
}
```

```java
A obj = new C();
obj.show();
```

Output:

```text
B
```

Why:

- `C` does not define `show`
- Java moves upward to `B`
- `B` has `show`
- `B.show()` runs

## 7.7 Fields and Polymorphism

Fields do not follow runtime polymorphism.

Fields use the reference type.

Example:

```java
class A {

    int x = 5;

}

class B extends A {

    int x = 10;

}
```

```java
A obj = new B();
System.out.println(obj.x);
```

Output:

```text
5
```

Because field access uses the reference type `A`.

## 7.8 Casting and Field Access

```java
A obj = new B();
System.out.println(((B)obj).x);
```

Output:

```text
10
```

Because casting changes the reference type used for field access.

## 7.9 Important Rules

- overloading is compile time polymorphism
- overriding is runtime polymorphism
- overridden methods use object type
- fields use reference type
- method availability is checked by reference type

## 7.10 Common Exam Traps

- thinking fields behave like overridden methods
- confusing overloading with overriding
- assuming child only methods can be called through a parent reference
- forgetting that Java chooses the closest implementation from the object class upward

---

# 8. Abstract Classes

## 8.1 Definition

An abstract class is a class that cannot be instantiated directly.

It is used as a base class for subclasses.

It may contain:

- abstract methods
- normal methods
- fields
- constructors

## 8.2 Abstract Methods

An abstract method has no body.

```java
abstract class Animal {

    abstract void sound();

}
```

## 8.3 Rules of Abstract Methods

- an abstract method has no body
- if a class contains an abstract method, the class must be abstract
- the first concrete subclass must implement the abstract method

## 8.4 Example of Implementation

```java
abstract class Animal {

    abstract void sound();

}
```

```java
class Dog extends Animal {

    void sound() {
        System.out.println("Bark");
    }

}
```

## 8.5 Abstract Class with Normal Method

```java
abstract class Animal {

    abstract void sound();

    void eat() {
        System.out.println("Animal eating");
    }

}
```

Subclasses must implement `sound()`, but they may directly use `eat()`.

## 8.6 Abstract Class with Constructor

Abstract classes can have constructors.

```java
abstract class A {

    A() {
        System.out.println("A constructor");
    }

    abstract void show();

}

class B extends A {

    B() {
        System.out.println("B constructor");
    }

    void show() {
        System.out.println("B show");
    }

}
```

```java
A obj = new B();
obj.show();
```

Output:

```text
A constructor
B constructor
B show
```

## 8.7 Important Rules

- abstract classes cannot be instantiated
- abstract methods must be implemented by concrete subclasses
- abstract classes may contain normal methods
- abstract classes may contain constructors and fields

## 8.8 Difference Between Normal Method and Abstract Method in Abstract Class

### Normal method

```java
abstract class A {

    void show() {
        System.out.println("A");
    }

}
```

This method already has code. Subclasses may use it directly.

### Abstract method

```java
abstract class A {

    abstract void show();

}
```

This method has no code. Subclasses must implement it.

## 8.9 Common Exam Traps

- trying to instantiate an abstract class
- forgetting to implement inherited abstract methods
- thinking abstract classes cannot have constructors or normal methods
- confusing abstract methods with normal methods without bodies, which is illegal unless the method is abstract

---

# 9. Interfaces

## 9.1 Definition

An interface defines a contract that implementing classes must follow.

It describes what methods must exist.

An interface focuses on behavior, not shared object state.

## 9.2 Purpose

Interfaces are used to:

- define common behavior for unrelated classes
- support abstraction
- support polymorphism
- allow multiple interface implementation

## 9.3 Basic Declaration

```java
interface Flyable {

    void fly();

}
```

## 9.4 Meaning of Contract

The interface says:

Any class implementing `Flyable` must provide a method named `fly`.

## 9.5 Implementing an Interface

```java
class Bird implements Flyable {

    public void fly() {
        System.out.println("Flying");
    }

}
```

## 9.6 Important Rule About Access

Interface methods are public by default.

So when implementing them, the method must be `public`.

Invalid:

```java
class Bird implements Flyable {

    void fly() {
        System.out.println("Flying");
    }

}
```

This causes a compile error because access became weaker.

## 9.7 Interface Polymorphism

```java
interface A {

    void show();

}

class B implements A {

    public void show() {
        System.out.println("B");
    }

}
```

```java
A obj = new B();
obj.show();
```

Output:

```text
B
```

## 9.8 Multiple Interfaces

A class can implement more than one interface.

```java
interface A {
    void show();
}

interface B {
    void print();
}

class C implements A, B {

    public void show() {
        System.out.println("Show");
    }

    public void print() {
        System.out.println("Print");
    }

}
```

## 9.9 Default Methods

Interfaces can contain default methods with implementation.

```java
interface A {

    default void show() {
        System.out.println("Default show");
    }

}
```

A class implementing `A` can use the default method without overriding it.

## 9.10 Interface Method Conflict Resolution

If two interfaces contain the same default method, the implementing class must override it.

```java
interface A {

    default void show() {
        System.out.println("A");
    }

}

interface B {

    default void show() {
        System.out.println("B");
    }

}

class C implements A, B {

    public void show() {
        System.out.println("C");
    }

}
```

Without overriding `show()`, a compile error occurs.

## 9.11 Interface Variables

Interface variables are automatically:

- public
- static
- final

Example:

```java
interface A {

    int x = 10;

}
```

This is actually:

```java
public static final int x = 10;
```

So this is illegal:

```java
A.x = 20;
```

Because `x` is final.

## 9.12 Important Rules

- interfaces cannot be instantiated
- interface methods are public by default
- interface variables are public static final
- a class can implement multiple interfaces
- if a class does not implement all interface methods, it must be abstract

## 9.13 Common Exam Traps

- forgetting `public` in implemented methods
- trying to instantiate an interface
- forgetting to implement all methods
- trying to modify interface variables
- confusing `implements` with `extends`

---

# 10. Exception Handling

## 10.1 Definition

Exception handling is the mechanism used to handle runtime errors and prevent unexpected program termination.

## 10.2 Purpose

Exception handling allows programs to:

- detect runtime problems
- handle errors safely
- continue execution after handling a problem

## 10.3 try catch Structure

```java
try {

    int x = 10 / 0;

}
catch (ArithmeticException e) {

    System.out.println("Cannot divide by zero");

}
```

## 10.4 Flow of Execution

When an exception occurs inside the `try` block:

1. the remaining lines inside `try` are skipped
2. Java jumps to the matching `catch` block
3. after `catch`, normal execution continues

## 10.5 Example

```java
try {

    System.out.println("Start");
    int x = 10 / 0;
    System.out.println("End");

}
catch (ArithmeticException e) {

    System.out.println("Math Error");

}

System.out.println("Done");
```

Output:

```text
Start
Math Error
Done
```

## 10.6 Common Exception Types

| Exception Type | Meaning |
|----------------|---------|
| ArithmeticException | Division by zero |
| ArrayIndexOutOfBoundsException | Invalid array index |
| NullPointerException | Using a null reference |
| NumberFormatException | Invalid numeric conversion |

## 10.7 Catch Order

Specific exceptions must come before general exceptions.

Correct:

```java
try {
    int x = 10 / 0;
}
catch (ArithmeticException e) {
    System.out.println("Math error");
}
catch (Exception e) {
    System.out.println("General error");
}
```

Wrong:

```java
try {
    int x = 10 / 0;
}
catch (Exception e) {
    System.out.println("General error");
}
catch (ArithmeticException e) {
    System.out.println("Math error");
}
```

This causes a compile error because the general catch comes first.

## 10.8 Important Rules

- exceptions happen during runtime
- remaining `try` code is skipped after an exception
- matching `catch` block handles the exception
- catch order matters

## 10.9 Common Exam Traps

- thinking runtime exceptions are compile errors
- forgetting output before the exception line still prints
- writing catch blocks in the wrong order

---

# 11. Arrays

## 11.1 Definition

An array stores multiple values of the same type in one structure.

## 11.2 Purpose

Arrays are used to store related values together.

## 11.3 Declaration Methods

### Method 1

```java
int[] arr = {10, 20, 30};
```

### Method 2

```java
int[] arr = new int[3];
```

## 11.4 Indexing

Array indexes start from `0`.

For an array of length `n`, valid indexes are:

`0` to `n - 1`

## 11.5 Example

```java
int[] arr = {10, 20, 30, 40};

System.out.println(arr[2]);
```

Output:

```text
30
```

## 11.6 Default Values

Arrays created with `new` receive default values.

| Type | Default Value |
|------|---------------|
| int | 0 |
| double | 0.0 |
| boolean | false |
| String | null |

Example:

```java
int[] arr = new int[3];
System.out.println(arr[1]);
```

Output:

```text
0
```

## 11.7 Invalid Index

```java
int[] arr = {1, 2, 3};
System.out.println(arr[5]);
```

This causes `ArrayIndexOutOfBoundsException`.

## 11.8 Important Rules

- index starts at 0
- array size is fixed after creation
- invalid index access causes runtime exception

## 11.9 Common Exam Traps

- starting from index 1 instead of 0
- treating invalid index as compile error
- forgetting default values in arrays created with `new`

---

# 12. Parameter Passing

## 12.1 Definition

Java uses pass by value.

This means a copy of the value is passed to the method.

## 12.2 Primitive Types

For primitive variables, Java passes a copy of the actual value.

```java
class Test {

    static void change(int x) {
        x = 50;
    }

    public static void main(String[] args) {

        int a = 10;
        change(a);

        System.out.println(a);

    }

}
```

Output:

```text
10
```

Why:

- `a` remains unchanged
- method changes only the local copy `x`

## 12.3 Object References

For objects, Java passes a copy of the reference.

Both references point to the same object.

```java
class Box {
    int value;
}

class Test {

    static void change(Box b) {
        b.value = 50;
    }

    public static void main(String[] args) {

        Box obj = new Box();
        obj.value = 10;

        change(obj);

        System.out.println(obj.value);

    }

}
```

Output:

```text
50
```

Why:

- `obj` and `b` point to the same object
- changing `b.value` changes the object itself

## 12.4 Reassigning the Parameter

```java
class Box {
    int value;
}

class Test {

    static void reset(Box b) {
        b = new Box();
        b.value = 100;
    }

    public static void main(String[] args) {

        Box obj = new Box();
        obj.value = 10;

        reset(obj);

        System.out.println(obj.value);

    }

}
```

Output:

```text
10
```

Why:

- `b = new Box()` changes only the local reference
- `obj` still points to the original object

## 12.5 Important Rules

- Java is always pass by value
- primitive types pass a copy of the actual value
- object variables pass a copy of the reference
- changing object fields affects the original object
- reassigning the parameter does not affect the original reference

## 12.6 Common Exam Traps

- thinking Java is pass by reference
- confusing field changes with reference reassignment
- thinking `b = new Box()` changes the original object reference

---

# 13. Compilation Errors and Code Analysis

## 13.1 Definition

Compilation errors are problems detected by the compiler before the program runs.

Code analysis questions test whether code will compile, what error occurs, or what output is produced.

## 13.2 Method Signature Mismatch

Method calls must match method declarations exactly.

Example:

```java
class A {

    void show(int x) {
        System.out.println(x);
    }

}
```

```java
A obj = new A();
obj.show();
```

This causes a compile error because `show(int x)` requires one `int` argument.

## 13.3 Missing Constructors

```java
class Car {

    Car(int speed) {
    }

}
```

```java
Car c = new Car();
```

Compile error because no no argument constructor exists.

## 13.4 Access Modifier Conflicts

```java
class A {

    private int x = 10;

}
```

```java
A obj = new A();
System.out.println(obj.x);
```

Compile error because `x` is private.

## 13.5 Missing Method Implementation in Abstract Classes

```java
abstract class A {

    abstract void show();

}

class B extends A {
}
```

Compile error because `B` must implement `show()` or be declared abstract.

## 13.6 Missing Method Implementation in Interfaces

```java
interface A {

    void show();

}

class B implements A {
}
```

Compile error because `B` must implement `show()` or be abstract.

## 13.7 Wrong Access While Implementing Interface

```java
interface A {

    void show();

}

class B implements A {

    void show() {
        System.out.println("B");
    }

}
```

Compile error because interface methods must be implemented as `public`.

## 13.8 Compile Time, Runtime, and Logical Errors

### Compile Time Error

Detected before execution.

Example:

```java
System.out.println("Hello")
```

Missing semicolon.

### Runtime Error

Occurs during execution.

Example:

```java
int x = 10 / 0;
```

ArithmeticException.

### Logical Error

Program runs but gives wrong output.

Example:

```java
if (score > 50) {
    System.out.println("Pass");
}
```

If passing score should include 50, then the condition is logically wrong.

## 13.9 Important Rules

- compile errors stop the program before execution
- runtime errors happen while the program runs
- logical errors do not crash the program but produce incorrect results
- code analysis questions often combine constructors, access modifiers, polymorphism, and abstract or interface rules

## 13.10 Common Exam Traps

- confusing compile errors with runtime exceptions
- missing constructor problems
- wrong method signatures
- incorrect access modifiers
- incomplete interface or abstract method implementation

---

# 14. Final Summary

These notes covered the full set of core Java OOP topics needed for exam revision.

The material included:

- Java program structure
- classes and objects
- methods
- constructors
- access modifiers and encapsulation
- inheritance
- polymorphism
- abstract classes
- interfaces
- exception handling
- arrays
- parameter passing
- compilation errors and code analysis

The most heavily tested areas in Java OOP exams are usually:

- constructor behavior
- inheritance and `super`
- method overloading and overriding
- runtime polymorphism
- abstract classes and interfaces
- access modifiers and encapsulation
- parameter passing
- compile error detection

A strong revision strategy is to focus on the rules of each concept, then practice mixed questions where multiple concepts appear in one code snippet.
