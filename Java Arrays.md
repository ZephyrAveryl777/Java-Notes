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
   - **Declaration**, **Instantiation** and **Initialization** of Java Array
     - **Syntax**: `**int a[]={1,2,3,4,5}**`
     - Example: 
     ```java 
     class Testarray1{  
      public static void main(String args[]){  
      int a[]={33,3,4,5};//declaration, instantiation and initialization  
      //printing array  
      for(int i=0;i<a.length;i++)//length is the property of array  
      System.out.println(a[i]);  
      }} 
      /* 
      Output:
      33
      3
      4
      5
      */
     ````
     - For-each Loop Array 
       - for-each loop prints array elements one by one.
       - it holds an array element in a variable, then executes the body of the loop. 
       - **Syntax**: `for(data_type variable:array){//body of the loop}`
       - **Example**:
      ```java 
       class Testarray1{  
      public static void main(String args[]){  
      int arr[]={33,3,4,5};  
      //printing array using for-each loop  
      for(int i:arr)  
      System.out.println(i);  
      }}
       ````
     - Passing Array to a Method 
     ```java 
     class Testarray2{  
      //creating a method which receives an array as a parameter  
      static void min(int arr[]){  
      int min=arr[0];  
      for(int i=1;i<arr.length;i++)  
       if(min>arr[i])  
        min=arr[i];  

      System.out.println(min);  
      }  

      public static void main(String args[]){  
      int a[]={33,3,4,5};//declaring and initializing an array  
      min(a);//passing array to method  
      }}  // Output: 3
     ````
     - Anonymous Array in Java 
       - need not delcare the array while passing an array to the method. 
     ```java 
     public class TestAnonymousArray{  
      //creating a method which receives an array as a parameter  
      static void printArray(int arr[]){  
      for(int i=0;i<arr.length;i++)  
      System.out.println(arr[i]);  
      }  

      public static void main(String args[]){  
      printArray(new int[]{10,22,44,66});//passing anonymous array to method  
      }}  
     ````
      - Returning Array from the Method
      ```java 
      class TestReturnArray{  
      //creating method which returns an array  
      static int[] get(){  
      return new int[]{10,30,50,90,60};  
      }  

      public static void main(String args[]){  
      //calling method which returns an array  
      int arr[]=get();  
      //printing the values of an array  
      for(int i=0;i<arr.length;i++)  
      System.out.println(arr[i]);  
      }}  
      ````
      - ArrayIndexOutofBoundsException
        - JVM throws ArrayIndexOutofBoundsException if length of the array is negative, equal to the array size or greater than the array size while traversing the array.
      ```java
      public class TestArrayException{  
      public static void main(String args[]){  
      int arr[]={50,60,70,80};  
      for(int i=0;i<=arr.length;i++){  
      System.out.println(arr[i]);  
      }  
      }}  
      ````
 
- **Multidimensional Array**: 
  - data is stored in row and column based index (matrix form)
  - **Syntax**: 
  ```java 
    // Declare Multidimensioanl Array
    dataType[][] arrayRefVar; (or)  
    dataType [][]arrayRefVar; (or)  
    dataType arrayRefVar[][]; (or)  
    dataType []arrayRefVar[];   
    // instantiate Multidimensional Array 
    int[][] arr = new int[3][3]; // 3 row and 3 column
  ````
  - **Examples**
  ```java 
  arr[0][0]=1;  
  arr[0][1]=2;  
  arr[0][2]=3;  
  arr[1][0]=4;  
  arr[1][1]=5;  
  arr[1][2]=6;  
  arr[2][0]=7;  
  arr[2][1]=8;  
  arr[2][2]=9; 
  ````
  ```java 
    class Testarray3{  
  public static void main(String args[]){  
  //declaring and initializing 2D array  
  int arr[][]={{1,2,3},{2,4,5},{4,4,5}};  
  //printing 2D array  
  for(int i=0;i<3;i++){  
   for(int j=0;j<3;j++){  
     System.out.print(arr[i][j]+" ");  
   }  
   System.out.println();  
  }  
  }}  
  ````
  - Jagged Array
  ```java
  class TestJaggedArray{  
    public static void main(String[] args){  
        //declaring a 2D array with odd columns  
        int arr[][] = new int[3][];  
        arr[0] = new int[3];  
        arr[1] = new int[4];  
        arr[2] = new int[2];  
        //initializing a jagged array  
        int count = 0;  
        for (int i=0; i<arr.length; i++)  
            for(int j=0; j<arr[i].length; j++)  
                arr[i][j] = count++;  
   
        //printing the data of a jagged array   
        for (int i=0; i<arr.length; i++){  
            for (int j=0; j<arr[i].length; j++){  
                System.out.print(arr[i][j]+" ");  
            }  
            System.out.println();//new line  
        }  
    }  
  }  
  ````
  - Copy Java Array 
    - can copy an array to another by the `arraycopy()` method of the System class.
    - Syntax:
    ```java
    public static void arraycopy(  
    Object src, int srcPos,Object dest, int destPos, int length  
    )  
    ````
    - Example:
    ```java 
    class TestArrayCopyDemo {  
    public static void main(String[] args) {  
        //declaring a source array  
        char[] copyFrom = { 'd', 'e', 'c', 'a', 'f', 'f', 'e',  
                'i', 'n', 'a', 't', 'e', 'd' };  
        //declaring a destination array  
        char[] copyTo = new char[7];  
        //copying array using System.arraycopy() method  
        System.arraycopy(copyFrom, 2, copyTo, 0, 7);  
        //printing the destination array  
        System.out.println(String.valueOf(copyTo));  
    }}  
    ````
    - Clonning an Array 
      - clone of single-dimensional array creates the deep copy (copy the actual value) of the Java array. 
      - clone of a multidimensional array, creates a shallow copy (copies the reference)
    ````java 
    class Testarray1{  
    public static void main(String args[]){  
    int arr[]={33,3,4,5};  
    System.out.println("Printing original array:");  
    for(int i:arr)  
    System.out.println(i);  
    System.out.println("Printing clone of the array:");  
    int carr[]=arr.clone();  
    for(int i:carr)  
    System.out.println(i);  
    System.out.println("Are both equal?");  
    System.out.println(arr==carr);  
    }}  
    ````    
---
