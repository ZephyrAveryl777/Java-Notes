---
title: HashSet and TreeSet Class in Java
created: '2021-04-09T09:21:08.338Z'
modified: '2021-04-09T09:38:38.859Z'
---

# HashSet and TreeSet Class in Java

**HashSet**

- This class implements the Set interface, backed by a hash table
- HashSet doesn’t maintain any order, the elements would be returned in any random order.
- HashSet doesn’t allow duplicates
- HashSet is non-synchronized.
     However it can be synchronized explicitly like this: 

     Set s = Collections.synchronizedSet(new HashSet(...));
---

**HashSet Example**

```java
import java.util.HashSet;
public class HashSetExample {
   public static void main(String args[]) {
      // HashSet declaration
      HashSet<String> hset = 
               new HashSet<String>();

      // Adding elements to the HashSet
      hset.add("Apple");
      hset.add("Mango");
      hset.add("Grapes");
      hset.add("Orange");
      hset.add("Fig");
      //Addition of duplicate elements
      hset.add("Apple");
      hset.add("Mango");
      //Addition of null values
      hset.add(null);
      hset.add(null);

      //Displaying HashSet elements
      System.out.println(hset);
    }
}
/*
Output:

[null, Mango, Grapes, Apple, Orange, Fig]
*/
```
---
**HashSet Methods**

boolean add(Element  e): It adds the element e to the list.

void clear(): It removes all the elements from the list.

Object clone(): This method returns a shallow copy of the HashSet.

boolean contains(Object o): It checks whether the specified Object o is present in the list or not. If the object has been found it returns true else false.

boolean isEmpty(): Returns true if there is no element present in the Set.

int size(): It gives the number of elements of a Set.

boolean(Object o): It removes the specified Object o from the Set.
---

**TreeSet**

- TreeSet is similar to HashSet except that it sorts the elements in the ascending order while HashSet doesn’t maintain any order.
-  this class is also not synchronized, however it can be synchronized explicitly like this: 

SortedSet s = Collections.synchronizedSortedSet(new TreeSet(...));
---

**TreeSet Example:**

```java

import java.util.TreeSet;
public class TreeSetExample {
     public static void main(String args[]) {
         // TreeSet of String Type
         TreeSet<String> tset = new TreeSet<String>();

         // Adding elements to TreeSet<String>
         tset.add("ABC");
         tset.add("String");
         tset.add("Test");
         tset.add("Pen");
         tset.add("Ink");
         tset.add("Jack");

         //Displaying TreeSet
         System.out.println(tset);

         // TreeSet of Integer Type
         TreeSet<Integer> tset2 = new TreeSet<Integer>();

         // Adding elements to TreeSet<Integer>
         tset2.add(88);
         tset2.add(7);
         tset2.add(101);
         tset2.add(0);
         tset2.add(3);
         tset2.add(222);
         System.out.println(tset2);
    }
 }
 /*
Output: You can see both the TreeSet have been sorted in ascending order implicitly.
*/
```
---


