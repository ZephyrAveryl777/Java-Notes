# Access Modifiers in Java
- two types of modifiers in Java: 
    - **access modifiers** 
    - **non-access modifiers**.
-  access modifiers specifies the accessibility or scope of a field, method, constructor, or class. 
-  can change the access level of fields, constructors, methods, and class by applying the access modifier on it. 
- four types of Java access modifiers:
    1.  **Private**: 
    	- The access level of a private modifier is only within the class. 
    	- It cannot be accessed from outside the class.
    2.  **Default**: 
    	- The access level of a default modifier is only within the package. 
    	- It cannot be accessed from outside the package. 
    	- If you do not specify any access level, it will be the default.
    3.  **Protected**: 
    	- The access level of a protected modifier is within the package and outside the package through child class. 
    	- If you do not make a child class, it cannot be accessed from outside the package.
    4.  **Public**: 
    	- The access level of a public modifier is everywhere. 
    	- It can be accessed from within the class, outside the class, within the package and outside the package.

* * * * *

### Understanding Access Modifiers

| Modifier      | within class | within package | outside package by subclass only | outside package |
| ------------- | ------------ | -------------- | -------------------------------- | --------------- |
|  |
| **Private**   | Y            | N              | N                                | N               |
| **Default**   | Y            | Y              | N                                | N               |
| **Protected** | Y            | Y              | Y                                | N               |
| **Public**    | Y            | Y              | Y                                | Y     |

* * * * *

### Private
 - private access modifier is accessible only within the class.
- **Example**
```java
class A{  
private int data=40;  
private void msg(){System.out.println("Hello java");}  
}  
public class Simple{  
public static void main(String args[]){  
A obj=new A();  
System.out.println(obj.data);//Compile Time Error  
obj.msg();//Compile Time Error  
}  
}  
```

#### Role of Private Constructor
- a private class constructor cannot create the instance of that class from outside the class
```java
class A{  
private A(){}//private constructor  
void msg(){System.out.println("Hello java");}  
}  
public class Simple{  
public static void main(String args[]){  
A obj=new A();//Compile Time Error  
}  
}  
```
> **Note**: 
> - A class cannot be private or protected except nested class.

* * * * *

### Default

- If any modifier not used , it is treated as **default** by default. 
- default modifier is accessible only within package, cannot be accessed from outside the package. 
- provides more accessibility than private but is more restrictive than protected, and public. 
- **Example**:
```java
//save by A.java  
package pack;  
class A{  
void msg(){System.out.println("Hello");}  
}  
//save by B.java  
package mypack;  
import pack.*;  
class B{  
public static void main(String args[]){  
A obj = new A();//Compile Time Error  
obj.msg();//Compile Time Error  
}  
}  
```
* * * * *

### Protected

- **protected access modifier** is accessible within package and outside the package but through inheritance only.
- The protected access modifier can be applied on the data member, method and constructor. 
- It can't be applied on the class.
- It provides more accessibility than the default modifer.
- **Example**
```java
//save by A.java  
package pack;  
public class A{  
protected void msg(){System.out.println("Hello");}  
}  
//save by B.java  
package mypack;  
import pack.*;  
class B extends A{  
public static void main(String args[]){  
B obj = new B();  
obj.msg();  
}  
}  
/*
Output:Hello
*/
```
* * * * *

### Public

-  **public access modifier** is accessible everywhere. 
-  It has the widest scope among all other modifiers.
-  **Example**:
```java
//save by A.java  
package pack;  
public class A{  
public void msg(){System.out.println("Hello");}  
}  
//save by B.java  
package mypack;  
import pack.*;  
class B{  
public static void main(String args[]){  
A obj = new A();  
obj.msg();  
}  
}  
/*
Output:Hello
*/
```
* * * * *

### Java Access Modifiers with Method Overriding

- overridden method (i.e. declared in subclass) must not be more restrictive.
- default modifier is more restrictive than protected
```java
class A{  
protected void msg(){System.out.println("Hello java");}  
}  
public class Simple extends A{  
void msg(){System.out.println("Hello java");}//C.T.Error  
public static void main(String args[]){  
Simple obj=new Simple();  
obj.msg();  
}  
}  
```

---
