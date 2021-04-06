# Switch Case statement
- used when there are number of options and need to perform a different task. 
- Syntax 
```java 
switch (variable or an integer expression){
  case constant:
  // Java code ; 
  case constant
  // Java code ;
  default:
  // Java code ;
}
```
- Example 
```java 
public class SwitchCaseExample1 {

   public static void main(String args[]){
     int num=2;
     switch(num+2)
     {
        case 1:
	  System.out.println("Case1: Value is: "+num);
	case 2:
	  System.out.println("Case2: Value is: "+num);
	case 3:
	  System.out.println("Case3: Value is: "+num);
        default:
	  System.out.println("Default: Value is: "+num);
      }
   }
}
// Output Default: Value is: 2
```
<h3 align="center">
  <img src="https://www.alphacodingskills.com/java/img/java-switch.png" alt="switch case" height="475px">
</h3>

---

### default and break statements
- default case and break statements are optional  
   - **Default Case**: 
   	- executed when there is no match between switch expression and test cases. 
   - **Break Statement**:
   	- used to get out of the Switch statement after a match is found. 
 ```java 
 public class MyClass {
  public static void main(String[] args) {
    int i = 10;
    switch(i){
      case 1: 
         System.out.println("Red");
         break; 
      case 2: 
         System.out.println("Blue");
         break;
      case 3: 
         System.out.println("Green");
         break;
      default:
         System.out.println("There is no match in the switch statement.");
    }  
  }
}
// Output: Case 2 
 ```
 ---
 
 ### Few Points about Switch Case 
- There can be one or N number of case values for a switch expression.
- The case value must be of switch expression type only. The case value must be literal or constant. It doesn't allow variables.
- The case values must be unique. In case of duplicate value, it renders compile-time error.
- The Java switch expression must be of byte, short, int, long (with its Wrapper type), enums and string.
- Each case statement can have a break statement which is optional. When control reaches to the break statement, it jumps the control after the switch expression. If a break statement is not found, it executes the next case.
- The case value can have a default label which is optional.

---

### Examples of Different Switch cases 
- Switch Expression type 
```java 
public class SwitchExample {  
public static void main(String[] args) {  
    //Declaring a variable for switch expression  
    int number=20;  
    //Switch expression  
    switch(number){  
    //Case statements  
    case 10: System.out.println("10");  
    break;  
    case 20: System.out.println("20");  
    break;  
    case 30: System.out.println("30");  
    break;  
    //Default case statement  
    default:System.out.println("Not in 10, 20 or 30");  
    }  
}  
}  
```
- Switch Statement fall through : executes all statements after the first match if a break statement is not present. 
```java 
//Java Switch Example where we are omitting the  
//break statement  
public class SwitchExample2 {  
public static void main(String[] args) {  
    int number=20;  
    //switch expression with int value  
    switch(number){  
    //switch cases without break statements  
    case 10: System.out.println("10");  
    case 20: System.out.println("20");  
    case 30: System.out.println("30");  
    default:System.out.println("Not in 10, 20 or 30");  
    }  
}  
}  
```
- Switch Statement with String 
```java 
public class SwitchStringExample {    
public static void main(String[] args) {    
    //Declaring String variable  
    String levelString="Expert";  
    int level=0;  
    //Using String in Switch expression  
    switch(levelString){    
    //Using String Literal in Switch case  
    case "Beginner": level=1;  
    break;    
    case "Intermediate": level=2;  
    break;    
    case "Expert": level=3;  
    break;    
    default: level=0;  
    break;  
    }    
    System.out.println("Your Level is: "+level);  
}    
}   
```
- Nested Switch Statement 
```java
// Nested Switch Statement 
public class NestedSwitchExample {    
    public static void main(String args[])  
      {  
      //C - CSE, E - ECE, M - Mechanical  
        char branch = 'C';                 
        int collegeYear = 4;  
        switch( collegeYear )  
        {  
            case 1:  
                System.out.println("English, Maths, Science");  
                break;  
            case 2:  
                switch( branch )   
                {  
                    case 'C':  
                        System.out.println("Operating System, Java, Data Structure");  
                        break;  
                    case 'E':  
                        System.out.println("Micro processors, Logic switching theory");  
                        break;  
                    case 'M':  
                        System.out.println("Drawing, Manufacturing Machines");  
                        break;  
                }  
                break;  
            case 3:  
                switch( branch )   
                {  
                    case 'C':  
                        System.out.println("Computer Organization, MultiMedia");  
                        break;  
                    case 'E':  
                        System.out.println("Fundamentals of Logic Design, Microelectronics");  
                        break;  
                    case 'M':  
                        System.out.println("Internal Combustion Engines, Mechanical Vibration");  
                        break;  
                }  
                break;  
            case 4:  
                switch( branch )   
                {  
                    case 'C':  
                        System.out.println("Data Communication and Networks, MultiMedia");  
                        break;  
                    case 'E':  
                        System.out.println("Embedded System, Image Processing");  
                        break;  
                    case 'M':  
                        System.out.println("Production Technology, Thermal Engineering");  
                        break;  
                }  
                break;  
        }  
    }  
}  
```
- Enum in Switch Statement 
```java 
public class JavaSwitchEnumExample {      
       public enum Day {  Sun, Mon, Tue, Wed, Thu, Fri, Sat  }    
       public static void main(String args[])    
       {    
         Day[] DayNow = Day.values();    
           for (Day Now : DayNow)    
           {    
                switch (Now)    
                {    
                    case Sun:    
                        System.out.println("Sunday");    
                        break;    
                    case Mon:    
                        System.out.println("Monday");    
                        break;    
                    case Tue:    
                        System.out.println("Tuesday");    
                        break;         
                    case Wed:    
                        System.out.println("Wednesday");    
                        break;    
                    case Thu:    
                        System.out.println("Thursday");    
                        break;    
                    case Fri:    
                        System.out.println("Friday");    
                        break;    
                    case Sat:    
                        System.out.println("Saturday");    
                        break;    
                }    
            }    
        }    
}    
```
- Wrapper in Switch Statement 
```java 
public class WrapperInSwitchCaseExample {       
       public static void main(String args[])  
       {         
            Integer age = 18;        
            switch (age)  
            {  
                case (16):            
                    System.out.println("You are under 18.");  
                    break;  
                case (18):                
                    System.out.println("You are eligible for vote.");  
                    break;  
                case (65):                
                    System.out.println("You are senior citizen.");  
                    break;  
                default:  
                    System.out.println("Please give the valid age.");  
                    break;  
            }             
        }  
}  
```
----


