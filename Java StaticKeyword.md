# Java static keyword

-  used for memory management mainly.
-  can apply static keyword with variables methods, blocks and nested classes. 
-  static keyword belongs to the class than an instance of the class.

The static can be:

1.  Variable (also known as a class variable)
2.  Method (also known as a class method)
3.  Block
4.  Nested class

![Static in Java](https://static.javatpoint.com/images/java-static-keyword1.png)

---
### Java static variable

- any variable declared as static, it is known as a static variabl
-  used to refer to the common property of all objects 
-  for example, the company name of employees, college name of students, etc.
-  static variable gets memory only once in the class area at the time of class loading.

- Advantages of static variable

	- efficient memory management.

- Understanding the problem without static variable
```java
class Student{  
int rollno;  
String name;  
String college="IIT Goa";  // common property need not initate again hence static variable 
}  
````

- static property is shared to all objects.
- **Example **
```java
//Java Program to demonstrate the use of static variable  
class Student{  
int rollno;//instance variable  
String name;  
static String college ="ITS";//static variable  
//constructor  
Student(int r, String n){  
rollno = r;  
name = n;  
}  
//method to display the values  
void display (){System.out.println(rollno+" "+name+" "+college);}  
}  
//Test class to show the values of objects  
public class TestStaticVariable1{  
public static void main(String args[]){  
Student s1 = new Student(111,"Karan");  
Student s2 = new Student(222,"Aryan");  
//we can change the college of all objects by the single line of code  
//Student.college="BBDIT";  
s1.display();  
s2.display();  
}  
}  
/*
Output:
111 Karan IIT Goa
222 Aryan IIT Goa
*/
````

![Static Variable](https://static.javatpoint.com/images/staticvariable.JPG)

----

### Program of counter by static variable
- static variable will get the memory only once, 
- if any object changes the value of the static variable, it will retain its value.
```java
1.  //Java Program to illustrate the use of static variable which  
2.  //is shared with all objects.  
3.  class Counter2{  
4.  static int count=0;//will get memory only once and retain its value  
6.  Counter2(){  
7.  count++;//incrementing the value of static variable  
8.  System.out.println(count);  
9.  }  
11. public static void main(String args[]){  
12. //creating objects  
13. Counter2 c1=new Counter2();  
14. Counter2 c2=new Counter2();  
15. Counter2 c3=new Counter2();  
16. }  
17. }  
/*
Output:
1
2
3
*/
```
---

### Java static method

- If you apply static keyword with any method, it is known as static method.

      -   A static method belongs to the class rather than the object of a class.
      -   A static method can be invoked without the need for creating an instance of a class.
      -   A static method can access static data member and can change the value of it.
      -   **Example**
```java
//Java Program to demonstrate the use of a static method.  
class Student{  
int rollno;  
String name;  
static String college = "ITS";  
//static method to change the value of static variable  
static void change(){  
college = "BBDIT";  
}  
//constructor to initialize the variable  
Student(int r, String n){  
rollno = r;  
name = n;  
}  
//method to display values  
void display(){System.out.println(rollno+" "+name+" "+college);}  
}  
//Test class to create and display the values of object  
public class TestStaticMethod{  
public static void main(String args[]){  
Student.change();//calling change method  
//creating objects  
Student s1 = new Student(111,"Karan");  
Student s2 = new Student(222,"Aryan");  
Student s3 = new Student(333,"Sonoo");  
//calling display method  
s1.display();  
s2.display();  
s3.display();  
}  
}  
/*
Output:111 Karan BBDIT
       222 Aryan BBDIT
       333 Sonoo BBDIT
*/
````
* * * * *

### Another example of a static method that performs a normal calculation

[](https://www.javatpoint.com/static-keyword-in-java#)[](https://www.javatpoint.com/static-keyword-in-java#)[](https://www.javatpoint.com/static-keyword-in-java#)

1.  //Java Program to get the cube of a given number using the static method  

3.  class Calculate{  
4.  static int cube(int x){  
 5.  return x*x*x;  
6.  }  

8.  public static void main(String args[]){  
9.  int result=Calculate.cube(5);  
10. System.out.println(result);  
11. }  
12. }  

[Test it Now](https://www.javatpoint.com/opr/test.jsp?filename=Calculate)

Output:125

### Restrictions for the static method

There are two main restrictions for the static method. They are:

1.  The static method can not use non static data member or call non-static method directly.
2.  this and super cannot be used in static context.

[](https://www.javatpoint.com/static-keyword-in-java#)[](https://www.javatpoint.com/static-keyword-in-java#)[](https://www.javatpoint.com/static-keyword-in-java#)

1.  class A{  
2.  int a=40;//non static  

4.  public static void main(String args[]){  
5.  System.out.println(a);  
6.  }  
7.  }        

[Test it Now](https://www.javatpoint.com/opr/test.jsp?filename=A)

Output:Compile Time Error

* * * * *

### Q) Why is the Java main method static?

Ans) It is because the object is not required to call a static method. If it were a non-static method, [JVM](https://www.javatpoint.com/jvm-java-virtual-machine) creates an object first then call main() method that will lead the problem of extra memory allocation.

* * * * *

3) Java static block
--------------------

-   Is used to initialize the static data member.
-   It is executed before the main method at the time of classloading.

### Example of static block

[](https://www.javatpoint.com/static-keyword-in-java#)[](https://www.javatpoint.com/static-keyword-in-java#)[](https://www.javatpoint.com/static-keyword-in-java#)

1.  class A2{  
2.  static{System.out.println("static block is invoked");}  
3.  public static void main(String args[]){  
4.  System.out.println("Hello main");  
5.  }  
6.  }  

[Test it Now](https://www.javatpoint.com/opr/test.jsp?filename=A2)

Output:static block is invoked
       Hello main

* * * * *

### Q) Can we execute a program without main() method?

Ans) No, one of the ways was the static block, but it was possible till JDK 1.6. Since JDK 1.7, it is not possible to execute a Java class without the [main method](https://www.javatpoint.com/java-main-method).

[](https://www.javatpoint.com/static-keyword-in-java#)[](https://www.javatpoint.com/static-keyword-in-java#)[](https://www.javatpoint.com/static-keyword-in-java#)

1.  class A3{  
2.  static{  
3.  System.out.println("static block is invoked");  
4.  System.exit(0);  
5.  }  
6.  }  

[Test it Now](https://www.javatpoint.com/opr/test.jsp?filename=A3)

Output:

static block is invoked

Since JDK 1.7 and above, output would be:

Error: Main method not found in class A3, please define the main method as:
   public static void main(String[] args)
or a JavaFX application class must extend javafx.application.Application
