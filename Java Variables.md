# Variables
- container which holds the value while Java program is executed. 
- assigned with a data type 
- name of memory location, three types of variables: **local**,**instance**,**static**.
- different types of variables:
  - **String** 
     - stores text, such as "Hello". String values are surrounded by double quotes
  - **int** 
    - stores integers (whole numbers), without decimals, such as 123 or -123
  - **float**
    - stores floating point numbers, with decimals, such as 19.99 or -19.99
  - **char** 
    - stores single characters, such as 'a' or 'B'. Char values are surrounded by single quotes
  - **boolean** 
    - stores values with two states: true or false
 ---
 ### Declaromg Variables
 - Syntax **`type variable = value;`**
 - _type_ is one of Java's types(such as int or String)
 - _variable_ is name of the variables(such as x or name)
 - _equal sign_ is used to assign values to the variable.
 ```java 
String name = "ABCD";
System.out.println(name) // outputs the name 
int number = 15;
System.out.println(number);
// declare variables without assigning them
int number_2;
number_2 = 13;
System.out.println(number_2);
// change of value by assigning new value 
int number_3 = 12;
number_3 = 20; // number_3 is now 20
System.out.println(number_3)
````
----
### Variable demonstration
```java 
int myNum = 5;
float myFloatNum = 5.99f;
char myLetter = 'D';
boolean myBool = true;
String myText = "Hello";
```
---
### Final variables
- add final keyword if variable value is not to be overwritten.
- its same as const keyword meaning unchangeable and read-only.
```java 
final int number = 10;
number = 20; // will generate an error : cannot assign a value to a final variable. 
````
---
### Display Variables 
- **`println()`** method is often used to display variables.
- combine both text and a variable, use the `+` character:
```java
String name = "Java";
System.out.println("Hello"+name);
```
- can use the `+` character to add a variable to another variable. 
```java
String firstName = "John ";
String lastName = "Doe";
String fullName = firstName + lastName;
System.out.println(fullName);
// can be used for numeric types too
int x = 5;
int y = 6;
System.out.println(x + y); // Print the value of x + y
```
---
### Declaring Many Variables 
- to declare more than one variable of the same type, 
```java
int x = 5, y = 6, z = 50;
System.out.println(x + y + z);
```
---
### Java Identifiers 
- all Java variables must be identified with unique names.
- unique names are called identifiers. 
- The general rules for constructing names for variables (unique identifiers) are:
  -  Names can contain letters, digits, underscores, and dollar signs
  -  Names must begin with a letter
  -  Names should start with a lowercase letter and it cannot contain whitespace
  -  Names can also begin with $ and _ (but we will not use it in this tutorial)
  -  Names are case sensitive ("myVar" and "myvar" are different variables)
  -  Reserved words (like Java keywords, such as int or boolean) cannot be used as names
---
### Types of Variables 
- **Local Variable**:
  - variable declated inside the body of the method 
  - can use this variable only within that method
  - other methods in that class aren't aware of its existance.
- **Instance Variable**:
  - variables declared inside the class but outside the body of the method
  - called instance variable because its value is instance specific and is not shared among instances.
 - **Static Varibale**:
    - variable which is declared as static is called static variable.
    - can create single copy of static variable and share among all the instance of the class. 
    - Memory allocation for static variable happens only once when class is loaded in the memory.
```java 
class A{  
int data=50;//instance variable  
static int m=100;//static variable  
void method(){  
int n=90;//local variable  
}  
}//end of class  
````
---
