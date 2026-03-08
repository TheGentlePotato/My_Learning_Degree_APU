# Java OOP Objective Revision Notes
## Exact Objective Questions, Options, Answers, and Detailed Explanations

---

## Table of Contents

1. [Question 1](#question-1)
2. [Question 3](#question-3)
3. [Question 4](#question-4)
4. [Question 5](#question-5)
5. [Question 6](#question-6)
6. [Question 7](#question-7)
7. [Question 8](#question-8)
8. [Question 9](#question-9)
9. [Question 10](#question-10)
10. [Question 11](#question-11)
11. [Question 12](#question-12)
12. [Question 13](#question-13)
13. [Question 14](#question-14)
14. [Question 15](#question-15)
15. [Question 16](#question-16)
16. [Question 17](#question-17)
17. [Question 19](#question-19)
18. [Question 20](#question-20)
19. [Question 21](#question-21)
20. [Question 22](#question-22)

---

## Question 1

### Question

```java
interface A {
    public void doSomething(String thing);
}

public class AImpl implements A {
    public void doSomething(String msg) { }
}

public class B {
    public A doit() {
        return new AImpl();
    }

    public String execute() {
        return "hi";
    }
}

public class C extends B {
    public AImpl doit() {
        return new AImpl();
    }

    public Object execute() {
        return "hi";
    }
}
```

Which statement is true?

A. Compilation of class C will fail because of an error in line 2.  
B. Compilation of class C will fail because of an error in line 6.  
C. Compilation of all classes will succeed.  
D. Compilation of class AImpl will fail because of an error in line 2.  

### Correct Answer

B

### Why B is correct

Class B has:

```java
public String execute()
```

Class C tries to override it with:

```java
public Object execute()
```

That is invalid overriding.

In Java, when overriding a method, the return type must be:

- the same type, or
- a more specific subtype

String is a subclass of Object.

So:

- parent returns String
- child returns Object

This makes the child return type more general, which Java does not allow.

### Why the other options are wrong

A is wrong because `public AImpl doit()` is valid. AImpl is a more specific return type than A. This is called covariant return type.

C is wrong because class C does not compile.

D is wrong because parameter names do not need to match. `thing` and `msg` are both `String`, so AImpl correctly implements the interface method.

---

## Question 3

### Question

```java
abstract class ClassA {
    __1__ void exec() { }
    protected abstract void comp();
}

class ClassB extends ClassA {
    __2__ void exec() { }
    __3__ void comp() { }
}
```

Which of the following are incorrect?

i. __1__ = private, __2__ = protected, __3__ = public  
ii. __1__ = private, __2__ = private, __3__ = protected  
iii. __1__ = protected, __2__ = void, __3__ = public  
iv. __1__ = protected, __2__ = public, __3__ = protected  
v. __1__ = public, __2__ = public, __3__ = public  
vi. __1__ = void, __2__ = void, __3__ = void  
vii. __1__ = protected, __2__ = protected, __3__ = protected  

A. All except (iii) and (vi)  
B. All except (ii) and (vi)  
C. All except (i) and (vii)  
D. All except (v) and (vi)  

### Correct Answer

A

### Why A is correct

Rules used:

- A child method overriding a parent method cannot reduce visibility.
- A method implementing `protected abstract void comp()` must be `protected` or `public`.

Check the invalid ones.

iii is invalid.

Parent `exec()` is `protected`, child `exec()` becomes default access.  
That reduces visibility. Not allowed.

vi is invalid.

Parent `comp()` is:

```java
protected abstract void comp();
```

Child `comp()` becomes default access.  
That reduces visibility. Not allowed.

### Why the others are valid

i and ii are valid because a private parent method is not inherited, so the child `exec()` is not overriding it.

iv is valid because child visibility is the same or wider.

v is valid because both methods use public.

vii is valid because both methods use protected.

---

## Question 4

### Question

```java
interface Car {
    int basePrice = 1000;
}

public class InterfaceTest2 implements Car {
    public static void main(String[] args) {
        basePrice = 2000;
        System.out.print(basePrice);
    }
}
```

What is the result?

A. 1000  
B. 2000  
C. Compilation error  
D. Runtime error  

### Correct Answer

C

### Why C is correct

Every variable declared in an interface is automatically:

- public
- static
- final

So this line:

```java
int basePrice = 1000;
```

is treated as:

```java
public static final int basePrice = 1000;
```

Because it is `final`, it cannot be changed.

This line causes the error:

```java
basePrice = 2000;
```

### Why the other options are wrong

A and B are wrong because the code never compiles.

D is wrong because the error happens at compile time, not runtime.

---

## Question 5

### Question

```java
public class Jump {
    private int rope = 1;
    protected boolean outside;

    public Jump() {
        // p1
        outside = true;
    }

    public Jump(int rope) {
        this.rope = outside ? rope : rope + 1;
    }

    public static void main(String[] args) {
        System.out.print(new Jump().rope);
    }
}
```

Which code, inserted at p1, produces the output 5?

A. `this(4);`  
B. `super(4);`  
C. `rope = 4;`  
D. `this.rope = 4;`  

### Correct Answer

A

### Why A is correct

`new Jump()` calls the no argument constructor.

If p1 is:

```java
this(4);
```

then execution becomes:

- `Jump()` starts
- `this(4)` calls `Jump(int rope)`
- at that time, `outside` is still `false`, because `outside = true` has not run yet

So the line

```java
this.rope = outside ? rope : rope + 1;
```

becomes

```java
this.rope = 4 + 1;
```

So rope becomes 5.

Then execution returns to `Jump()`, and `outside = true` runs.

### Why the other options are wrong

B is wrong because `super(4)` calls a parent constructor, not another constructor in the same class.

C is wrong because it sets the field to 4, so the output would be 4.

D is wrong because it sets the field directly to 4, so the output would be 4.

---

## Question 6

### Question

```java
public static void ifElseMystery(int x, int y) {
    int z = 0;

    if (x >= y) {
        z = x - y;
    }

    if (x > z && y <= z) {
        z++;
    } else if (x > z) {
        z = x + y;
    }

    System.out.println(x + " " + y + " " + z);
}
```

What is the output of:

```java
ifElseMystery(-10, 100);
```

A. -10 100 0  
B. -10 100 1  
C. 90 100 0  
D. Compilation error  

### Correct Answer

A

### Why A is correct

Start values:

- x = -10
- y = 100
- z = 0

First if:

```java
if (x >= y)
```

becomes:

```java
if (-10 >= 100)
```

False, so nothing changes.

Second if:

```java
if (x > z && y <= z)
```

becomes:

```java
if (-10 > 0 && 100 <= 0)
```

The first part is already false, so the whole condition is false.

Else if:

```java
else if (x > z)
```

becomes:

```java
else if (-10 > 0)
```

False again.

So final values stay:

- x = -10
- y = 100
- z = 0

---

## Question 7

### Question

```java
class Vehicle {
    String type = "4W";
    int maxSpeed = 100;

    Vehicle(String type, int maxSpeed) {
        this.type = type;
        this.maxSpeed = maxSpeed;
    }

    Vehicle() { }
}

class Car extends Vehicle {
    String trans;

    Car(String trans) {
        this.trans = trans;
    }

    Car(String type, int maxSpeed, String trans) {
        super(type, maxSpeed);
        this.trans = trans;
    }
}

public class Main {
    public static void main(String[] args) {
        Car c1 = new Car("Auto");
        System.out.println(c1.type + " " + c1.maxSpeed + " " + c1.trans);

        Car c2 = new Car("4W", 150, "Manual");
        System.out.println(c2.type + " " + c2.maxSpeed + " " + c2.trans);
    }
}
```

What is the output?

A. 0 0 Auto and 4W 150 Manual  
B. 4W 100 Auto and 4W 150 Manual  
C. 4W 100 Auto and 4W 100 Manual  
D. Compilation error  

### Correct Answer

B

### Why B is correct

For c1:

```java
Car c1 = new Car("Auto");
```

The constructor `Car(String trans)` is used.

There is no explicit `super(...)`, so Java inserts:

```java
super();
```

That calls `Vehicle()`.

`Vehicle()` does not change the already initialized fields, so:

- type = "4W"
- maxSpeed = 100

Then `this.trans = trans` makes:

- trans = "Auto"

So first output is:

```java
4W 100 Auto
```

For c2:

```java
Car c2 = new Car("4W", 150, "Manual");
```

The constructor calls:

```java
super(type, maxSpeed);
```

So the parent fields become:

- type = "4W"
- maxSpeed = 150

Then `trans = "Manual"`.

So second output is:

```java
4W 150 Manual
```

---

## Question 8

### Question

```java
public void test(String filename, String statement) {
    File f = new File(n);
    BufferedWriter bw = new BufferedWriter(new FileWriter(f));
    bw.write("Hello World!");
}
```

Which modification(s), made independently, enable the code to compile?

i. Add `throws IOException`  
ii. Add `throws FileNotFoundException`  
iii. Add `try { } catch(Exception e) { }`  
iv. Add `try { } catch(NullPointerException e) { }`  

A. i and ii only  
B. i and iii only  
C. ii and iii only  
D. iii and iv only  

### Correct Answer

B

### Why B is correct

`FileWriter` and `bw.write(...)` can throw checked exceptions.

Checked exceptions must be handled using:

- `throws`, or
- `try catch`

i is correct.

`throws IOException` covers these file writing operations.

ii is wrong.

`FileNotFoundException` is narrower than `IOException`.  
`bw.write(...)` may still throw `IOException`, so this is not enough.

iii is correct.

`Exception` catches `IOException`, so the code compiles.

iv is wrong.

`NullPointerException` is unrelated to the file I/O checked exception.

---

## Question 9

### Question

Indicate the incorrect statement about constructors in the given list.

A. It is possible to have many constructors, but not many methods in a class.  
B. Constructor is called whenever an object is created using `new` keyword, whereas methods will need to be invoked.  
C. Constructors must have the same name as the class but methods cannot have a class name.  
D. Constructor initializes instance of the class whereas methods performs operations pertaining to the class itself.  

### Correct Answer

A

### Why A is correct

A class can have:

- many constructors
- many methods

So statement A is false.

### Why the others are correct

B is correct because constructors run automatically when `new` creates an object.

C is correct because constructor name must match the class name exactly.

D is correct because constructors initialize object state, while methods perform actions.

---

## Question 10

### Question

```java
class Plant {
    private String name;

    public Plant(String name) {
        this.name = name;
    }
}

public class Tree extends Plant {
    public void growFruit() { }
    public void dropLeaves() { }
}
```

Which statement is true?

A. The code compiles as is.  
B. The code compiles if Tree is declared abstract.  
C. The code will compile if `public Plant() { }` is added to Plant.  
D. The code will compile if `name` is changed to protected.  

### Correct Answer

C

### Why C is correct

Tree extends Plant.

Since Tree has no constructor, Java automatically creates:

```java
Tree() {
    super();
}
```

But Plant does not have a no argument constructor. It only has:

```java
Plant(String name)
```

So compilation fails.

If this is added:

```java
public Plant() { }
```

then `super()` becomes valid and the code compiles.

### Why the others are wrong

A is wrong because `super()` has no matching constructor.

B is wrong because the problem is constructor matching, not abstraction.

D is wrong because access level of `name` is not the cause of the constructor error.

---

## Question 11

### Question

```java
class A {
    void apu(Object o) {
        System.out.print("A");
    }
}

class B {
    void apu(String o) {
        System.out.print("B");
    }
}

class C extends A {
    void apu(String s) {
        System.out.print("C");
    }
}

class D extends B {
    void apu(Object o) {
        System.out.print("D");
    }
}

public class Test {
    public static void main(String[] args) {
        A a = new C();
        a.apu("OODJ");

        C c = new C();
        c.apu("OODJ");

        B b = new D();
        b.apu("OODJ");

        D d = new D();
        d.apu("OODJ");
    }
}
```

What is the output?

A. ACBD  
B. ACBB  
C. ABCD  
D. ACDD  

### Correct Answer

B

### Why B is correct

```java
A a = new C();
```

Reference type is A, so method lookup at compile time uses methods in A.

A has:

```java
void apu(Object o)
```

`"OODJ"` is a `String`, but it can be passed as `Object`.

C does not override `apu(Object)`, so `A.apu(Object)` runs.

Output: A

```java
C c = new C();
```

C has:

```java
void apu(String s)
```

Exact match.

Output: C

```java
B b = new D();
```

Reference type is B.

B has:

```java
void apu(String o)
```

D does not override that method. It defines `apu(Object)` instead.

So `B.apu(String)` runs.

Output: B

```java
D d = new D();
```

D has its own `apu(Object)`, and it inherits `apu(String)` from B.

Java chooses the most specific match for `"OODJ"`, which is `apu(String)`.

So inherited `B.apu(String)` runs.

Output: B

Final output:

```java
ACBB
```

---

## Question 12

### Question

```java
class Base {
    Base() {
        System.out.println("Base");
    }
}

class Derived extends Base {
    Derived() {
        System.out.println("Derived");
    }
}

class DeriDerived extends Derived {
    DeriDerived() {
        System.out.println("DeriDerived");
    }
}

public class Test {
    public static void main(String[] args) {
        Derived b = new DeriDerived();
    }
}
```

What is the output?

A. Derived Base DeriDerived  
B. Base Derived DeriDerived  
C. DeriDerived Derived Base  
D. Compilation error  

### Correct Answer

B

### Why B is correct

Constructors run from parent to child.

Creating `new DeriDerived()` causes:

- `Base()`
- `Derived()`
- `DeriDerived()`

Reference type does not change constructor order. The actual object type controls constructor execution.

---

## Question 13

### Question

```java
class SuperCalc {
    protected static int multiply(int a, int b) {
        return a * b;
    }
}

class SubCalc extends SuperCalc {
    public static int multiply(int a, int b) {
        int c = super.multiply(a, b);
        return c;
    }
}
```

Which statement is true?

A. The code compiles and prints the product.  
B. Compilation fails because of line 2.  
C. Compilation fails because of line 6.  
D. Runtime error occurs.  

### Correct Answer

C

### Why C is correct

This line is the problem:

```java
int c = super.multiply(a, b);
```

`multiply` is a static method.

Static methods belong to the class, not an object.

`super` refers to the parent object context, so it cannot be used to call a static method.

Correct way would be:

```java
int c = SuperCalc.multiply(a, b);
```

### Why the other options are wrong

A is wrong because the code does not compile.

B is wrong because the static method declaration itself is valid.

D is wrong because the error is compile time, not runtime.

---

## Question 14

### Question

```java
int number_ls[] = {12, 34, 56, 78, 90};

try {
    System.out.println(number_ls[5]);
}
catch (ArrayIndexOutOfBoundsException e) {
    System.out.println("ArrayIndexOutOfBoundsException");
}
catch (IOException e) {
    System.out.println("IOException");
}
catch (NullPointerException e) {
    System.out.println("NullPointerException");
}
```

What is the output?

1. ArrayIndexOutOfBoundsException  
2. IOException  
3. NullPointerException  
4. Compilation error  

### Correct Answer

4

### Why 4 is correct

The array has 5 elements, so valid indexes are:

- 0
- 1
- 2
- 3
- 4

So `number_ls[5]` would normally cause `ArrayIndexOutOfBoundsException`.

But the code never reaches runtime because of this catch block:

```java
catch (IOException e)
```

`IOException` is a checked exception.

The try block only accesses an array. It does not contain file or I/O code, so `IOException` cannot happen there.

Java does not allow catching a checked exception that cannot occur in the try block.

So the code fails to compile.

---

## Question 15

### Question

```java
interface Run {
    default void walk() {
        System.out.println("Walking and running!");
    }
}

interface Jog {
    default void walk() {
        System.out.println("Walking and jogging!");
    }
}

class Sprint implements Run, Jog {
    public void walk() {
        Run.super.walk();
    }
}

public class Test {
    public static void main(String[] args) {
        new Sprint().walk();
    }
}
```

What is the output?

A. Walking and running!  
B. Walking and jogging!  
C. Compilation error  
D. Nothing is printed  

### Correct Answer

A

### Why A is correct

Both interfaces contain a default method named `walk()`.

That creates a conflict, so Sprint must override the method.

Inside the override, this line is used:

```java
Run.super.walk();
```

That explicitly chooses the default implementation from interface Run.

So output is:

```java
Walking and running!
```

---

## Question 16

### Question

```java
class Shape {
    protected void display() { }
}

class Circle extends Shape {
    __access_modifier__ void display() { }
}
```

Which access modifier can be used in Circle so the code compiles?

A. Only protected  
B. public, protected, and private  
C. Only public  
D. public and protected  

### Correct Answer

D

### Why D is correct

Parent method is:

```java
protected void display()
```

When overriding, the child method cannot reduce visibility.

So child can use:

- protected
- public

Child cannot use:

- default access
- private

because both are weaker than `protected`.

---

## Question 17

### Question

```java
class Phone {
    private int size;

    public Phone(int size) {
        this.size = size;
    }

    public static void sendHome(Phone p, int newSize) {
        p = new Phone(newSize);
        p.size = 4;
    }

    public static final void main(String... params) {
        final Phone phone = new Phone(3);
        sendHome(phone, 7);
        System.out.print(phone.size);
    }
}
```

What is the output?

A. 7  
B. The code does not compile  
C. 4  
D. 3  

### Correct Answer

D

### Why D is correct

`phone` points to an object whose `size = 3`.

When `sendHome(phone, 7)` is called, parameter `p` gets a copy of the reference.

At first:

- `phone` and `p` point to the same object

Then this line runs:

```java
p = new Phone(newSize);
```

Now `p` points to a new object, but `phone` still points to the original object.

Then:

```java
p.size = 4;
```

This changes only the new object.

The original object still has:

```java
size = 3
```

So the final print is:

```java
3
```

---

## Question 19

### Question

```java
class Paper { }
class Pen { }

class Clerk {
    public void checkFiles(Paper paper, Pen pen) { }
}

class Manager {
    public void giveClerkWork(Paper paper) {
        Pen pen = new Pen();
        Clerk ck = new Clerk();
        ck.checkFiles(pen, paper);
    }
}
```

Which line has the error?

A. Line 3  
B. Line 12  
C. Line 13  
D. No error  

### Correct Answer

C

### Why C is correct

The method definition is:

```java
checkFiles(Paper paper, Pen pen)
```

So the method call must pass arguments in this order:

- Paper
- Pen

But the call is:

```java
ck.checkFiles(pen, paper);
```

That passes:

- Pen
- Paper

Wrong order, so compilation fails on the method call line.

---

## Question 20

### Question

```java
interface A {
    void a();
}

abstract class B implements A {
    abstract void b();
}

class C extends B {
    // insert code here
}
```

Which inserted code allows the program to compile?

A.

```java
void b() { }
```

B.

```java
public void a() { }
void b() { }
```

C.

```java
public void a() { }
```

D. All the choices are correct.  

### Correct Answer

B

### Why B is correct

C extends abstract class B.

B still has two abstract methods that must be implemented:

- `a()` from interface A
- `b()` from abstract class B

So C must implement both.

`a()` must be `public` because interface methods are implicitly public.

So correct code is:

```java
public void a() { }
void b() { }
```

### Why the other options are wrong

A is missing `a()`.

C is missing `b()`.

D is wrong because only one option is complete.

---

## Question 21

### Question

```java
public class Test {
    static int x, y;

    public static void main(String[] args) {
        x--;
        myMethod();
        System.out.println(x + y + ++x);
    }

    public static void myMethod() {
        y = x++ + ++x;
        System.out.println(y);
        System.out.println(x);
    }
}
```

What is the final output of the last print statement?

A. 1  
B. 2  
C. 3  
D. 4  

### Correct Answer

C

### Why C is correct

Initial values of static ints are:

- x = 0
- y = 0

First line in `main`:

```java
x--;
```

Now:

```java
x = -1
```

Call `myMethod()`.

Inside:

```java
y = x++ + ++x;
```

Evaluate left to right.

First part, `x++`:

- value used is -1
- then x becomes 0

Second part, `++x`:

- x becomes 1
- value used is 1

So:

```java
y = -1 + 1 = 0
```

Now:

- x = 1
- y = 0

Back in `main`:

```java
System.out.println(x + y + ++x);
```

Current values:

- x = 1
- y = 0

`++x` makes `x = 2`

Expression becomes:

```java
1 + 0 + 2 = 3
```

So final answer is 3.

---

## Question 22

### Question

```java
abstract class Planet {
    protected void revolve() { }   // n1
    abstract void rotate();        // n2
}

class Earth extends Planet {
    void revolve() { }             // n3
    protected void rotate() { }    // n4
}
```

Which two modifications, made independently, enable the code to compile?

A. Make the method at line n3 public  
B. Make the method at line n4 public  
C. Make the method at line n3 protected  
D. Make the method at line n2 protected  

### Correct Answer

A and C

### Why A and C are correct

The problem is here.

Parent:

```java
protected void revolve()
```

Child:

```java
void revolve()
```

The child reduces visibility from `protected` to default access. That is not allowed in overriding.

To fix it, line n3 must become:

```java
protected void revolve()
```

or

```java
public void revolve()
```

So A and C are correct.

### Why B is not needed

`rotate()` in parent has default access:

```java
abstract void rotate();
```

Child has:

```java
protected void rotate()
```

That is wider visibility, which is allowed.

### Why D is not needed

Changing the parent abstract method access is unnecessary because line n4 is already valid.
