# Encapsulation in Java

- **Encapsulation in Java** is a *process of wrapping code and data together into a single unit*.
- can create a fully encapsulated class  by making all the data members of the class private and can use setter and getter methods to set and get the data in it.
- Example of a fully encapsulated class **Java Bean** class

![Encapsulation in Java](https://media.geeksforgeeks.org/wp-content/uploads/Encapsulation.jpg)

**Advantages of Encapsulation**:  

-   **Data Hiding:** 
	-  The user will have no idea about the inner implementation of the class. 
	-  It will not be visible to the user how the class is storing values in the variables. 
	-  The user will only know that we are passing the values to a setter method and variables are getting initialized with that value.
-   **Increased Flexibility:** 
	-    make the variables of the class as read-only or write-know that only depending on our requirement. 
	-    if variables are read-only then, have to omit the setter methods like setName(), setAge(), etc. 
	-    if  variables as write-only then, have to omit the get methods like getName(), getAge(), etc. from the above program
-   **Reusability:** 
	-    improves the re-usability and easy to change with new requirements.
-   **Testing code is easy:** 
	-   Encapsulated code is easy to test for unit testing.

---

### Simple Examples of Encapsulation in Java

```java
// File: Student.java

//A fully encapsulated class 
// has a private data member and getter and setter methods.  
package sample;  
public class Student{  
//private data member  
private String name;  
//getter method for name  
public String getName(){  
return name;  
}  
//setter method for name  
public void setName(String name){  
this.name=name  
}  
}  

// File: Test.java

//A Java class to test the encapsulated class.  
package sample;  
class Test{  
public static void main(String[] args){  
//creating instance of the encapsulated class  
Student s=new Student();  
//setting value in the name member  
s.setName("SAM");  
//getting value of the name member  
System.out.println(s.getName());  
}  
}  
/*
Output: SAM
*/
```
> Compile By: 
> - **`javac -d . Test.java`**

> Run By: 
> - **`java sample.Test`**


### Read-Only class

```java
//A Java class which has only getter methods.  
public class Student{  
//private data member  
private String college="ABC";  
//getter method for college  
public String getCollege(){  
return college;  
}  
}  
```
> can't change the value of the college data member which is "ABC". 
> - `s.setCollege("KITE");//will render compile time error`  

### Write-Only class

```java
//A Java class which has only setter methods.  
public class Student{  
//private data member  
private String college;  
//getter method for college  
public void setCollege(String college){  
this.college=college;  
}  
}  
```

> can't get the value of the college, can only change the value of college data member. 

```java
System.out.println(s.getCollege());
//Compile Time Error, because there is no such method  

System.out.println(s.college);

//Compile Time Error, because the college data member is private.   
//So, it can't be accessed from outside the class  
```

### Reallife Example of Encapsulation in Java

```java
// File: Account.java

//A Account class which is a fully encapsulated class.  
//It has a private data member and getter and setter methods.  
class Account {  
//private data members  
private long acc_no;  
private String name,email;  
private float amount;  
//public getter and setter methods  
public long getAcc_no() {  
return acc_no;  
}  
public void setAcc_no(long acc_no) {  
this.acc_no = acc_no;  
}  
public String getName() {  
return name;  
}  
public void setName(String name) {  
this.name = name;  
}  
public String getEmail() {  
return email;  
}  
public void setEmail(String email) {  
this.email = email;  
}  
public float getAmount() {  
return amount;  
}  
public void setAmount(float amount) {  
this.amount = amount;  
}  
}

// File: TestAccount.java

//A Java class to test the encapsulated class Account.  
public class TestEncapsulation {  
public static void main(String[] args) {  
//creating instance of Account class  
Account acc=new Account();  
//setting values through setter methods  
acc.setAcc_no(56860504000L);  
acc.setName("Swan Jones");  
acc.setEmail("swanjones@gmail.com");  
acc.setAmount(500000f);  
//getting values through getter methods  
 System.out.println(acc.getAcc_no()+" "+acc.getName()+" "+acc.getEmail()+" "+acc.getAmount());  
}  
}  
/*
Output:
56860504000 Swan Jones swanjones@gmail.com 500000.0
*/
```

---
