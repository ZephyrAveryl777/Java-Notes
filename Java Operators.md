# Operators  
- symbols used to perform operations 
- there are many operators in Java:
  - Arithmetic Operator,
  - Relational Operator,
  - Bitwise Operator,
  - Logical Operator,
  - Ternary Operator and
  - Assignment Operator
----
### Operator Precedence 
| Operator Type        | Category                                | Precedence                               |
| -------------------- | --------------------------------------- | ---------------------------------------- |
| Unary                | postfix   `_expr_++ _expr_--`           | prefix    `++_expr_ --_expr_ +_expr_ -_expr_ ~ !`|
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

---
### Relational Operators 
- holds the relations between different operands 
- mostly used for comparision and for finding a relation among operands
```java 
class OperatorExample{  
public static void main(String args[]){  
int a=10;  
int b=5;  
int c=20;  
System.out.println(a<b&&a<c);//false && true = false  
System.out.println(a<b&a<c);//false & true = false   
}}  
````
| Operator                       | Description                                                                                                                     | Example               |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------- | --------------------- |
|  |
| \== (equal to)                 | Checks if the values of two operands are equal or not, if yes then condition becomes true.                                      | (A == B) is not true. |
| != (not equal to)              | Checks if the values of two operands are equal or not, if values are not equal then condition becomes true.                     | (A != B) is true.     |
| \> (greater than)              | Checks if the value of left operand is greater than the value of right operand, if yes then condition becomes true.             | (A > B) is not true.  |
| < (less than)                  | Checks if the value of left operand is less than the value of right operand, if yes then condition becomes true.                | (A < B) is true.      |
| \>= (greater than or equal to) | Checks if the value of left operand is greater than or equal to the value of right operand, if yes then condition becomes true. | (A >= B) is not true. |
| <= (less than or equal to)     | Checks if the value of left operand is less than or equal to the value of right operand, if yes then condition becomes true.    | (A <= B) is true.     |

---
### Bitwise Operators
- Bitwise operators work on bits and performs bit-by-bit operation
- can be applied to the integer types,long,int,short,char,and byte. 
```java 
public class Test {
   public static void main(String args[]) {
      int a = 60;	/* 60 = 0011 1100 */
      int b = 13;	/* 13 = 0000 1101 */
      int c = 0;
      c = a & b;        /* 12 = 0000 1100 */
      System.out.println("a & b = " + c );
      c = a | b;        /* 61 = 0011 1101 */
      System.out.println("a | b = " + c );
      c = a ^ b;        /* 49 = 0011 0001 */
      System.out.println("a ^ b = " + c );
      c = ~a;           /*-61 = 1100 0011 */
      System.out.println("~a = " + c );
      c = a << 2;       /* 240 = 1111 0000 */
      System.out.println("a << 2 = " + c );
      c = a >> 2;       /* 15 = 1111 */
      System.out.println("a >> 2  = " + c );
      c = a >>> 2;      /* 15 = 0000 1111 */
      System.out.println("a >>> 2 = " + c );
   }
}
```
| Operator                     | Description                                                                                                                                                              | Example                                                                                      |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------- |
|  |
| & (bitwise and)              | Binary AND Operator copies a bit to the result if it exists in both operands.                                                                                            | (A & B) will give 12 which is 0000 1100                                                      |
| | (bitwise or)               | Binary OR Operator copies a bit if it exists in either operand.                                                                                                          | (A | B) will give 61 which is 0011 1101                                                      |
| ^ (bitwise XOR)              | Binary XOR Operator copies the bit if it is set in one operand but not both.                                                                                             | (A ^ B) will give 49 which is 0011 0001                                                      |
| ~ (bitwise compliment)       | Binary Ones Complement Operator is unary and has the effect of 'flipping' bits.                                                                                          | (~A ) will give -61 which is 1100 0011 in 2's complement form due to a signed binary number. |
| << (left shift)              | Binary Left Shift Operator. The left operands value is moved left by the number of bits specified by the right operand.                                                  | A << 2 will give 240 which is 1111 0000                                                      |
| \>> (right shift)            | Binary Right Shift Operator. The left operands value is moved right by the number of bits specified by the right operand.                                                | A >> 2 will give 15 which is 1111                                                            |
| \>>> (zero fill right shift) | Shift right zero fill operator. The left operands value is moved right by the number of bits specified by the right operand and shifted values are filled up with zeros. | A >>>2 will give 15 which is 0000 1111                                                       |

---
### Logical Operator
- used for having a logical understanding among the operands
- returned value will always be a boolean 
```java 
public class Test {

   public static void main(String args[]) {
      boolean a = true;
      boolean b = false;

      System.out.println("a && b = " + (a&&b));
      System.out.println("a || b = " + (a||b) );
      System.out.println("!(a && b) = " + !(a && b));
   }
}
````
| Operator         | Description                                                                                                                                      | Example           |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------- |
|  |
| && (logical and) | Called Logical AND operator. If both the operands are non-zero, then the condition becomes true.                                                 | (A && B) is false |
| || (logical or)  | Called Logical OR Operator. If any of the two operands are non-zero, then the condition becomes true.                                            | (A || B) is true  |
| ! (logical not)  | Called Logical NOT Operator. Use to reverses the logical state of its operand. If a condition is true then Logical NOT operator will make false. | !(A && B) is true |

---
### Assignment Operator 
- assign values to variables 
```java
public class Test {
   public static void main(String args[]) {
      int a = 10;
      int b = 20;
      int c = 0;
      c = a + b;
      System.out.println("c = a + b = " + c );
      c += a ;
      System.out.println("c += a  = " + c );
      c -= a ;
      System.out.println("c -= a = " + c );
      c *= a ;
      System.out.println("c *= a = " + c );
      a = 10;
      c = 15;
      c /= a ;
      System.out.println("c /= a = " + c );
      a = 10;
      c = 15;
      c %= a ;
      System.out.println("c %= a  = " + c );
      c <<= 2 ;
      System.out.println("c <<= 2 = " + c );
      c >>= 2 ;
      System.out.println("c >>= 2 = " + c );
      c >>= 2 ;
      System.out.println("c >>= 2 = " + c );
      c &= a ;
      System.out.println("c &= a  = " + c );
      c ^= a ;
      System.out.println("c ^= a   = " + c );
      c |= a ;
      System.out.println("c |= a   = " + c );
   }
}
```
| Operator | Description                                                                                                                | Example                                     |
| -------- | -------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------- |
|  |
| \=       | Simple assignment operator. Assigns values from right side operands to left side operand.                                  | C = A + B will assign value of A + B into C |
| +=       | Add AND assignment operator. It adds right operand to the left operand and assign the result to left operand.              | C += A is equivalent to C = C + A           |
| \-=      | Subtract AND assignment operator. It subtracts right operand from the left operand and assign the result to left operand.  | C -= A is equivalent to C = C – A           |
| \*=      | Multiply AND assignment operator. It multiplies right operand with the left operand and assign the result to left operand. | C \*= A is equivalent to C = C \* A         |
| /=       | Divide AND assignment operator. It divides left operand with the right operand and assign the result to left operand.      | C /= A is equivalent to C = C / A           |
| %=       | Modulus AND assignment operator. It takes modulus using two operands and assign the result to left operand.                | C %= A is equivalent to C = C % A           |
| <<=      | Left shift AND assignment operator.                                                                                        | C <<= 2 is same as C = C << 2               |
| \>>=     | Right shift AND assignment operator.                                                                                       | C >>= 2 is same as C = C >> 2               |
| &=       | Bitwise AND assignment operator.                                                                                           | C &= 2 is same as C = C & 2                 |
| ^=       | bitwise exclusive OR and assignment operator.                                                                              | C ^= 2 is same as C = C ^ 2                 |
| |=       | bitwise inclusive OR and assignment operator.                                                                              | C |= 2 is same as C = C | 2                 |

---
### Ternary Operator 
- also known as conditional operator
- consists of three operands and is used to evaluate Boolean expressions 
- **Syntax**:  **`variable x = (expression) ? value if true : value if false`**
```java
public class Test {
   public static void main(String args[]) {
      int a, b;
      a = 10;
      b = (a == 1) ? 20: 30;
      System.out.println( "Value of b is : " +  b );
      b = (a == 10) ? 20: 30;
      System.out.println( "Value of b is : " + b );
   }
}
/*
Output
Value of b is : 30
Value of b is : 20
*/
```
---
### instance of Operator 
- used for object reference variables 
- checks for whether the object is a praticular type 
- **Syntax** **`(Object refernce variable) instanceof (class/interface type)`**
```java 
public class Test {
   public static void main(String args[]) {
      String name = "James";
      // following will return true since name is type of String
      boolean result = name instanceof String;
      System.out.println( result );
   }
}
```
---


