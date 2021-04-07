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

    - **Return Type:** 
    	- is a data type that the method returns. 
    	- may have a primitive data type, object, collection, void, etc. 
    	- for the method to not return anything, use void keyword.

    - **Method Name:** 
    	- is a unique name that is used to define the name of a method.
    	-  It must be corresponding to the functionality of the method. 
    	-  **Example**:  **subtraction().**
    	-   A method is invoked by its name.

    - **Parameter List:** 
    	- is the list of parameters separated by a comma and enclosed in the pair of parentheses.
    	- contains the data type and variable name. 
    	- If method has no parameter, leave the  parentheses blank.

    - **Method Body:** 
    	- a part of the method declaration. 
    	- contains all the actions to be performed.  
    	- is enclosed within the pair of curly braces.

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
````
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
public int getId()    
{    
return Id;    
}  
```

- **Mutator Method:** 
	- The method(s) read the instance variable(s) and also modify the values.
	- can easily identify it because the method is prefixed with the word **set**. It is also known as **setters** or **modifiers**. 
	- does not return anything, accepts a parameter of the same data type that depends on the field
	-  is used to set the value of the private field.
	-  **Example**
```java
public class Student   
{  
private int roll;  
private String name;  
public int getRoll()    //accessor method  
{  
return roll;  
}  
public void setRoll(int roll) //mutator method  
{  
this.roll = roll;  
}  
public String getName()   
{  
return name;  
}  
public void setName(String name)   
{  
this.name = name;  
}  
public void display()  
{  
System.out.println("Roll no.: "+roll);  
System.out.println("Student name: "+name);  
}  
}  
``` 
---

### Abstract Method

- A method that does not has method body is known as abstract method. 
- always declares in the **abstract class**,  the class itself must be abstract if it has abstract method. 
- To create an abstract method, we use the keyword **abstract**.
- **Syntax** `abstract void method_name()`;  
- **Example**
```java
abstract class Demo //abstract class  
{  
//abstract method declaration  
abstract void display();  
}  
public class MyClass extends Demo  
{  
//method impelmentation  
void display()  
{  
System.out.println("Abstract method?");  
}  
public static void main(String args[])  
{  
//creating object of abstract class  n
Demo obj = new MyClass();  
//invoking abstract method  
obj.display();  
}  
}  
/*
Output:
Abstract method...
*/
```
---
