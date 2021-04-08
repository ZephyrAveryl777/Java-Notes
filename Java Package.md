# Java Package
-  **package** is a group of similar types of classes, interfaces and sub-packages.
-  can be categorized in two form, built-in package and user-defined package. 
-  There are many built-in packages such as java, lang, awt, javax, swing, net, io, util, sql etc.

### Advantage of Java Package

        1) Java package is used to categorize the classes and interfaces so that they can be easily maintained.

        2) Java package provides access protection.

        3) Java package removes naming collision.

![package in java](https://static.javatpoint.com/images/package.JPG "package")
```java
//save as Simple.java  
package mypack;  
public class Simple{  
public static void main(String args[]){  
System.out.println("Welcome to package");  
}  
}  
```
---

### Compiling java package

- **Syntax** `javac -d directory javafilename`
- **Example** `javac -d . Simple.java`   


> - The -d switch specifies the destination where to put the generated class file. 
> - If you want to keep the package within the same directory, you can use . (dot).


### runing java package program

- need a fully qualified name.
- **To Compile:** javac -d . Simple.java 
- **To Run:** java mypack.Simple 

### accessing package from another package.

There are three ways to access the package from outside the package.

1.  import package.*;
2.  import package.classname;
3.  fully qualified name.

#### `Using packagename.*`

- if **`packagename.*`**  used. then all the classes and interfaces of this package will be accessible but not subpackages.
- import keyword is used to make the classes and interface of another package accessible to the current package.
- **Example**:
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
Output:
Hello
*/
````
* * * * *

#### `Using packagename.classname`

-  If **`package.classname`** is imported then only declared class of this package will be accessible.
-  **Example**:
```java

//save by A.java  

package pack;  
public class A{  
public void msg(){System.out.println("Hello");}  
}  

//save by B.java  
package mypack;  
import pack.A;  

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
---

#### `Using fully qualified name`

- If fully qualified name is used then only declared class of this package will be accessible. 
- no need to import. 
- need to use fully qualified name every time while accessing the class or interface.
- generally used when two packages have same class name e.g. `java.util` and `java.sql` packages contain Date class.
- **Example**:
```java
//save by A.java  
package pack;  
public class A{  
public void msg(){System.out.println("Hello");}  
}  

//save by B.java  
package mypack;  
class B{  
public static void main(String args[]){  
pack.A obj = new pack.A();//using fully qualified name  
obj.msg();  
}  
}  
/*
Output:Hello

```

> **Note:** 
> - If you import a package, all the classes and interface of that package will be imported excluding the classes and interfaces of the subpackages.
> - Sequence of the program must be package then import then class.

![sequence of package](https://static.javatpoint.com/images/sequenceofpackage.JPG "sequence of package")

* * * * *

### Subpackage in java

- Package inside the package is called the **subpackage**. 
- created **to categorize the package further**.
- **Example** 
```java
package com.javat.core;  
class Simple{  
public static void main(String args[]){  
System.out.println("Hello subpackage");  
}  
}  
// Output:Hello subpackage
```

-   **To Compile:** javac -d . Simple.java 
-   **To Run:** java com.javatpoint.core.Simple 

* * * * *

### Sending the class file to another directory or drive

- **Example**: to put the class file of A.java source file in classes folder of c: drive. 

![how to put class file in another package](https://static.javatpoint.com/images/anotherpackage.JPG "how to put class file in another package")

```java
//save as Simple.java  
package mypack;  
public class Simple{  
public static void main(String args[]){  
System.out.println("Welcome to package");  
}  
}  
// Output: Welcome to package
```

- To Compile:
- **e:\sources> javac -d c:\classes Simple.java**

- To Run:
- **e:\sources> set classpath=c:\classes.;**
- **e:\sources> java mypack.Simple**

**Another way to run this program by -classpath switch of java:**

-  **-classpath** switch can be used with javac and java tool.
- To run program from e:\source directory, can use -classpath switch of java that tells where to look for class file. 
- **Example**:
- **e:\sources> java -classpath c:\classes mypack.Simple**

* * * * *

### Ways to load the class files or jar files

There are two ways to load the class files temporary and permanent. 

-   Temporary
-   By setting the classpath in the command prompt
-   By -classpath switch
-   Permanent
-   By setting the classpath in the environment variables
-   By creating the jar file, that contains all the class files, and copying the jar file in the **jre/lib/ext** folder. 

> **Rule**: 
> - There can be only one public class in a java source file and it must be saved by the public class name.
```java
//save as C.java otherwise Compilte Time Error  
class A{}  
class B{}  
public class C{}  
```
* * * * *

### put two public classes in a package 

-  to put two public classes in a package, have two java source files containing one public class, but keep the package name same. 
-  **Example**:
```java
//save as A.java  
package javatutorial;  
public class A{}  
//save as B.java  
package javatutorial;  
public class B{}  
````

* * * * *

