---
title: Java Collections- ArrayList
created: '2021-04-08T09:57:42.319Z'
modified: '2021-04-08T10:54:44.772Z'
---

# Java Collections- ArrayList

- The Java Collections Framework is a collection of interfaces and classes which helps in storing and processing the data efficiently


 <img src="https://beginnersbook.com/wp-content/uploads/2013/12/Java-collection-framework-hierarchy.png" alt="Decision Making in Go"  width="50%" height="100px%" align="center" />

 **Java Collections – List**
 - an ordered Collection
 - Elements can be inserted or accessed by their position in the list, using a zero-based index
---

 ***ArrayList***

 - implements List interface and it is based on an Array data structure
 - a resizable-array implementation of the List interface
---
 **Why ArrayList is better than Array?**

 - ArrayList can dynamically grow and shrink after addition and removal of elements

 <img src="https://beginnersbook.com/wp-content/uploads/2013/12/Adding_Element_ArrayList_diagram.png" alt="Decision Making in Go"  width="50%" height="100px%" align="center" />

 <img src="https://beginnersbook.com/wp-content/uploads/2013/12/Removing_Element_from_ArrayList_diagram.png" alt="Decision Making in Go"  width="50%" height="100px%" align="center" />
---
 **How to create an ArrayList?**

 - ArrayList that accepts String
 ```java
 ArrayList<String> alist=new ArrayList<String>();
 ```

- ArrayList that accepts int elements
```java
ArrayList<Integer> list=new ArrayList<Integer>();
```
---
**How to add elements to an ArrayList?**

- We add elements to an ArrayList by using add() method

```java
import java.util.*;  
class JavaExample{  
   public static void main(String args[]){  
      ArrayList<String> alist=new ArrayList<String>();  
      alist.add("Steve");
      alist.add("Tim");
      alist.add("Lucy");
      alist.add("Pat");
      alist.add("Angela");
      alist.add("Tom");
  
      //displaying elements
      System.out.println(alist);
  
      //Adding "Steve" at the fourth position
      alist.add(3, "Steve");
  
      //displaying elements
      System.out.println(alist);
   }  
}
/*
Output:

[Steve, Tim, Lucy, Pat, Angela, Tom]
[Steve, Tim, Lucy, Steve, Pat, Angela, Tom]*/
```
---

**Change an element in ArrayList**

-  use the set method to change an element in ArrayList
- provide the index and new element, this method then updates the element present at the given index with the new given element

```java
import java.util.ArrayList;
public class JavaExample {
   public static void main(String[] args) {
      ArrayList<String> names = new ArrayList<String>();
      names.add("Jim");
      names.add("Jack");
      names.add("Ajeet");
      names.set(0, "Lucy");
      System.out.println(names);
   }
}
/* Output
[Lucy,Jack,Ajeet]*/
```
---

**How to remove elements from ArrayList?**

- use remove() method to remove elements from an ArrayList

```java
import java.util.*;
class JavaExample{
   public static void main(String args[]){
      ArrayList<String> alist=new ArrayList<String>(); 
      alist.add("Steve");
      alist.add("Tim");
      alist.add("Lucy");
      alist.add("Pat");
      alist.add("Angela");
      alist.add("Tom");

      //displaying elements
      System.out.println(alist);

      //Removing "Steve" and "Angela"
      alist.remove("Steve");
      alist.remove("Angela");

      //displaying elements
      System.out.println(alist);

      //Removing 3rd element
      alist.remove(2);

      //displaying elements
      System.out.println(alist);
   }
}
/*
Output:

[Steve, Tim, Lucy, Pat, Angela, Tom]
[Tim, Lucy, Pat, Tom]
[Tim, Lucy, Tom]
*/
```
---

**Iterating ArrayList**

```java
import java.util.*;  
class JavaExample{  
  public static void main(String args[]){  
     ArrayList<String> alist=new ArrayList<String>();  
     alist.add("Gregor Clegane");  
     alist.add("Khal Drogo");  
     alist.add("Cersei Lannister");  
     alist.add("Sandor Clegane"); 
     alist.add("Tyrion Lannister");
  
     //iterating ArrayList
     for(String str:alist)  
        System.out.println(str);  
     }  
}
/*
Output:

Gregor Clegane
Khal Drogo
Cersei Lannister
Sandor Clegane
Tyrion Lannister
*/
```
---

**ArrayList Size**

```java
import java.util.ArrayList;

public class JavaExample {
   public static void main(String[] args) {
      ArrayList<Integer> numbers = new ArrayList<Integer>();
      numbers.add(1);
      numbers.add(7);
      numbers.add(5);
      numbers.add(6);

      //We can use size() method of ArrayList to find the number of elements in an ArrayList. 

      System.out.println("Number of elements in ArrayList: "+numbers.size());
   }
}
/*
Output:
Number of elements in ArrayList: 4
*/
```
---

**Sort ArrayList**

```java
import java.util.ArrayList;
import java.util.Collections;

public class JavaExample {
   public static void main(String[] args) {
      ArrayList<String> fruits = new ArrayList<String>();
      fruits.add("Orange");
      fruits.add("Apple");
      fruits.add("Banana");
      fruits.add("Pineapple");

      //**We have a sort() method in the Collections class.**

      Collections.sort(fruits);

      for (String str : fruits) {
         System.out.println(str);
      }
   }
}
/*
Output:
  Apple
  Banana
  Orange
  Pineapple
  */
```
---
