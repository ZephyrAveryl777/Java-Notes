---
title: Java Decision Making
created: '2021-04-05T19:18:17.993Z'
modified: '2021-04-05T19:34:58.591Z'
---

# Java Decision Making



### Java if Statement

- used to test the condition
-  It executes the if block if condition is true

```
//Syntax of If 
if(condition){  
//code to be executed  
}  
```

---

### Go if-else

- used to test condition
- If condition is true, if block is executed otherwise else block is executed.

```
//Syntax 
if(condition){  
//code if condition is true  
}else{  
//code if condition is false  
}  
```

---

### Using Ternary Operator

-  ternary operator (? :) is a shorthand way to check the condition
- If the condition is true, the result of ? is returned. But, if the condition is false, the result of : is returned.
```
public class IfElseTernaryExample {    
public static void main(String[] args) {    
    int number=13;    
    //Using ternary operator  
    String output=(number%2==0)?"even number":"odd number";    
    System.out.println(output);  
}    
}    
```
Output:

odd number
---

### Java if-else-if ladder Statement

The if-else-if ladder statement executes one condition from multiple statements.

```
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
```
Output:

NEGATIVE

---

### Java Nested if statement

-  if block within another if block
- the inner if block condition executes only when outer if block condition is true.



```//Java Program to demonstrate the use of Nested If Statement.  
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
```

Output:

You are eligible to donate blood




---


