# Constructors in Java
-  a constructor is a block of codes similar to the method.
-  called when an instance of class is created. 
-  At the time of calling constructor, memory for the object is allocated in the memory.
-   used to initialize the object.
-   Every time object created using the new() keyword, at least one constructor is called.

>**Note:** It is called constructor because it constructs the values at the time of object creation. It is not necessary to write a constructor for a class. It is because java compiler creates a default constructor if your class doesn't have any.

---

### Rules for creating Java constructor

1.  Constructor name must be the same as its class name
2.  A Constructor must have no explicit return type
3.  A Java constructor cannot be abstract, static, final, and synchronized

> **Note**: We can use access modifiers while declaring a constructor. It controls the object creation. In other words, we can have private, protected, public or default constructor in Java.

---

### Types of Java constructors

There are two types of constructors in Java:

1.  Default constructor (no-arg constructor)
2.  Parameterized constructor

![Java Constructors](https://javatpoint.com/images/core/java-constructor.png)

---

### Java Default Constructor: 
- constructor with no parameter
- used to provide default values to the objects like 0,null...
- **Syntax**:  `<class_name>(){}`   
- Example:
```java 
class Student3{  
int id;  
String name;  
//method to display the value of id and name  
void display(){System.out.println(id+" "+name);}  
  
public static void main(String args[]){  
//creating objects  
Student3 s1=new Student3();  
Student3 s2=new Student3();  
//displaying values of the object  
s1.display();  
s2.display();  
}  
}  

/*
Output: 
0 null
0 null
*/
````
> **Rule**: If there is no constructor in a class, compiler automatically creates a default constructor.

![Java default constructor](https://javatpoint.com/images/default-constructor1.png)

---

### Java Parameterized Constructor

- constructor which has a specific number of parameters called Parameterized Constructor.
-  used to provide different values to distinct objects, can provide the same values also.
-  Example
```java
//Java Program to demonstrate the use of the parameterized constructor.  
class Student4{  
int id;  
String name;  
//creating a parameterized constructor  
Student4(int i,String n){  
id = i;  
name = n;  
 }  
//method to display the values  
void display(){System.out.println(id+" "+name);}  
public static void main(String args[]){  
creating objects and passing values  
Student4 s1 = new Student4(111,"Karan");  
Student4 s2 = new Student4(222,"Aryan");  
// calling method to display the values of object  
s1.display();  
s2.display();  
}  
}  
/*
Output:

111 Karan
222 Aryan
*/
````
--- 

### Constructor Overloading in Java
- a technique of having more than one constructor with different parameter lists.
- arranged in a way that each constructor performs a different task. 
-  differentiated by the compiler by the number of parameters in the list and their types.
- **Example**:
```java  
//Java program to overload constructors  
class Student5{  
int id;  
String name;  
int age;  
//creating two arg constructor  
Student5(int i,String n){  
id = i;  
name = n;  
}  
//creating three arg constructor  
Student5(int i,String n,int a){  
id = i;  
name = n;  
age=a;  
}  
void display(){System.out.println(id+" "+name+" "+age);}  
public static void main(String args[]){  
Student5 s1 = new Student5(111,"Karan");  
Student5 s2 = new Student5(222,"Aryan",25);  
s1.display();  
s2.display();  
}  
}
/*
Output:
111 Karan 0
222 Aryan 25
*/
````
---
