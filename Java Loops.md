# Loops in Java 
- used to execute a set of instructions/fucntions repeatedly when some conditions become true
- three types of loops:
  - for loop 
  - while loop
  - do-while loop
 
 <h3 align="center">
    <img src="https://javatpoint.com/images/java-loops.png" alt="loops in Java" height="385px">
</h3>

---
### Comparison of loops in Java

| Comparison                 | for loop                                                                                                                                       | while loop                                                                                                                               | do while loop                                                                                                                                                             |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|  |
| Introduction               | The Java for loop is a control flow statement that iterates a part of the [programs](https://www.javatpoint.com/java-programs) multiple times. | The Java while loop is a control flow statement that executes a part of the programs repeatedly on the basis of given boolean condition. | The Java do while loop is a control flow statement that executes a part of the programs at least once and the further execution depends upon the given boolean condition. |
| When to use                | If the number of iteration is fixed, it is recommended to use for loop.                                                                        | If the number of iteration is not fixed, it is recommended to use while loop.                                                            | If the number of iteration is not fixed and you must have to execute the loop at least once, it is recommended to use the do-while loop.                                  |
| Syntax                     | for(init;condition;incr/decr){//code to executed }                                                                                  |  while(condition){//code to be executed}                                                                                             | do{//code to be executed}while(condition);                                                                                                                          |
| Example                    | //for loop  `for(int i=1;i<=10;i++){ System.out.println(i);}`                                                                              | //while loop  `int i=1;while(i<=10){System.out.println(i);i++; }`                                                             | //do-while loop  `int i=1;do{System.out.println(i);i++; }while(i<=10);`                                                                                         |
| Syntax for infinitive loop | `for(;;){//code to be executed}`                                                                                                        | `while(true){//code to be executed}`    |                                                                                            `do{//code to be executed}while(true);`                                                                                                           | 
