# Java OOPs Concepts

- Main aim of object-oriented programming is to implement real-world entities
- Object means a real-world entity such as a pen, chair..
- Object-Oriented Programming is a methodology or paradigm to design a program using classes and objects


***OOPS CONCEPTS***
- Object
- Class
- Inheritance
- Polymorphism
- Abstraction
- Encapsulation
<img src="https://static.javatpoint.com/images/java-oops.png" alt="Decision Making in Go"  width="100%" height="500px%" align="left" />

**OBJECT**
- Any entity that has state and behavior
- can be defined as an instance of a class
- contains an address and takes up some space in memory
- it  can communicate without knowing the details of each other's data or code

**CLASS**
- Collection of objects
- it can be defined as a blueprint from which you can create an individual object
- doesn't consume any space

---

**INHERITANCE**
- When one object acquires all the properties and behaviors of a parent object, it is known as inheritance
- provides code reusability
-
      Super Class: The class whose features are inherited is known as superclass(or a base class or a parent class)

      Sub Class: The class that inherits the other class is known as subclass(or a derived class, extended class, or child class)
- The keyword used for inheritance is extends.
Syntax:
```java
// Java program to illustrate the
// concept of inheritance

// base class
class Bicycle {
	// the Bicycle class has two fields
	public int gear;
	public int speed;

	// the Bicycle class has one constructor
	public Bicycle(int gear, int speed)
	{
		this.gear = gear;
		this.speed = speed;
	}

	// the Bicycle class has three methods
	public void applyBrake(int decrement)
	{
		speed -= decrement;
	}

	public void speedUp(int increment)
	{
		speed += increment;
	}

	// toString() method to print info of Bicycle
	public String toString()
	{
		return ("No of gears are " + gear + "\n"
				+ "speed of bicycle is " + speed);
	}
}

// derived class
class MountainBike extends Bicycle {

	// the MountainBike subclass adds one more field
	public int seatHeight;

	// the MountainBike subclass has one constructor
	public MountainBike(int gear, int speed,
						int startHeight)
	{
		// invoking base-class(Bicycle) constructor
		super(gear, speed);
		seatHeight = startHeight;
	}

	// the MountainBike subclass adds one more method
	public void setHeight(int newValue)
	{
		seatHeight = newValue;
	}

	// overriding toString() method
	// of Bicycle to print more info
	@Override public String toString()
	{
		return (super.toString() + "\nseat height is "
				+ seatHeight);
	}
}

// driver class
public class Test {
	public static void main(String args[])
	{

		MountainBike mb = new MountainBike(3, 100, 25);
		System.out.println(mb.toString());
	}
}

/*
 Output
	No of gears are 3
	speed of bicycle is 100
	seat height is 25
*/
````
---

**POLYMORPHISM**
- If one task is performed in different ways, it is known as polymorphism
- Polymorphism in Java are mainly of 2 types:

      -  Overloading in Java
      -  Overriding in Java
```java
// Java program to demonstrate Polymorphism

// This class will contain
// 3 methods with same name,
// yet the program will
// compile & run successfully
public class Sum {

	// Overloaded sum().
	// This sum takes two int parameters
	public int sum(int x, int y)
	{
		return (x + y);
	}

	// Overloaded sum().
	// This sum takes three int parameters
	public int sum(int x, int y, int z)
	{
		return (x + y + z);
	}

	// Overloaded sum().
	// This sum takes two double parameters
	public double sum(double x, double y)
	{
		return (x + y);
	}

	// Driver code
	public static void main(String args[])
	{
		Sum s = new Sum();
		System.out.println(s.sum(10, 20));
		System.out.println(s.sum(10, 20, 30));
		System.out.println(s.sum(10.5, 20.5));
	}
}
/*
Output:
	30
	60
	31.0
*/
```
---

**ABSTRACTION**

- Hiding internal details and showing functionality
- only the essential details are displayed to the user, the trivial or the non-essentials units are not displayed to the user
- abstraction is achieved by interfaces and abstract classes

```java
// Java program to illustrate the
// concept of Abstraction
abstract class Shape {
	String color;

	// these are abstract methods
	abstract double area();
	public abstract String toString();

	// abstract class can have constructor
	public Shape(String color)
	{
		System.out.println("Shape constructor called");
		this.color = color;
	}

	// this is a concrete method
	public String getColor() { return color; }
}
class Circle extends Shape {
	double radius;

	public Circle(String color, double radius)
	{

		// calling Shape constructor
		super(color);
		System.out.println("Circle constructor called");
		this.radius = radius;
	}

	@Override double area()
	{
		return Math.PI * Math.pow(radius, 2);
	}

	@Override public String toString()
	{
		return "Circle color is " + super.getColor()
			+ "and area is : " + area();
	}
}
class Rectangle extends Shape {

	double length;
	double width;

	public Rectangle(String color, double length,
					double width)
	{
		// calling Shape constructor
		super(color);
		System.out.println("Rectangle constructor called");
		this.length = length;
		this.width = width;
	}

	@Override double area() { return length * width; }

	@Override public String toString()
	{
		return "Rectangle color is " + super.getColor()
			+ "and area is : " + area();
	}
}
public class Test {
	public static void main(String[] args)
	{
		Shape s1 = new Circle("Red", 2.2);
		Shape s2 = new Rectangle("Yellow", 2, 4);

		System.out.println(s1.toString());
		System.out.println(s2.toString());
	}
}

/*
Output
	Shape constructor called
	Circle constructor called
	Shape constructor called
	Rectangle constructor called
	Circle color is Redand area is : 15.205308443374602
	Rectangle color is Yellowand area is : 8.0
*/
```
---

**ENCAPSULATION**

- wrapping up of data under a single unit
- Encapsulation can be achieved by Declaring all the variables in the class as private and writing public methods in the class to set and get the values of variables
```java
// Java program to demonstrate encapsulation
class Encapsulate {
	// private variables declared
	// these can only be accessed by
	// public methods of class
	private String geekName;
	private int geekRoll;
	private int geekAge;

	// get method for age to access
	// private variable geekAge
	public int getAge() { return geekAge; }

	// get method for name to access
	// private variable geekName
	public String getName() { return geekName; }

	// get method for roll to access
	// private variable geekRoll
	public int getRoll() { return geekRoll; }

	// set method for age to access
	// private variable geekage
	public void setAge(int newAge) { geekAge = newAge; }

	// set method for name to access
	// private variable geekName
	public void setName(String newName)
	{
		geekName = newName;
	}

	// set method for roll to access
	// private variable geekRoll
	public void setRoll(int newRoll) { geekRoll = newRoll; }
}

public class TestEncapsulation {
	public static void main(String[] args)
	{
		Encapsulate obj = new Encapsulate();

		// setting values of the variables
		obj.setName("Harsh");
		obj.setAge(19);
		obj.setRoll(51);

		// Displaying values of the variables
		System.out.println("Geek's name: " + obj.getName());
		System.out.println("Geek's age: " + obj.getAge());
		System.out.println("Geek's roll: " + obj.getRoll());

		// Direct access of geekRoll is not possible
		// due to encapsulation
		// System.out.println("Geek's roll: " +
		// obj.geekName);
	}
}
/*
- Output
	Geek's name: Harsh
	Geek's age: 19
	Geek's roll: 51

*/
````
---


