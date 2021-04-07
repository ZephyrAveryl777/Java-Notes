# Comments in Java 
- comments are not executed by the compiler and interpreter. 
- provide information or explanation about variable,method,calss or any statement. 
- also used to hide program

<h3 align="center">
  <img src="https://javatpoint.com/images/java-types-of-comments.png" alt="" height="">
</h3>

---

### Types of Java Comments 

- **Single Comment**:  
  - used to comment only one line 
  - **Syntax**: `**// This is a single line comment**`
 ```java 
 public class CommentExample1 {  
public static void main(String[] args) {  
    int i=10; //Here, i is a variable  
    System.out.println(i); // Ouput is 10  
}  
} 
```
- **Multi Line Comment**:
  - comment multiple lines of code.
```java 
/*
This 
is a
multiple 
line 
comment 
*/
```
  - Example 
  ````java
  public class CommentExample2 {  
public static void main(String[] args) {  
/* Let's declare and 
 print variable in java. */  
    int i=10;  
    System.out.println(i);  
}  
}
  ````
- **Documentation Comment**:
   - used to create documentation API.
   - need javadoc tool 
   - **Syntax**:
   ```java
   /** 
  This  
  is  
  documentation  
  comment 
  */
   ````
  - Example:
 ```java 
 /** The Calculator class provides methods to get addition and subtraction of given 2 numbers.*/  
public class Calculator {  
/** The add() method returns addition of given numbers.*/  
public static int add(int a, int b){return a+b;}  
/** The sub() method returns subtraction of given numbers.*/  
public static int sub(int a, int b){return a-b;}  
}  
// 
Compile it by javac tool : javac Calculator.java
create documentation API by javadoc tool: javadoc Calculator.java
 ```
----
