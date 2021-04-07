# Java Break Statement 
- used to come out of the loop instantly and loop gets terminated for rest of the iterations. 
- used mostly with if statement, inside the loop, when loops gets terminated for a particular condition.
- when used inside a nested loop, only inner loop gets terminated.
- generally all cases in switch are followed by a break statement to prevent unwanted cases being printed
- Syntax `**break;**`

<h3 align="center">
  <img src="https://www.includehelp.com/java/Images/break-in-java.jpg" alt="break image" height="475">
</h3>

---
### Examples of Break statement 
- Break in while loop
```java 
public class BreakExample1 {
   public static void main(String args[]){
      int num =0;
      while(num<=100)
      {
          System.out.println("Value of variable is: "+num);
          if (num==2)
          {
             break;
          }
          num++;
      }
      System.out.println("Out of while-loop");
  }
}
/*
Output: 
Value of variable is: 0
Value of variable is: 1
Value of variable is: 2
Out of while-loop
*/
````
- Break in for loop
```java 
public class BreakExample2 {

   public static void main(String args[]){
	int var;
	for (var =100; var>=10; var --)
	{
	    System.out.println("var: "+var);
	    if (var==99)
	    {
	         break;
	    }
	 }
	 System.out.println("Out of for-loop");
   }
}
/* 
Output
var: 100
var: 99
Out of for-loop
*/
```
- Break in switch case 
```java 
public class BreakExample3 {

   public static void main(String args[]){
	int num=2;
	      
	switch (num)
	{
	    case 1:
	       System.out.println("Case 1 ");
	       break;
	    case 2:
	       System.out.println("Case 2 ");
	       break;
	    case 3:
	       System.out.println("Case 3 ");
	       break;
	    default:
	       System.out.println("Default ");
	}
   }
}
/*
Output:
Case 2
*/
```
- Break statement in Inner Loop
```java 
public class BreakExample2 {  
public static void main(String[] args) {  
            //outer loop   
            for(int i=1;i<=3;i++){    
                    //inner loop  
                    for(int j=1;j<=3;j++){    
                        if(i==2&&j==2){    
                            //using break statement inside the inner loop  
                            break;    
                        }    
                        System.out.println(i+" "+j);    
                    }    
            }    
}  
}  
/*
Output: 
1 1
1 2
1 3
2 1
3 1
3 2
3 3
*/
```
- Break Statement with Labeled For Loop
```java 
public class BreakExample3 {  
public static void main(String[] args) {  
            aa:  
            for(int i=1;i<=3;i++){    
                    bb:  
                    for(int j=1;j<=3;j++){    
                        if(i==2&&j==2){    
                            //using break statement with label  
                            break aa;    
                        }    
                        System.out.println(i+" "+j);    
                    }    
            }    
}  
}  
/*
Output:
1 1
1 2
1 3
2 1
*/
```
- Break Statement in do-while loop
```java 
public class BreakDoWhileExample {  
public static void main(String[] args) {  
    //declaring variable  
    int i=1;  
    //do-while loop  
    do{  
        if(i==5){  
           //using break statement  
           i++;  
           break;//it will break the loop  
        }  
        System.out.println(i);  
        i++;  
    }while(i<=10);  
}  
}  
/*
Output: 
1
2
3
4
*/
```
---
