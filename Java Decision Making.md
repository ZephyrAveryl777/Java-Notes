
# Java Decision Making

### Java if Statement

- used to test the condition
-  It executes the if block if condition is true

```java 
//Syntax of If 
if(condition){  
//code to be executed  
}  
```
<h3 align="center">
    <img src="https://www.alphacodingskills.com/java/img/java-if.png" alt="if loop" height="475px">
</h3>

```java 
//Java Program to demonstate the use of if statement.  
public class IfExample {  
public static void main(String[] args) {  
    //defining an 'age' variable  
    int age=20;  
    //checking the age  
    if(age>18){  
        System.out.print("Age is greater than 18");  
    }  
}  
}  
```
---

### Java if-else

- used to test condition
- If condition is true, if block is executed otherwise else block is executed.

```java
//Syntax 
if(condition){  
//code if condition is true  
}else{  
//code if condition is false  
}  
```
<h3 align="center">
    <img src="https://www.alphacodingskills.com/java/img/java-if-else.png" alt="if-else image" height="475px">
</h3>

```java 
//A Java Program to demonstrate the use of if-else statement.  
//It is a program of odd and even number.  
public class IfElseExample {  
public static void main(String[] args) {  
    //defining a variable  
    int number=13;  
    //Check if the number is divisible by 2 or not  
    if(number%2==0){  
        System.out.println("even number");  
    }else{  
        System.out.println("odd number");  
    }  
}  
}  
```
---

### Using Ternary Operator

-  ternary operator (? :) is a shorthand way to check the condition
- If the condition is true, the result of ? is returned. But, if the condition is false, the result of : is returned.
```java
public class IfElseTernaryExample {    
public static void main(String[] args) {    
    int number=13;    
    //Using ternary operator  
    String output=(number%2==0)?"even number":"odd number";    
    System.out.println(output);  
}    
}    
```
Output: odd number

---
### Java if-else-if ladder Statement

- The if-else-if ladder statement executes one condition from multiple statements.

```java
public class PositiveNegativeExample {    
public static void main(String[] args) {    
    int number=-13;    
    if(number>0){  
    System.out.println("POSITIVE");  
    }else if(number<0){  
    System.out.println("NEGATIVE");  
    }else{  
    System.out.println("ZERO");  
   }  
}    
} 
// Output: NEGATIVE
```
<h3 align="center">
    <img src="https://www.alphacodingskills.com/java/img/java-if-elseif-else.png" alt="if-else ladder" height="475px">
</h3>

---
### Java Nested if statement

-  if block within another if block
- the inner if block condition executes only when outer if block condition is true.

```java
//Java Program to demonstrate the use of Nested If Statement.  
public class JavaNestedIfExample {    
public static void main(String[] args) {    
    //Creating two variables for age and weight  
    int age=20;  
    int weight=80;    
    //applying condition on age and weight  
    if(age>=18){    
        if(weight>50){  
            System.out.println("You are eligible to donate blood");  
        }    
    }    
}}
// Output: You are eligible to donate blood
```
<h3 align="center">
    <img src="https://www.javatpoint.com/corebasic/images/nestedif.png" alt="NestedIFExample" height="750px" width="20%">
</h3>

---


