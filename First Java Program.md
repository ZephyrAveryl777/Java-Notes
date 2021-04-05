# First Java Program 
- Java Program, is a collection of objects that communicate via invoking each others methods. 

### Requirement for Java Programs 
For executing any java program, you need to
- Install the JDK if you don't have installed it, download the JDK and install it.
- Set path of the jdk/bin directory. http://www.javatpoint.com/how-to-set-path-in-java
- Create the java program
- Compile and run the java program
for further inforamtion or details refer Youtube or Google. 
---
### Hello World Program 
```java 
class Hello{
  public static void main(String args[]){
      System.out.println("Hello World");
     }
   }
/*
Output: Hello World
*/
````
> save the file as <FileName>.java, To compile: `**javac <FileName>.java**`, To execute: `**java <FileName>**`
--- 
### Paramaters used in First Java Program
- **Case Sensitivity** - Java is case sensitive, which means
identifier Helloand hello would have different meaning in Java.
- **Class Names** - For all class names the first letter should be in Upper Case.
If several words are used to form a name of the class, each inner word's first letter
should be in Upper Case.
Example: class MyFirstJavaClass
- **Method Names** - All method names should start with a Lower Case letter.
If several words are used to form the name of the method, then each inner word's
first letter should be in Upper Case.
Example: public void myMethodName()
- **Program File Name** - Name of the program file should exactly match the class
name.
When saving the file, you should save it using the class name (Remember Java is
case sensitive) and append `.java` to the end of the name (if the file name and the
class name do not match, your program will not compile).
Example: Assume 'MyFirstJavaProgram' is the class name. Then the file should
be saved as 'MyFirstJavaProgram.java'
- **public static void main(String args[])** - Java program processing starts from
the main() method which is a mandatory part of every Java program.
