# Abstract class in Java

- A class with the abstract keyword is an abstract class.
- can have abstract and non-abstract methods (method with the body).

### Abstraction in Java

- **Abstraction**:
	-  a process of hiding the implementation details and showing only functionality to the user.
	- shows only essential things to the user and hides the internal details.
	- Abstraction lets you focus on what the object does instead of how it does it.

### Ways to achieve Abstraction

Two ways to achieve abstraction:

    1.  Abstract class (0 to 100%)
    2.  Interface (100%)

---

### Abstract class in Java

- A class which is declared as abstract is known as an **abstract class**.
-  It can have abstract and non-abstract methods. 
-  It needs to be extended and its method implemented. 
-  It cannot be instantiated.

#### Points to Remember

-   An abstract class must be declared with an abstract keyword.
-   It can have abstract and non-abstract methods.
-   It cannot be instantiated.
-   It can have constuctors and static methods also.
-   It can have final methods which will force the subclass not to change the body of the method.

- **Syntax of abstract class** `abstract class A{}`  

---

### Abstract Method in Java

- A method which is declared as abstract and does not have implementation is known as an abstract method.
- **Syntax**: `abstract void printStatus();//no method body and abstract`
- **Example**:
```java
abstract class Bike{  
abstract void run();  
}  
class Honda4 extends Bike{  
void run(){System.out.println("running safely");}  
public static void main(String args[]){  
Bike obj = new Honda4();  
obj.run();  
}  
}  
/*
Output:
running safely
*/

// Example 2
 abstract class Shape{  
 abstract void draw();  
 }   //In real scenario, implementation is provided by others i.e. unknown by end user  
 class Rectangle extends Shape{  
 void draw(){System.out.println("drawing rectangle");}  
 }  
 class Circle1 extends Shape{  
 void draw(){System.out.println("drawing circle");}  
 }  
 //In real scenario, method is called by programmer or user  
 class TestAbstraction1{  
 public static void main(String args[]){  
Shape s=new Circle1();//In a real scenario, object is provided through   		method, e.g., getShape() method  
 s.draw();  
 }  
 }  
/*
Output
drawing circle
*/
````

---

### Abstract class having constructor, data member and methods

- An abstract class can have a data member, abstract method, method body (non-abstract method), constructor, and even main() method.

```java
 //Example of an abstract class that has abstract and non-abstract methods  
 abstract class Bike{  
 Bike(){System.out.println("bike is created");}  
 abstract void run();  
 void changeGear(){System.out.println("gear changed");}  
 }  
 //Creating a Child class which inherits Abstract class  
 class Honda extends Bike{  
 void run(){System.out.println("running safely..");}  
 }  
 //Creating a Test class which calls abstract and non-abstract methods  
 class TestAbstraction2{  
 public static void main(String args[]){  
 Bike obj = new Honda();  
 obj.run();  
 obj.changeGear();  
 }  
 }  
/*
Output
       bike is created
       running safely..
       gear changed
*/
```

----
>  Rule: If there is an abstract method in a class, that class must be abstract.
```java
class Bike12{  
abstract void run();  
}  
/* Output:
compile time error
*/
````

> Rule: If you are extending an abstract class that has an abstract method, you must either provide the implementation of the method or make this class abstract.
- **Example**
```java
interface A{  
void a();  
void b();  
void c();  
void d();  
}  
 abstract class B implements A{  
 public void c(){System.out.println("I am c");}  
 }
 class M extends B{  
 public void a(){System.out.println("I am a");}  
 public void b(){System.out.println("I am b");}  
 public void d(){System.out.println("I am d");}  
 }  
 class Test5{  
public static void main(String args[]){  
A a=new M();  
a.a();  
a.b();  
a.c();  
a.d();  
}}  
/*
Output:I am a
       I am b
       I am c
       I am d
*/
````
