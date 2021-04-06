## Type Casting 
- when you assign a value of one primitive data type to another type.
<br>
In Java, there are two types of casting:

- Widening Casting (automatically) - converting a smaller type to a larger type size
**`byte -> short -> char -> int -> long -> float -> double`**

- Narrowing Casting (manually) - converting a larger type to a smaller size type
**`double -> float -> long -> int -> char -> short -> byte`**

<h3 align="center">
  <img src="https://static.javatpoint.com/core/images/type-casting-in-java.png" alt="Type Casting image" height="350px">
</h3>

---
### Widening Casting 
- Converting a lower data type into a higher one
- also known as implicit conversion or casting down
- It is done automatically
- Its safe as no loss of data occurs 
- most done when: 
   -  Both data types must be compatible with each other.
    - The target type must be larger than the source type.
```java 
public class Main {
  public static void main(String[] args) {
    int myInt = 9;
    double myDouble = myInt; // Automatic casting: int to double

    System.out.println(myInt);      // Outputs 9
    System.out.println(myDouble);   // Outputs 9.0
  }
}
```
---
### Narrowing Casting
- Converting a higher data type into a lower one
- known as explicit conversion or casting up
- done manually; if not done properly, throws complie time error 
```java
public class Main {
  public static void main(String[] args) {
    double myDouble = 9.78;
    int myInt = (int) myDouble; // Manual casting: double to int

    System.out.println(myDouble);   // Outputs 9.78
    System.out.println(myInt);      // Outputs 9
  }
}
```
----
