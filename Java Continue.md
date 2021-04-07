# Continue Statement in Java
- most commonly used inside loops to jump to next iteration of loop immediately.
- continues the current flow of the program and skips the remaining code at specific condition.
- Syntax `continue;`
```java 
public class ContinueExample {

   public static void main(String args[]){
	for (int j=0; j<=6; j++)
	{
           if (j==4)
           {
	      continue;
	   }

           System.out.print(j+" ");
	}
   }
}
/* 
Output 0 1 2 3 5 6
*/
````
<h3 align="center">
  <img src="https://1.bp.blogspot.com/-wT_od70gfdM/WzsfRvI8fvI/AAAAAAAAH_Y/8iGNAOo97xsQP_mHeWdmkbroAgdid4FjwCLcBGAs/s1600/Continue_Statement_C.jpg" alt="continue" height="375px">
</h3>

---
### Examples of continue in Loops
- continue in While Loop
```java 
public class ContinueExample2 {

   public static void main(String args[]){
	int counter=10;
	while (counter >=0)
	{
           if (counter==7)
           {
	       counter--;
	       continue;
           }
           System.out.print(counter+" ");
           counter--;
	}
   }
}
/*
Output
10 9 8 6 5 4 3 2 1 0
*/
```
- continue with do-While Loop
```java 
public class ContinueExample3 {

   public static void main(String args[]){
	int j=0;
        do
	{
	   if (j==7)
	   {
		 j++;
		 continue;
	   }
	   System.out.print(j+ " ");
	   j++;
       }while(j<10);
		  
   }
}
/*
Output
0 1 2 3 4 5 6 8 9 
*/
```
