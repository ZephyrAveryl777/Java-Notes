# Data Types 
- each variable must be a specified data type.
- Data types specify the different sizes and values that can be stored in the variable.
- These are of two types:
  - **Primitive data types**: 
    - Primitive data types include boolean, char,byte,short,int,long,float and double.
  - **Non primitive data types**:
    - includes Classes, Interfaces and Arrays.
 <h3 align="center">
  <img src="https://static.javatpoint.com/images/java-data-types.png" alt="Data Types" height="500px">
 </h3>
 
 ---
 
### Primitive Data Types
- building blocks of data manipulation 
- basic data types available in Java language. 

| **Data Type** | **Default Value** | **Default size** | **Description** | 
| ------------- | ----------------- | ---------------- | ---------|
| boolean       | false             | 1 bit            | Stores true or false values |
| char          | '\\u0000'         | 2 byte           |Stores a single character/letter or ASCII values |
| byte          | 0                 | 1 byte           |Stores whole numbers from -128 to 127 |
| short         | 0                 | 2 byte           |Stores whole numbers from -32,768 to 32,767|
| int           | 0                 | 4 byte           |Stores whole numbers from -2,147,483,648 to 2,147,483,647|
| long          | 0L                | 8 byte           |Stores whole numbers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807|
| float         | 0.0f              | 4 byte           |Stores fractional numbers. Sufficient for storing 6 to 7 decimal digits|
| double        | 0.0d              | 8 byte           |Stores fractional numbers. Sufficient for storing 15 decimal digits|

---
### Numbers 
- **Integers**:
  - stores whole numbers, positive or negative (such as 123 or -456), without decimals. 
  - valid types are byte,short,int and long. 
- **Floating point types**:
  - represents numbers with a fractional part, containing one or more decimals. 
  - two types: float and double.
---
### Integer Types
- **Byte**:
  - byte data type can store whole numbers from -128 to 127.
  - used instead of int or other integer types to save memory.
  ```java 
  byte number = 100;
  System.out.println(number);
  ````
- **Short**:
  - can store whole numbers from -32768 to 32767.
  ```java 
  short number = 5000;
  System.out.println(number);
  ```
- **Int**:
  - int can store whole numbers from -2147483648 to 2147483647 
  - preferred data type to create variables with a numeric value.
  ```java 
  int number = 100000;
  System.out.println(number);
   ```
 - **Long**:
   - long data type can store whole numbers from -9223372036854775808 to 9223372036854775807.
   - used when int is not large enough to store the value. 
   - end the value with an "L".
   ```java
   long number = 15000000L;
   System.out.println(number);
   ````
 ---
 ### Floating Point Types
 - use a floating point type whenever you need a number with a decimal, such as 9.99 or 3.145
 - **Float**:
   - float data type can store fractional numbers from 3.4e-038 to 3.4e+038. 
   - end value with an "f".
   ```java
   float number = 5.52f;
   System.out.println(number);
   ```
 - **Double**:
   - double data type can store fractional numbers from 1.7e-308 to 1.7e+308. 
   - end value with a "d".
   ```java
   double number = 19.99d;
   System.out.println(number);
   ```
> The precision of float is only six or seven decimal digits, while double variables have a precision of about 15 digits. Therefore it is safer to use double for most calculations.
- Floating point numbers can also be a scientific number with an "e" to indicate the power of 10.
```java
float f1 = 35e3f;
double d1 = 12E4d;
System.out.println(f1);
System.out.println(d1);
```
---
### Booleans
-  declared with the boolean keyword and can only take the values `true` or `false`
-  mostly used for conditional testing.
```java
boolean isJavaFun = true;
boolean isFishTasty = false;
System.out.println(isJavaFun);     // Outputs true
System.out.println(isFishTasty);   // Outputs false
```
---
### Characters 
- char data type is used to store a single character. 
- character must surround in single quotes like 'A' or 'B'.
```java 
char character = 'A';
System.out.println(character);
````
- ASCII values can be used to display certain characters.
```java
char a = 65, b = 66, c = 67;
System.out.println(a);
System.out.println(b);
System.out.println(c);
```
---
### Strings 
- string data type is used to store a sequence of characters.
- string values must be surrounded by double quotes.
```java 
String greeting = "Hello World";
System.out.println(greeting);
```
---
### Non-Primitive Data Types
Non-primitive data types are called reference types because they refer to objects.

The main difference between primitive and non-primitive data types are:

Primitive types are predefined (already defined) in Java. Non-primitive types are created by the programmer and is not defined by Java (except for String).
Non-primitive types can be used to call methods to perform certain operations, while primitive types cannot.
A primitive type has always a value, while non-primitive types can be null.
A primitive type starts with a lowercase letter, while non-primitive types starts with an uppercase letter.
The size of a primitive type depends on the data type, while non-primitive types have all the same size.
