# Method in Java

-  **method** is a collection of instructions that performs a specific task. 
-   provides reusability easily modify code using **methods**. 
-   method is executed only when we call or invoke it.
-   most important method in java is the main method. 

---

### Method Declaration
- provides information about method attributes, such as visibility, return-type, name, and arguments. 
- has six components that are known as **method header**

![Method in Java](https://static.javatpoint.com/core/images/method-in-java.png)


- **Method Signature:** 
		- Every method has a method signature as a part of the method declaration, includes the **method name** and **parameter list**.
	- **Access Specifier:**
		- also called modifier, is the access type of the method
		- specifies the visibility of the method. 
		- Java provides **four** types of access specifier:

            -   **Public:** The method is accessible by all classes when we use public specifier in our application.
            -   **Private:** When we use a private access specifier, the method is accessible only in the classes in which it is defined.
            -   **Protected:** When we use protected access specifier, the method is accessible within the same package or subclasses in a different package.
            -   **Default:** When we do not use any access specifier in the method declaration, Java uses default access specifier by default. It is visible only from the same package only.

            - **Return Type:** Return type is a data type that the method returns. It may have a primitive data type, object, collection, void, etc. If the method does not return anything, we use void keyword.

            - **Method Name:** It is a unique name that is used to define the name of a method. It must be corresponding to the functionality of the method. Suppose, if we are creating a method for subtraction of two numbers, the method name must be **subtraction().** A method is invoked by its name.

            - **Parameter List:** It is the list of parameters separated by a comma and enclosed in the pair of parentheses. It contains the data type and variable name. If the method has no parameter, left the parentheses blank.

            - **Method Body:** It is a part of the method declaration. It contains all the actions to be performed. It is enclosed within the pair of curly braces.

--- 

### Naming a Method
-  the method name must be a **verb** and start with a **lowercase** letter. 
-  If the method name has more than two words, the first name must be a verb followed by adjective or noun. 
-  In the multi-word method name, the first letter of each word must be in **uppercase** except the first word. 
-  For example:
    - **Single-word method name:** sum(), area()

    - **Multi-word method name:** areaOfCircle(), stringComparision()

-  a method having the same name as another method name in the same class, it is known as **method overloading**.

---
### Types of Method

There are two types of methods in Java:

-   Predefined Method
-   User-defined Method

- Predefined Method
	- method that is already defined in the Java class libraries is known as predefined methods. 
	-  also known as the **standard library method** or **built-in method**.
	-  can directly use these methods just by calling them in the program at any point. 
	-  Examples: **length(), equals(), compareTo(), sqrt()** 
```java
public class Demo   
{  
public static void main(String[] args)   
{  
// using the max() method of Math class  
System.out.print("The maximum number is: " + Math.max(9,7));  
}  
}  
/*
Output:
The maximum number is: 9
*/
````
---

### User-defined Method

- method written by the user or programmer 
- can be modified according to the requirement.
- Example
```java 
import java.util.Scanner;  
public class EvenOdd  
{  
public static void main (String args[])  
{  
//creating Scanner class object     
Scanner scan=new Scanner(System.in);  
System.out.print("Enter the number: ");  
//reading value from user  
int num=scan.nextInt();  
//method calling  
findEvenOdd(num);  
}  
//user defined method  
public static void findEvenOdd(int num)  
{  
//method body  
if(num%2==0)   
System.out.println(num+" is even");   
else   
System.out.println(num+" is odd");  
}  
}  

```
---

### Static Method
- A method that has static keyword ( also a method that belongs to a class rather than an instance of a class) 
- create a static method by using the keyword **static** before the method name.
- advantage of a static method is it can be called without creating an object. 
- can access static data members and also change the value of it. 
- used to create an instance method. 
- is invoked by using the class name. 
-  example of a static method is the **main()** method.
- **Example**
```java
public class Display  
{  
public static void main(String[] args)   
{  
show();  
}  
static void show()   
{  
System.out.println("It is an example of static method.");  
}  
}  
/*
Output:
It is an example of a static method.
*/
````
---

### Instance Method

- The method of the class is known as an **instance method**. 
- It is a **non-static** method defined in the class. 
- Before calling or invoking the instance method, it is necessary to create an object of its class.
- Example
```java
public class InstanceMethodExample  
{  
public static void main(String [] args)  
{  
//Creating an object of the class  
InstanceMethodExample obj = new InstanceMethodExample();  
//invoking instance method   
System.out.println("The sum is: "+obj.add(12, 13));  
}  
int s;  
//user-defined method because we have not used static keyword  
public int add(int a, int b)  
{  
s = a+b;  
//returning the sum  
return s;  
}  
}  
/*
Output:
The sum is: 25
*/
````
- There are two types of instance method:

    -   **Accessor Method**
    -   **Mutator Method**

- **Accessor Method:** 
		- The method(s) that reads the instance variable(s) is known as the accessor method. 
		- can easily identify it because the method is prefixed with the word **get**. It is also known as **getters**. 
		- returns the value of the private field. It is used to get the value of the private field.
**Example**
```java
1.  public int getId()    
2.  {    
3.  return Id;    
4.  }    
```
- **Mutator Method:** The method(s) read the instance variable(s) and also modify the values. We can easily identify it because the method is prefixed with the word **set**. It is also known as **setters** or **modifiers**. It does not return anything. It accepts a parameter of the same data type that depends on the field. It is used to set the value of the private field.

**Example**

[](https://www.javatpoint.com/method-in-java#)[](https://www.javatpoint.com/method-in-java#)[](https://www.javatpoint.com/method-in-java#)

1.  public void setRoll(int roll)   
2.  {  
3.  this.roll = roll;  
4.  }  

### Example of accessor and mutator method

**Student.java**

[](https://www.javatpoint.com/method-in-java#)[](https://www.javatpoint.com/method-in-java#)[](https://www.javatpoint.com/method-in-java#)

1.  public class Student   
2.  {  
3.  private int roll;  
4.  private String name;  
5.  public int getRoll()    //accessor method  
6.  {  
7.  return roll;  
8.  }  
9.  public void setRoll(int roll) //mutator method  
10. {  
11. this.roll = roll;  
12. }  
13. public String getName()   
14. {  
15. return name;  
16. }  
17. public void setName(String name)   
18. {  
19. this.name = name;  
20. }  
21. public void display()  
22. {  
23. System.out.println("Roll no.: "+roll);  
24. System.out.println("Student name: "+name);  
25. }  
26. }  

### Abstract Method

The method that does not has method body is known as abstract method. In other words, without an implementation is known as abstract method. It always declares in the **abstract class**. It means the class itself must be abstract if it has abstract method. To create an abstract method, we use the keyword **abstract**.

**Syntax**

[](https://www.javatpoint.com/method-in-java#)[](https://www.javatpoint.com/method-in-java#)[](https://www.javatpoint.com/method-in-java#)

1.  abstract void method_name();  

### Example of abstract method

**Demo.java**

[](https://www.javatpoint.com/method-in-java#)[](https://www.javatpoint.com/method-in-java#)[](https://www.javatpoint.com/method-in-java#)

1.  abstract class Demo //abstract class  
2.  {  
3.  //abstract method declaration  
4.  abstract void display();  
5.  }  
6.  public class MyClass extends Demo  
7.  {  
8.  //method impelmentation  
9.  void display()  
10. {  
11. System.out.println("Abstract method?");  
12. }  
13. public static void main(String args[])  
14. {  
15. //creating object of abstract class  
16. Demo obj = new MyClass();  
17. //invoking abstract method  
18. obj.display();  
19. }  
20. }  

**Output:**

Abstract method...

### Factory method

It is a method that returns an object to the class to which it belongs. All static methods are factory methods. For example, **NumberFormat obj = NumberFormat.getNumberInstance();**

* * * * *
