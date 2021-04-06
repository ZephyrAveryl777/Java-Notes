# Operators  
- symbols used to perform operations 
- there are many operators in Java:
  - Unary Operator,
  - Arithmetic Operator,
  - Shift Operator,
  - Relational Operator,
  - Bitwise Operator,
  - Logical Operator,
  - Ternary Operator and
  - Assignment Operator
----
### Operator Precedence 
| Operator Type        | Category                                | Precedence                               |
| -------------------- | --------------------------------------- | ---------------------------------------- |
|  |
| Unary                | postfix                                 | `_expr_++ _expr_--`                      |
| prefix               | `++_expr_ --_expr_ +_expr_ -_expr_ ~ !` |
| Arithmetic           | multiplicative                          | `* / %`                                  |
| additive             | `+ -`                                   |
| Shift                | shift                                   | `<< >> >>>`                              |
| Relational           | comparison                              | `< > <= >= instanceof`                   |
| equality             | `== !=`                                 |
| Bitwise              | bitwise AND                             | `&`                                      |
| bitwise exclusive OR | `^`                                     |
| bitwise inclusive OR | `|`                                     |
| Logical              | logical AND                             | `&&`                                     |
| logical OR           | `||`                                    |
| Ternary              | ternary                                 | `? :`                                    |
| Assignment           | assignment                              | `= += -= *= /= %= &= ^= |= <<= >>= >>>=` |

---
### Java Unary Operator 
- require only one operand 
- used to perform:
  - incrementing/decrementing a value by one
  - negating an expression 
  - inverting the value of a boolean
```java 
class OperatorExample{  
public static void main(String args[]){  
int x=10;  
System.out.println(x++);//10 (11)  
System.out.println(++x);//12  
System.out.println(x--);//12 (11)  
System.out.println(--x);//10  
}}  
```
---
### Java Arithmetic Operators 
- used to perform addition,subtraction,multiplication and division. 
- basic mathematical operations
```java 
class OperatorExample{  
public static void main(String args[]){  
int a=10;  
int b=5;  
System.out.println(a+b);//15  
System.out.println(a-b);//5  
System.out.println(a*b);//50  
System.out.println(a/b);//2  
System.out.println(a%b);//0  
}}  
````
| Operator            | Description                                                            | Example              |
| ------------------- | ---------------------------------------------------------------------- | -------------------- |
|  |
| \+ (Addition)       | Adds values on either side of the operator.                            | A + B will give 30   |
| \- (Subtraction)    | Subtracts right-hand operand from left-hand operand.                   | A - B will give -10  |
| \* (Multiplication) | Multiplies values on either side of the operator.                      | A \* B will give 200 |
| / (Division)        | Divides left-hand operand by right-hand operand.                       | B / A will give 2    |
| % (Modulus)         | Divides left-hand operand by right-hand operand and returns remainder. | B % A will give 0    |

