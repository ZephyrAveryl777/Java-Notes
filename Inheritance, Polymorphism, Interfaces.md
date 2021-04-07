# Inheritance, Polymorphism, Interfaces

**INHERITNCE**

```java
class Teacher {
   String designation = "Teacher";
   String college = "Beginnersbook";
   void does(){
	System.out.println("Teaching");
   }
}
public class MathTeacher extends Teacher{
   String mainSubject = "Maths";
   public static void main(String args[]){
      MathTeacher obj = new MathTeacher();
      System.out.println(obj.college);
      System.out.println(obj.designation);
      System.out.println(obj.mainSubject);
      obj.does();
   }
}

/*
Output:

Beginnersbook
Teacher
Maths
Teaching

*/
```

- Multi-level inheritance is allowed in Java but not multiple inheritance

<img src="https://beginnersbook.com/wp-content/uploads/2013/04/multilevel-multiple-inheritance.jpg" alt="Decision Making in Go"  width="100%" height="500px%" align="left" />



*Types of Inheritance:*
<img src="https://th.bing.com/th/id/OIP.EVWkQ9ZBkyIC8jTnujbEewHaD7?w=320&h=180&c=7&o=5&pid=1.7" alt="Decision Making in Go"  width="100%" height="500px%" align="left" />
---

**Polymorphism**
- an object oriented programming feature that allows us to perform a single action in different ways
- Types of Polymorphism
    1) Static Polymorphism
    2) Dynamic Polymorphism

*Static Polymorphism:*
- Polymorphism that is resolved during compiler time, eg:Method Overloading
```java
class DisplayOverloading
{
    public void disp(char c)
    {
         System.out.println(c);
    }
    public void disp(char c, int num)  
    {
         System.out.println(c + " "+num);
    }
}
public class ExampleOverloading
{
   public static void main(String args[])
   {
       DisplayOverloading obj = new DisplayOverloading();
       obj.disp('a');
       obj.disp('a',10);
   }
}
/*
Output:

a
a 10
*/
```
*Dynamic Polymorphism*
-  a process in which a call to an overridden method is resolved at runtime rather

```java
class Animal{
   public void animalSound(){
	System.out.println("Default Sound");
   }
}
public class Dog extends Animal{

   public void animalSound(){
	System.out.println("Woof");
   }
   public static void main(String args[]){
	Animal obj = new Dog();
	obj.animalSound();
   }
}
/*
Output:

Woof
*/
```
---

**Interfaces in Java**
- a blueprint of a class
- contain only constants and abstract methods (methods with only signatures no body)


<img src="https://th.bing.com/th/id/Rf22ac54d12ec03fa2b1c5f69af32e96c?rik=6lEbXjjWZDYg4g&riu=http%3a%2f%2f3.bp.blogspot.com%2f-iY5H3NVfu14%2fVmg99BkXpPI%2fAAAAAAAAES0%2fhKRMe87q1P4%2fs1600%2fabstract%252Bclass%252Bvs%252Binterface%252Bin%252BJava.png&ehk=I9Km3cbxzPlkJPgCio3onWBq4vFKMdBPvH8P6fn4O3E%3d&risl=&pid=ImgRawg" alt="Decision Making in Go"  width="100%" height="500px%" align="left" />


- Java does not support Multiple Inheritance, however a class can implement more than one interfaces
<img src="https://beginnersbook.com/wp-content/uploads/2013/04/Interface-example.jpg" alt="Decision Making in Go"  width="100%" height="500px%" align="left" />

*Access Specifiers*
- public: Accessible to all.
- private: Not accessible by other objects. Private members can be accessed only by the methods in the same class.
- protected: The scope of a protected variable is within the class which declares it and in the class which inherits from the class 
- Default: Scope is Package Level. 

