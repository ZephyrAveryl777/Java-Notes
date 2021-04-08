---
title: LinkedList
created: '2021-04-08T11:11:13.523Z'
modified: '2021-04-08T12:44:06.956Z'
---

# LinkedList

- LinkedList is a linear data structure
- are not stored in contiguous locations like arrays, they are linked with each other using pointers
---

**LinkedList representation**

- Each element in the LinkedList is called the Node
- Each Node of the LinkedList contains two items:
      1) Content of the element 
      2) Pointer/Address/Reference to the Next Node in the LinkedList


 <img src="https://beginnersbook.com/wp-content/uploads/2013/12/singly_linkedlist.png"  width="100%" height="500px%" align="center" />

 *Linked list allows dynamic memory allocation, which means memory allocation is done at the run time by the compiler and we do not need to mention the size of the list during linked list declaration.*


 *Linked list elements don’t need contiguous memory locations*
 ---

 **Hierarchy of LinkedList class in Java**

<img src="https://beginnersbook.com/wp-content/uploads/2013/12/linkedlist.png"  width="100%" height="500px%" align="center" />
---

**Java Linked List example of adding elements**

```java
package com.beginnersbook;
import java.util.*;
public class JavaExample{
   public static void main(String args[]){

     LinkedList<String> list=new LinkedList<String>();

     //Adding elements to the Linked list
     list.add("Steve");
     list.add("Carl");
     list.add("Raj");

     //Adding an element to the first position
     list.addFirst("Negan");

     //Adding an element to the last position
     list.addLast("Rick");

     //Adding an element to the 3rd position
     list.add(2, "Glenn");

     //Iterating LinkedList
     Iterator<String> iterator=list.iterator();
     while(iterator.hasNext()){
       System.out.println(iterator.next());
     }
   } 
} 
/*
Output:
Negan
Steve
Glenn
Carl
Raj
Rick
*/
```
---

**Removing elements from the LinkedList**

```java
package com.beginnersbook;
import java.util.*;
public class JavaExample{
   public static void main(String args[]){

      LinkedList<String> list=new LinkedList<String>();

      //Adding elements to the Linked list
      list.add("Steve");
      list.add("Carl");
      list.add("Raj");
      list.add("Negan");
      list.add("Rick");

      //Removing First element
      //Same as list.remove(0);
      list.removeFirst();

      //Removing Last element
      list.removeLast();

      //Iterating LinkedList
      Iterator<String> iterator=list.iterator();
      while(iterator.hasNext()){
         System.out.print(iterator.next()+" ");
      }

      //removing 2nd element, index starts with 0
      list.remove(1);

      System.out.print("\nAfter removing second element: ");
      //Iterating LinkedList again
      Iterator<String> iterator2=list.iterator();
      while(iterator2.hasNext()){
         System.out.print(iterator2.next()+" ");
      }
   }
}
/*
Output:
Carl Raj Negan
After removing second element: Carl Negan
*/
```
---
**Methods of LinkedList class:**

