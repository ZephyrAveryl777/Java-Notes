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

