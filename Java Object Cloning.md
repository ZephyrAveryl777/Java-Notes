# Object Cloning in Java

![constructor in java](http://spiroprojects.com/webadmin/uploads/Shallow%20vs%20Deep%20Clone%20Java.png)

- **object cloning** is a way to create exact copy of an object. 
- The **clone()** method of Object class is used to clone an object. 
- The **java.lang.Cloneable interface** must be implemented by the class whose object clone we want to create. 
- If not implemented Cloneable interface, clone() method generates **CloneNotSupportedException**. 
- **syntax** `protected Object clone() throws CloneNotSupportedException` 
- **clone() method** saves the extra processing task for creating the exact copy of an object. 
- If  performed by using the new keyword, it will take a lot of processing time to be performed that is why we use object cloning.

### Advantage of Object cloning

 - Although Object.clone() has some design issues but it is still a popular and easy way of copying objects. Following is a list of advantages of using clone() method:

-   You don't need to write lengthy and repetitive codes. Just use an abstract class with a 4- or 5-line long clone() method.
-   It is the easiest and most efficient way for copying objects, especially if we are applying it to an already developed or an old project. Just define a parent class, implement Cloneable in it, provide the definition of the clone() method and the task will be done. 
-   Clone() is the fastest way to copy array.

### Disadvantage of Object cloning

Following is a list of some disadvantages of clone() method:

-   To use the Object.clone() method, we have to change a lot of syntaxes to our code, like implementing a Cloneable interface, defining the clone() method and handling CloneNotSupportedException, and finally, calling Object.clone() etc.
-   We have to implement cloneable interface while it doesn't have any methods in it. We just have to use it to tell the JVM that we can perform clone() on our object.
-   Object.clone() is protected, so we have to provide our own clone() and indirectly call Object.clone() from it.
-   Object.clone() doesn't invoke any constructor so we don't have any control over object construction.
-   If you want to write a clone method in a child class then all of its superclasses should define the clone() method in them or inherit it from another parent class. Otherwise, the super.clone() chain will fail.
-   Object.clone() supports only shallow copying but we will need to override it if we need deep cloning.

### Example of clone() method (Object cloning)

Let's see the simple example of object cloning

[](https://www.javatpoint.com/object-cloning#)[](https://www.javatpoint.com/object-cloning#)[](https://www.javatpoint.com/object-cloning#)

1.  class Student18 implements Cloneable{  
2.  int rollno;  
3.  String name;  

5.  Student18(int rollno,String name){  
6.  this.rollno=rollno;  
7.  this.name=name;  
8.  }  

10. public Object clone()throws CloneNotSupportedException{  
11. return super.clone();  
12. }  

14. public static void main(String args[]){  
15. try{  
16. Student18 s1=new Student18(101,"amit");  

18. Student18 s2=(Student18)s1.clone();  

20. System.out.println(s1.rollno+" "+s1.name);  
21. System.out.println(s2.rollno+" "+s2.name);  

23. }catch(CloneNotSupportedException c){}  

25. }  
26. }  

[Test it Now](https://www.javatpoint.com/opr/test.jsp?filename=Student18)

Output:101 amit
       101 amit

[download the example of object cloning](https://static.javatpoint.com/src/oops/clone.zip)

As you can see in the above example, both reference variables have the same value. Thus, the clone() copies the values of an object to another. So we don't need to write explicit code to copy the value of an object to another.

If we create another object by new keyword and assign the values of another object to this one, it will require a lot of processing on this object. So to save the extra processing task we use clone() method.
