# Arrays in Java 
- Array, collection of similar type of elements which has contiguous memory location.
- index based, first element of array is stored at 0th index, 2nd element stored on 1st index and so on.
-  object of a dynamically generated class. 
- inherits the Object class, implements the Serializables as well as Cloneable interface. 
- can store primitive values or objects in array. 

<h3 align="center">
  <img src="https://beginnersbook.com/wp-content/uploads/2018/10/array.jpg" alt="array-image" height="258px">
</h3>

- **Advantages**
  	- **Code Optimization**: easy retrieve or storting of data.
  	- **Random access**: get any data located at an index poistion.
- **Disadvantages** : 
  - **Size Limit**: 
    - store only fixed size of elements in array.
    - doesnot grow its size at runtime. 
    - to make an array grow automatically collection framework is used 
----
### Types of Array
- **Single Dimensional Array**: 
  - Syntax to Declare an Array in Java: 
    ```java 
    dataType[] arr; (or)
    dataType []arr; (or)
    dataType arr[];
    ````
    - Instantiation of an Array in Java
    ````java 
    arrayRefVar = new datatype[size]
    ````
    - Example of Java Array 
    ```java 
    class Testarray{  
    public static void main(String args[]){  
    int a[]=new int[5];//declaration and instantiation  
    a[0]=10;//initialization  
    a[1]=20;  
    a[2]=70;  
    a[3]=40;  
    a[4]=50;  
    //traversing array  
    for(int i=0;i<a.length;i++)//length is the property of array  
    System.out.println(a[i]);  
    }} 
    ```
    
    
---
