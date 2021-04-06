# Java Strings
- Strings are used for storing text 
- String variable contains a collection of characters surrounded by double quotes:
```java 
String greeting = "Hello";
````
---
### String length
- string an object, which contain methods can perform certain operations on string. 
```java 
String txt = "ABCSDESFGR"
System.out.println("The length od the text string is:"+txt.length());
````
---
### More String Methods 
- many string methods available ``toUpperCase()` and `toLowerCase()`
```java 
String txt = "Hello World";
System.out.println(txt.toUpperCase());   // Outputs "HELLO WORLD"
System.out.println(txt.toLowerCase());   // Outputs "hello world"
````
---
### Finding a Character in a String 
- `indexOf()` method returns the index (the position) of the first occurrence of a specified text in a string 
```java 
String txt = "Please locate where 'locate' occurs!";
System.out.println(txt.indexOf("locate")); // Output 7
````
---
### String Concatenation 
- `+` operator can be used between strings to combine.
- aslo called **concatenation**. 
```java 
String firstName = "John";
String lastName = "Doe";
System.out.println(firstName + " " + lastName);
```
---
### Special Characters
- use to create a special format to the string 
```java 
String txt = "We are the so-called "Vikings" from the north.";
````
- `\f` : for inserting a formfeed.
- `\'` : for inserting a quote character.
- `\"` : for inserting a double quote character.
- `\\` : for inserting a backslash character.
- `\t` : for inserting a tab.
- `\b` : for inserting a backspace.
- `\n` : for inserting a newline.
- `\r` : for inserting a carriage return.
