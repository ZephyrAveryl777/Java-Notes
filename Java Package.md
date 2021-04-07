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

#### 1) Using packagename.*

If you use package.* then all the classes and interfaces of this package will be accessible but not subpackages.

The import keyword is used to make the classes and interface of another package accessible to the current package.

Example of package that import the packagename.*
------------------------------------------------

[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)

1.  //save by A.java  
2.  package pack;  
3.  public class A{  
4.  public void msg(){System.out.println("Hello");}  
5.  }  

[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)

1.  //save by B.java  
2.  package mypack;  
3.  import pack.*;  

5.  class B{  
6.  public static void main(String args[]){  
7.  A obj = new A();  
8.  obj.msg();  
9.  }  
10. }  

Output:Hello

* * * * *

#### 2) Using packagename.classname

If you import package.classname then only declared class of this package will be accessible.

Example of package by import package.classname
----------------------------------------------

[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)

1.  //save by A.java  

3.  package pack;  
4.  public class A{  
5.  public void msg(){System.out.println("Hello");}  
6.  }  

[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)

1.  //save by B.java  
2.  package mypack;  
3.  import pack.A;  

5.  class B{  
6.  public static void main(String args[]){  
7.  A obj = new A();  
8.  obj.msg();  
9.  }  
10. }  

Output:Hello

* * * * *

#### 3) Using fully qualified name

If you use fully qualified name then only declared class of this package will be accessible. Now there is no need to import. But you need to use fully qualified name every time when you are accessing the class or interface.

It is generally used when two packages have same class name e.g. java.util and java.sql packages contain Date class.

Example of package by import fully qualified name
-------------------------------------------------

[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)

1.  //save by A.java  
2.  package pack;  
3.  public class A{  
4.  public void msg(){System.out.println("Hello");}  
5.  }  

[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)

1.  //save by B.java  
2.  package mypack;  
3.  class B{  
4.  public static void main(String args[]){  
5.  pack.A obj = new pack.A();//using fully qualified name  
6.  obj.msg();  
7.  }  
8.  }  

Output:Hello

#### Note: If you import a package, subpackages will not be imported.

If you import a package, all the classes and interface of that package will be imported excluding the classes and interfaces of the subpackages. Hence, you need to import the subpackage as well.

* * * * *

#### Note: Sequence of the program must be package then import then class.

![sequence of package](https://static.javatpoint.com/images/sequenceofpackage.JPG "sequence of package")

* * * * *

Subpackage in java
------------------

Package inside the package is called the **subpackage**. It should be created **to categorize the package further**.

Let's take an example, Sun Microsystem has definded a package named java that contains many classes like System, String, Reader, Writer, Socket etc. These classes represent a particular group e.g. Reader and Writer classes are for Input/Output operation, Socket and ServerSocket classes are for networking etc and so on. So, Sun has subcategorized the java package into subpackages such as lang, net, io etc. and put the Input/Output related classes in io package, Server and ServerSocket classes in net packages and so on.

#### The standard of defining package is domain.company.package e.g. com.javatpoint.bean or org.sssit.dao.

### Example of Subpackage

[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)

1.  package com.javatpoint.core;  
2.  class Simple{  
3.  public static void main(String args[]){  
4.  System.out.println("Hello subpackage");  
5.  }  
6.  }  

| **To Compile:** javac -d . Simple.java |
| **To Run:** java com.javatpoint.core.Simple |

Output:Hello subpackage

* * * * *

How to send the class file to another directory or drive?
---------------------------------------------------------

There is a scenario, I want to put the class file of A.java source file in classes folder of c: drive. For example:

![how to put class file in another package](https://static.javatpoint.com/images/anotherpackage.JPG "how to put class file in another package")

[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)

1.  //save as Simple.java  
2.  package mypack;  
3.  public class Simple{  
4.  public static void main(String args[]){  
5.  System.out.println("Welcome to package");  
6.  }  
7.  }  

### To Compile:

**e:\sources> javac -d c:\classes Simple.java**

### To Run:

| To run this program from e:\source directory, you need to set classpath of the directory where the class file resides. |
| **e:\sources> set classpath=c:\classes;.;** |
| **e:\sources> java mypack.Simple** |

### Another way to run this program by -classpath switch of java:

The -classpath switch can be used with javac and java tool.

To run this program from e:\source directory, you can use -classpath switch of java that tells where to look for class file. For example:

**e:\sources> java -classpath c:\classes mypack.Simple**

Output:Welcome to package

* * * * *

### Ways to load the class files or jar files

| There are two ways to load the class files temporary and permanent. |

-   Temporary
    -   By setting the classpath in the command prompt
    -   By -classpath switch
-   Permanent
    -   By setting the classpath in the environment variables
    -   By creating the jar file, that contains all the class files, and copying the jar file in the jre/lib/ext folder. 

* * * * *

#### Rule: There can be only one public class in a java source file and it must be saved by the public class name.

[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)

1.  //save as C.java otherwise Compilte Time Error  

3.  class A{}  
4.  class B{}  
5.  public class C{}  

* * * * *

### How to put two public classes in a package? 

| If you want to put two public classes in a package, have two java source files containing one public class, but keep the package name same. For example: |

[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)

1.  //save as A.java  

3.  package javatpoint;  
4.  public class A{}  

[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)[](https://www.javatpoint.com/package#)

1.  //save as B.java  

3.  package javatpoint;  
4.  public class B{}  

* * * * *
