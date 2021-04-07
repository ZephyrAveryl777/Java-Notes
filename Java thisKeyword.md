# This keyword in java

- this is a **reference variable** that refers to the current object.

![java this keyword](https://static.javatpoint.com/images/thisr.jpg)

---

### Usage of java this keyword

The 6 usage of java this keyword.

1.  this can be used to refer current class instance variable.
2.  this can be used to invoke current class method (implicitly)
3.  this() can be used to invoke current class constructor.
4.  this can be passed as an argument in the method call.
5.  this can be passed as argument in the constructor call.
6.  this can be used to return the current class instance from the method.

---

###  `this: to refer current class instance variable` 
- can be used to refer current class instance variable. 
- If there is ambiguity between the instance variables and parameters, this keyword resolves it.
```java
class Student{  
int rollno;  
String name;  
float fee;  
Student(int rollno,String name,float fee){  
this.rollno=rollno;  
this.name=name;  
this.fee=fee;  
}  
void display(){System.out.println(rollno+" "+name+" "+fee);}  
}  
class TestThis2{  
public static void main(String args[]){  
Student s1=new Student(111,"ankit",5000f);  
Student s2=new Student(112,"sumit",6000f);  
s1.display();  
s2.display();  
}}  
/*
Output:
111 ankit 5000
112 sumit 6000
```
---

### `this: to invoke current class method`

- invoke the method of the current class by using the this keyword. 
- If this keyword not used, compiler automatically adds this keyword while invoking the method. 
- Example 
![this keyword](https://static.javatpoint.com/images/thismethod.JPG)
```java
class A{  
void m(){System.out.println("hello m");}  
void n(){  
System.out.println("hello n");  
//m();//same as this.m()  
this.m();  
}  
}  
class TestThis4{  
public static void main(String args[]){  
A a=new A();  
a.n();  
}}  
/*
Output:
hello n
hello m
*/
````
----

### `this() : to invoke current class constructor`

- The this() constructor call can be used to invoke the current class constructor. 
- used to reuse the constructor (used for constructor chaining). 

**Calling default constructor from parameterized constructor:**
```java
class A{  
A(){System.out.println("hello a");}  
A(int x){  
this();  
System.out.println(x);  
}  
}  
class TestThis5{  
public static void main(String args[]){  
A a=new A(10);  
}}  
/*
Output:
hello a
10
*/
````
**Calling parameterized constructor from default constructor:**
```java
class A{  
A(){  
this(5);  
System.out.println("hello a");  
}  
A(int x){  
System.out.println(x);  
}  
}  
class TestThis6{  
public static void main(String args[]){  
A a=new A();  
}}  
/*
Output:
5
hello a
*/
````
**Constructor Chaining**:
```java
class Student{  
int rollno;  
String name,course;  
float fee;  
Student(int rollno,String name,String course){  
this.rollno=rollno;  
this.name=name;  
this.course=course;  
}  
Student(int rollno,String name,String course,float fee){  
this(rollno,name,course);//reusing constructor  
this.fee=fee;  
}  
void display(){System.out.println(rollno+" "+name+" "+course+" "+fee);}  
}  
class TestThis7{  
public static void main(String args[]){  
Student s1=new Student(111,"ankit","java");  
Student s2=new Student(112,"sumit","java",6000f);  
s1.display();  
s2.display();  
 }}  
/*
Output:
111 ankit java null
112 sumit java 6000
*/
````
- **Call to this() must be the first statement in constructor**.
```java
class Student{  
int rollno;  
String name,course;  
float fee;  
Student(int rollno,String name,String course){  
this.rollno=rollno;  
this.name=name;  
this.course=course;  
}  
Student(int rollno,String name,String course,float fee){  
this.fee=fee;  
this(rollno,name,course);//C.T.Error  
}  
void display(){System.out.println(rollno+" "+name+" "+course+" "+fee);}  
}  
class TestThis8{  
public static void main(String args[]){  
Student s1=new Student(111,"ankit","java");  
Student s2=new Student(112,"sumit","java",6000f);  
s1.display();  
s2.display();  
}} 
/*
Compile Time Error: Call to this must be first statement in constructor
*/
````
---

### `this: to pass as an argument in the method`

- It is mainly used in the event handling. 
- **Example**:
```java
class S2{  
void m(S2 obj){  
System.out.println("method is invoked");  
}  
void p(){  
m(this);  
}  
public static void main(String args[]){  
S2 s1 = new S2();  
s1.p();  
}  
}  
/*
Output:
method is invoked
*/
```
----

### `this: to pass as argument in the constructor call`

- pass the this keyword in the constructor also. 
- It is useful if we have to use one object in multiple classes. 
- **Example**:
```java
 class B{  
 A4 obj;  
 B(A4 obj){  
 this.obj=obj;  
 }  
 void display(){  
 System.out.println(obj.data);//using data member of A4 class  
 }  
 }  

 class A4{  
 int data=10;  
 A4(){  
 B b=new B(this);  
 b.display();  
 }  
 public static void main(String args[]){  
 A4 a=new A4();  
 }  
 }  
/*
Output:10
*/
````
---

### `this keyword can be used to return current class instance`

- can return this keyword as an statement from the method. 
- return type of the method must be the class type (non-primitive). 
- **Syntax**:
```java
return_type method_name(){  
return this;  
}  
````

- Example 
```java
class A{  
A getA(){  
return this;  
 }  
 void msg(){System.out.println("Hello java");}  
 }  
class Test1{  
public static void main(String args[]){  
new A().getA().msg();  
}  
}  
/*
Output:
Hello java
*/
````
---
