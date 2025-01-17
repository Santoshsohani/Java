
---

For a Java program to execute the following structure should be followed

```java
public class Main{
	public static void main(Strinh[] args){
		System.out.println("Hello World");
	}
}
```

- There should be a *class* and inside the class a *main* method should be present.

# Variables

A variable is a location in memory which holds some data. To indicate this location a identifier is provided. Each variable should be given a unique name.

```java
int speedLimit = 80;
```

Here 
- int : Data Type
- speedLimit : Identifier (Variable Name)
- 80 : Value assigned to speedLimit

# Literals 

A Literal is a fixed value, which can be used directly in the program

There are 5 types of Literals : 
1. Integer Literals
	1. Binary -- Start with 0b
	2. Octal --Start with 0
	3. Hexadecimal -- Start with 0x
	4. Decimal 
2. Floating Point Literals
	1. Float 
	2. Double
3. Character Literals -- Initialized inside of  single quotes
4. String Literals -- Initialized inside of double quotes
5. Boolean Literals 

# Data Types

- Data Types are used to specify what is the type of value which can be stored in the variable.
- Java is type language which means variables should be declared first before using it.

There are 8 Pre-defined data types present in Java, Also called as primitive types

 1. Boolean : true or false -- Default false
 2. byte 
 3. short 
 4. int 
 5. long
 6. char
 7. double
 8. float

## Default Values of Primitive Data Types in Java and its range

| Data Type | Default Value             | Description                               |
| --------- | ------------------------- | ----------------------------------------- |
| `byte`    | 0                         | 8-bit integer value.                      |
| `short`   | 0                         | 16-bit integer value.                     |
| `int`     | 0                         | 32-bit integer value.                     |
| `long`    | 0L                        | 64-bit integer value.                     |
| `float`   | 0.0f                      | 32-bit floating-point value.              |
| `double`  | 0.0d                      | 64-bit floating-point value.              |
| `char`    | '\u0000' (null character) | Unicode character with all bits set to 0. |
| `boolean` | false                     | Boolean value (true/false).               |

| Data Type | Size (Bits) | Range                                                                   | Default Value |
| --------- | ----------- | ----------------------------------------------------------------------- | ------------- |
| `byte`    | 8           | -128 to 127                                                             | 0             |
| `short`   | 16          | -32,768 to 32,767                                                       | 0             |
| `int`     | 32          | -2,147,483,648 to 2,147,483,647                                         | 0             |
| `long`    | 64          | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807                 | 0L            |
| `float`   | 32          | Approximately ±3.40282347E+38 (7 significant decimal digits)            | 0.0f          |
| `double`  | 64          | Approximately ±1.79769313486231570E+308 (15 significant decimal digits) | 0.0d          |

# Operators (AALUR-B)

1. Arithmetic Operator :  
	1. +
	2. -
	3. *
	4. /
	5. %

2. Assignment Operator : 
	1. = 
	2. += 
	3. -= 
	4. * = 
	5. /=
	6. %=

3.  Logical Operator
	1.  &&
	2. ||
	3. !

4.  Unary Operator
	1. ++
	2. --

5. Relational Operator
	1.  ==
	2. != 
	3. >
	4. <
	5. >= 
	6. <= 

6. Bit-wise Operator
	1. ~
	2. <<
	3. >>
	4. >>>
	5. &
	6. ^

# Conditional Statements

1.  If-else Block

```Java
if(age >= 18){
	System.out.println('Eligible to Vote');
}else{
	System.out.println('Not Eligible to Vote');
}
```

2. Ternary Operator

- Syntax : 
```
	condition ? expression1 : expression2
```

Here if the condition is true *expression1* is executed, else *expression2* is evaluated 

```java
class Main {
	public static void main(String[] args){
		int marks = 38;
		String result = (marks >= 35) ? "Pass" : "Fail"
	}
}
```

Ternary Operator can be used in some conditions, It makes the code more readable.


# Loops

In Programming when a certain block of code is executed multiple number of times. Then we use Loops.

There are mainly 3 types of Loops
1. For Loop
2. While Loop
3. Do-While Loop

1. For Loop

```
for(intialExpression; testExpression; updateExpression){
	
}
```

```Java
int sum = 0
for(int i = 0; i < 10; i++){
	sum += i
}
```

The Java *for-each* loop is an alternative way of looping through an array or collections

```
for (datatype item: array/collection){
	...
}
```

```java
class Main{
	public static void main(String[] args){
		int[] array = {10,20,30,40,50}
	}
	
	for(int number : array){
		System.out.println(number);
	}
}
```


2. While loop

This is another type of loop which gets executed until the condition is false

```java
while(true){
	System.out.println("Hello");
}
```

3. Do While loop

This is another loop which gets executed at least once. After the first iteration the condition is checked

```java
do{
	System.out.println("Hello");
}while(true)
```


# Break and Continue

The Break and Continue Statements can only be used in *loops* 

- The *Break* statement is used when a loop is to be terminated when met with a certain condition. It Terminates the entire loop and shifts the control of execution to the next statement after the loop

```java
for(int i = 0; i < 10; i++){
	if(i == 5){
		break;
	}
}
System.out.println('Loop used Break Statement at i = 5')
```

- The *Continue* statement is used when a certain iteration is to be skipped when met with a certain condition. It Does not terminates the entire loop

```java
for(int i = 0; i < 10; i++){
	if(i == 5){
		continue;
	}
}
System.out.println('Loop used Continue Statement at i = 5')
```


# Arrays

Array is an Linear Data structure which is used store data of similar type. 
For example a user wants to store names of 100 users. he/she can create an array of strings and store names in it.

Syntax : 

```
datatype[] arrayName = new datatype[size];
datatype[] arrayName = {_,_,_} Default Values
```

Arrays works on the principle of indexing, which means its elements can be accessed using index. The first index starts with 0

## Copy Arrays

1. Using Assignment Operator

```java
public class Copy{
	public static void main(String[] args){
		int[] arrayOne = {1,2,3,4,5,6};
		int[] arrayTwo = arrayOne;
	}
}
```

- This will copy the contents of array-one into array-two. But there is small issue here, If we change the contents of one array the other array will also change. This is because of *shallow copy* . Both the array points at same memory location

2. Using Loop

```java
public class Copy {
	public static void main(String[] args){
		int[] arr1 = {10,20,30,40,50,60};
		int[] arr2 = new int[6];

		for(int i = 0; i < arr1.length; i++){
			arr2[i] = arr1[i]
		}
	}
}
```

Here we are creating two arrays and copying the contents of one array into the another array. using for loop, Here changes made to one array will not affect another array. As both the arrays are pointing to two different memory locations. This concept is called as *deep copy*

3. Using the arraycopy() method

The System class consists of method called as arraycopy() which is used to copy array from a specific position.

It Takes 5 Parameters :
1. source 
2. Source Index
3. Target 
4. Target Index
5. Length

```java
class Main {
    public static void main(String[] args) {
        int[] n1 = {2, 3, 12, 4, 12, -2};
      
        int[] n3 = new int[5];
        int[] n2 = new int[n1.length];
      
        System.arraycopy(n1, 0, n2, 0, n1.length);  
    }
}
```


# OOPS

Java is an Object Oriented Programming Language. The main aim of OOP is to divide a complex problem into smaller objects.

A object is a real world entity which has states and behavior.  Consider the example of bicycle which has multiple states and behaviors.

 States : Static, Moving, First Gear
 Behavior : Acceleration, Break

## Class

Class is an important feature in Object Oriented Programming. Class is an Blueprint from which an object can be created.

Consider a blueprint of an house, where the floor plannings, doors, windows and other things will be sketched out. Based upon this house is built which is an object. 

Using a single blueprint multiple house can be created, which means multiple objects can be created from a single class

```java
class className {
	// Fields
	// Methods
}
```

Here, Fields are states and Methods are behaviors. 

```Java
class Bicycle {
	int gear = 5;
	public void breaking() {
		System.out.println('Working of Break);
	}
}
```


## Object

Object is an instance of a class.  For example Bicycle is the class and the object created from Bicycle are instance of it.

```java
className objectName = new className();
```

The above code snippet is the syntax to create a object in Java. we use *new* keyword and *constructor* method to create an object.

```java
class Lamp {
  boolean isOn;

  void turnOn() {
    isOn = true;
    System.out.println("Light on? " + isOn);
  }

  void turnOff() {
    isOn = false;
    System.out.println("Light on? " + isOn);
  }
}

public class Main {
  public static void main(String[] args) {

    Lamp led = new Lamp();
    Lamp halogen = new Lamp();

    led.turnOn();
    halogen.turnOff();
  }
}
```

## Methods

Methods in Java are block of code which performs a particular tasks.

In Java there are two types of methods 
1. User Defined Custom Methods
2. Built-in Methods

```java
returnType methodName {
	// Method Body
}
```

The above code snippet is the syntax to create a method, But where as a complex syntax would be something like this.

```java
modifier static returnType methodName {
	// Method Body
}
```

- Advantages of using Methods
	- Code Re-Usability
	- Dynamic use-age of single method

## Method Overloading

Method overloading is concept where two or more methods can have same name but differ in parameters : 
1. Number of Parameters
2. Type of Parameters

```java
class Caluclator{
	public int sum(int a, int b){
		return a+b;
	}

	public int sum(int a, int b, int c){
		return a+b+c;
	}
}
```

Here as you can see the class Calculator has two methods with the same name *sum*, But differ in number of parameters. Here there is *Method Overloading*

## Constructor

A Constructor is a method which is called when an object is created. The name of the constructor should be same as the class name. The Constructor does not have any return type.

There are 3 Types of constructors : 
1. No-Arg Constructor
2. Parameterized Constructor
3. Default Constructor

| Feature                 | No-Arg Constructor                                             | Parameterized Constructor                                                         | Default Constructor                                                                               |
| ----------------------- | -------------------------------------------------------------- | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- |
| **Definition**          | A constructor that does not take any arguments.                | A constructor that takes parameters to initialize an object with specific values. | A constructor provided by the compiler if no constructor is explicitly defined by the programmer. |
| **Arguments**           | No arguments                                                   | Requires arguments to be passed                                                   | No arguments                                                                                      |
| **Who defines it?**     | Programmer                                                     | Programmer                                                                        | Automatically defined by the compiler if no other constructor is present.                         |
| **Purpose**             | To initialize the object with default or preset values.        | To initialize the object with user-provided values.                               | Provides a basic object construction with default values.                                         |
| **Usage Scenario**      | Used when no initial values are needed during object creation. | Used when object creation requires specific values to be set.                     | Used when no constructor is explicitly defined and the object needs basic initialization.         |
| **Explicit Definition** | Must be explicitly defined by the programmer.                  | Must be explicitly defined by the programmer.                                     | Implicitly created by the compiler.                                                               |



### Summary:
- No-Arg Constructor is explicitly created with no parameters.
- Parameterized Constructor is created to accept specific values.
- Default Constructor is provided by the compiler when no other constructor is written.
- Constructors can be overloaded but cannot be overridden

## Static Keyword

Members of a particular class can be declared as *static* which means These members are only associated with the class and not associated with the instance of the class. 
The class Members can be accessed using class name and if required within the same class, Then it can be accessed directly.

### Static Methods

```java
class Calculator {
	public static void greet(){
		System.out.println("Helllo World!");
	}
}

public static void main(String[] args){
	Calculator.greet();
}
```

- Here the method *greet* is accessed using the class name itself. without creating any instance of it.

### Static Variables

Static Variables on the other hand are the variables which are associated with the class. We Know that non-static variables are independent for their own instance, But Static variables are same everywhere.

```java
class Calculator {
	static float pi = 3.142f;

	public static void greet(){
		System.out.println("Helllo World!");
	}
}

public static void main(String[] args){
	Calculator.greet();
}
```


### Static Blocks

Static Blocks are used to declare static variables 

```java
static {
	// Variables should be declared here
}
```

The static block is executed only when an class is loaded in the memory. This condition happens when an object of that class is requested or an static member is requested.

- Multiple static blocks can be used in the same class.
- Static blocks can also be nested
  
## String

Strings are the data types which are used to store sequence of characters. In Java string is not a primitive data type, But a class and all the strings created are Object of the *String* class.

```java
String name = "sansiro";
String name2 = new String("sansiro");
```

- Operations on Strings
```java
class StringOperation{
	public static void main(String[] args){
		String str1 = "sansiro";
		
		int length = str1.length(); // Length of String
		String str2 = str1.concat("Milan") // Concat
		boolean compare = str1.equals(str2);
	}
}
```

By Default, Strings are immutable in Java, which means once the string is declared its value cannot be manipulated, The *concat* operation does not update the string instead create a new string.

This is because Java uses *string pool* to store all the strings. If the similar string is again declared it will just assign its reference to the newly created string.

### Difference between the declarations of strings

We know that, Strings can be declared in two ways.

```java
String name = "sansiro";
String name2 = new String("sansiro");
```

In the first scenario 

```java
String name = "sansiro";
```

The JVM  first checks whether the string *sansiro* is present in the string pool or not. 
- If Present : Assigns the reference to the newly created string
- Not Present : Creates a new String inside the string pool

Second Scenario

```java
String name2 = new String("sansiro");
```

Now regardless whether the string is present in string pool or not, a new string is created in the string pool.

### Escape Character in Java Strings

The escape character is used to escape some of the characters present inside a string.

Suppose we need to include double quotes inside a string.

```java
// include double quote 
String example = "This is the "String" class";
```

Since strings are represented by **double quotes**, the compiler will treat `"This is the "` as the string. Hence, the above code will cause an error.

To solve this issue, we use the escape character `\` in Java. For example,

```java
// use the escape character
String example = "This is the \"String\" class.";
```

Now escape characters tell the compiler to escape **double quotes** and read the whole text.

## Access Modifiers

Access modifiers are used to limit the access of class, variables, methods, constructors, setters and interface.

There are 4 types of access modifiers 
1. Default
2. Private
3. Protected
4. Public

### Default


When a certain class is provided with the access modifier as default, Then it can be accessed anywhere within the package, Then all its variables, methods, constructors can be accessed.

```java
package defaultPackage;
class Logger {
    void message(){
        System.out.println("This is a message");
    }
}
```


### Private 

Firstly we cannot declare classed and interfaces private in Java. 
When methods and variables are declared as private then it can be only accessed within the class. Not anywhere outside the class.

```java
class Data {
    // private variable
    private String name;
}

public class Main {
    public static void main(String[] main){

        // create an object of Data
        Data d = new Data();

        // access private variable and field from another class
        d.name = "Programiz";
    }
}
```

The above code will throw an error

### Public 

When variables, classes, methods and so on are declared are public then it can be accessed from anywhere. The public access modifier has no restrictions.

```java
public class Animal {
    public int legCount;
    public void display() {
        System.out.println("I am an animal.");
        System.out.println("I have " + legCount + " legs.");
    }
}

// Main.java
public class Main {
    public static void main( String[] args ) {
        Animal animal = new Animal();
        animal.legCount = 4;
        animal.display();
    }
}
```


## This Keyword

This keyword refers to the current object inside of a method or a constructor.

This keyword is mainly used in various situations : 
1. Ambiguity of the variables names 
2. Getters and Setters
3. Using this in constructor overloading 

### Ambiguity of the variable names

In Java two or more variables cannot have the same name inside the same scope. But for the arguments and instance variables it can be same.

```java
class Example {
	int age;
	String name;

	Example(int age, String name){
		this.age = age;
		this.name = name;
	}
}

public class Main{
	public static void main(String[] args){
		Example ex = new Example(20, 'Sansiro');
	}
}
```

Here in the above example, this keyword refers to the object *ex* and assign the instance variables age and name as *20* and *Sansiro*


### Getters and Setters

This keyword is widely used with *getters* and *setters* 

```java
class Example{
	private int age;
	void setAge (int age){
		this.age = age;
	}

	int getAge(){
		return this.age;
	}
}
```

### Used in Constructor Overloading

In the case of constructor overloading there is another kind of this keyword is used. *this()*

Here *this()* is used to call another constructor of the same class.

```java
class Example{
	Example(int i, int j){
		//  Logic
	}
	
	Example(int i){
		this(i,i)
	}
}
```


## Final Keyword

The final keyword is used to declare constants, The final keyword can be used with variables, methods and classes.

- Once the variables is declared using final keyword, The variables cannot be manipulated
- Once the method is declared as final, The method cannot be overridden
- Once the class is declared as final, The class cannot be extended.

## Instance of operator

The Instance of operator is used to check whether an object is instance of a class or not.

```java
objectName instanceof className;
```

If this condition is satisfied, It returns *true* else return *false*


## Inheritance

Inheritance is one of the main feature of object oriented programming, Inheritance is used to create to new class from a existing class. The new class created is called as sub-class and the existing class is called as super-class.

```java
class BankAccount {
	protected String accountNumber;
	protected double balance;

	public BankAccount(String accountNumber, double intialBalance){
		this.accountNumber = accountNumber;
		this.balance = intialBalance;
	}

	public void deposit(double amount) { 
	balance += amount; 
	System.out.println("Deposited: " + amount); } 
	
	public void displayBalance() { 
	System.out.println("Account Number: " + accountNumber + ", Balance: " + balance); 
	}
}

class SavingsAccount extends BankAccount {
	private double intrestRate;

	public SavingsAccount(String accountNumber, double initialBalance, double interestRate) { 
	super(accountNumber, initialBalance);
	this.interestRate = interestRate; 
	}

	public void applyInterest() { 
	double interest = balance * interestRate / 100; balance += interest; 
	System.out.println("Interest applied: " + interest); 
	}
}
```

Here the super keyword is used to call the methods and constructors from the super class.

Inheritance works only when present of *is-a* relation between super and sub class

- Dog is a Animal
- Car is a Vehicle

When the super class and sub class has same method, then the method present in the super class is overridden by the sub class. This is called as *method overriding*

- The Protected Members present in super class can also be accessed by the sub-class

### Types of Inheritance

1. **Single Inheritance** : Single sub class is extended by the single super class
2. **Multilevel Inheritance** : Single sub class is extended by the single super class, Now the sub class also acts as the super class for another sub class.
3. **Hierarchical  Inheritance** : Here multiple sub classes extends single super class.
4. **Multilevel Inheritance** :  Here single sub class extends two or more super class

## Method Overriding

Method Overriding is a principle where method present in the super class overrides the method present in the sub-class. 

```java
class Animal{
	proctected void walks() {
		System.out.println("Animal Walks");
	}
}

class Dog extends Animal{
	@Override
	proctected void walks() {
		System.out.println("Dog Walks");
	}
}
```

In the above example the class Dog is inherited by the Animal class, when an object is created from the Dog class, the method is overridden.

- But we can access the method present in the super class using the super keyword.

Here also in the example we have used the annotation *@Override* it is not mandatory to use the annotation but if used, should follow all the rules of method overriding

### Rules of Method Overriding

- The method in both the classes should be of the same name, same return type and same parameters list
- We cannot override method declared as final or static
- Abstract methods of super class should be override

### Access Specifiers in method overriding

There can be different access specifiers for methods in super class and sub class, But only condition is that the access specifier in the sub class should have larger access than the super class.

For example for a method present in super class have access modifier of *protected* than the access specifier of the sub class should be either of *private* or *protected*

## Abstract Class and Abstract Methods

Abstract classes are the classes which cannot be instantiated, it is declared using *abstract* keyword. The classes declared using abstract keyword may or may not have abstract methods.

Abstract methods on the other hand does not contain any body. Its just the declaration. Abstract methods are called by the object of sub-class, If a method is declared as abstract then its class should also be abstract in nature.

```java
abstract class Bike {
    abstract public void brake();  
}

class MountainBike extends Bike {
    public void brake() {
        System.out.println("Breaking...");
    }
}

public class HelloWorld {
    public static void main(String[] args) {
        MountainBike Mb = new MountainBike();
        Mb.brake();  
    }
}
```

The constructor of Abstract methods can be used in the sub-class using the *super()* method


## Interface

- Interface is a abstract class where uses *interface* keyword to declare the interface, It Consists of various method definition.
- One can create a class by implementing an interface by providing all the definition of the methods defined in the interface.
- It is done using *implements* keyword
- Similar to class interface also can extend each other
- Single Interface can extend multiple interfaces as well

```java
interface Bike {
    public void brake();
}

interface BikeWithHardware extends Bike {
    public void wheels();
}

class MountainBike implements BikeWithHardware{
    public void brake() {
        System.out.println("Breaking...");
        }   
    public void wheels() {
        System.out.println("Bike has 2 Wheels...");
    }
}

public class HelloWorld {
    public static void main(String[] args) {
        MountainBike Mb = new MountainBike();
        Mb.brake();  
        Mb.wheels();
    }
}
```

### Default methods in interface

- One can provide default methods with its implementation inside of an interface using *default* keyword

```java
interface Bike {
    public void brake();
    public default void horn(){
        System.out.println("Sound Horn..");
    }
}

interface BikeWithHardware extends Bike {
    public void wheels();
}

class MountainBike implements BikeWithHardware{
    public void brake() {
        System.out.println("Breaking...");
        }   
    public void wheels() {
        System.out.println("Bike has 2 Wheels...");
    }
}

public class HelloWorld {
    public static void main(String[] args) {
        MountainBike Mb = new MountainBike();
        Mb.brake();  
        Mb.wheels();
        Mb.horn();
    }
}
```

## Abstraction 

Abstraction is one of the key feature of Object Oriented Programming, The main feature of Abstraction is to hide the unnecessary logic implementation, but provide only the feature or functionality to the user.

Think Abstraction as a Car every car has the functionality of Breaking, But instead of understanding how the internal working of breaking works, Just focus on what breaks does.

Abstraction can be implemented using two ways : 
1. Using Abstract Class
2. Using Interface

### Abstract Class

```java
abstract class Payment {
 abstract public void makePayment();
}

class CreditCard extends Payment {
    public void makePayment(){
        System.out.println("Payment Made Using Credit Card");
    }
}

class Upi extends Payment {
    public void makePayment(){
        System.out.println("Payment Made Using Credit Upi");
    }
}

public class HelloWorld {
    public static void main(String[] args) {
        CreditCard card = new CreditCard();
        Upi upi = new Upi();
        
        card.makePayment();
        upi.makePayment();
    }
}
```


### Interface

```java
 interface Payment {
  public void makePayment();
}

class CreditCard implements Payment {
    public void makePayment(){
        System.out.println("Payment Made Using Credit Card");
    }
}

class Upi implements Payment {
    public void makePayment(){
        System.out.println("Payment Made Using Credit Upi");
    }
}

public class HelloWorld {
    public static void main(String[] args) {
        CreditCard card = new CreditCard();
        Upi upi = new Upi();
        
        card.makePayment();
        upi.makePayment();
    }
}
```

### Why interface were introduced when there was already abstract class

1. To Support Multiple Inheritance
2. To avoid partial implementation of methods

### Multiple Inheritance

```java
interface Payable {
    void processPayment();
}

interface Refundable {
    void processRefund();
}

class Transaction implements Payable, Refundable {
    public void processPayment() {
        System.out.println("Processing payment...");
    }
    public void processRefund() {
        System.out.println("Processing refund...");
    }
}
```

## Polymorphism

Polymorphism is one of the core principles of object oriented programming, Polymorphism generally means which is present in multiple forms.

There are three ways in which polymorphism can be implemented in Java.
1. Method Overriding (Run Time Polymorphism)
2. Method Overloading (Compile Time Polymorphism)
3. Operator Overloading

### Method Overriding

The Method overriding is the phenomena where super class and sub class have the same name, But behave differently under different circumstances. Hence we can see polymorphism here 

```java
class Payment{
	public void makePayment(){
		System.out.println("Making Payment...");
	}
}

class CreditCard extends Payment{
	@Override
	public void makePayment(){
		System.out.println("Making Payment Using CreditCard");
	}
}

class UPI extends Payment{
	@Override
	public void makePayment(){
		System.out.println("Making Payment Using UPI");
	}
}
```

Here in the above example the *CreditCard* and *UPI* extends the *Payment* class, Here the method *makePayment* is polymorphic and is present in various forms.

Method to execute is decided during the runtime, hence it is called as runtime polymorphism 

### Method Overloading

Method overloading is a form of compile-time polymorphism where multiple methods in the same class have the same name but differ in their parameters (type, number, or both). The appropriate method is determined by the compiler based on the method signature, making it compile-time polymorphism.

Here is an example:

```java
class Payment {
    public void makePayment(int amount) {
        System.out.println("Making a Payment of " + amount);
    }

    public void makePayment(int amount, String currency) {
        System.out.println("Making a Payment of " + amount + " " + currency);
    }

    public void makePayment(int amount, String currency, String method) {
        System.out.println("Making a Payment of " + amount + " " + currency + " using " + method);
    }
}
```

In the above example, the `makePayment` method is overloaded to handle different types of payment requests:

1. **Single Parameter**: `makePayment(int amount)` for a basic payment.
2. **Two Parameters**: `makePayment(int amount, String currency)` for specifying the currency.
3. **Three Parameters**: `makePayment(int amount, String currency, String method)` for specifying both currency and payment method.

### Operator Overloading

The another method of polymorphism is Operator overloading, For example the same *+* operator can be used for addition and string concatenation as well.


## Encapsulation

Encapsulation is one of the feature of Object Oriented Programming, Which provides a way to bundle all the variables and methods inside a single class. 

- Using Encapsulation data hiding can be achieved.

```java
class AccountDetails {
	int accountNumber;
	String accountType;

	AccountDetails(int accountNumber,String accountType){
		this.accountNumber = accountNumber;
		this.accountType = accountType;
	}

	public void getAccountDetails(){
		// Logic
	}
}
```

Here in the above example the class *AccountDetails* has all its data members encapsulated in a single class. This is Encapsulation.

### Data Hiding Using Encapsulation

Data Hiding can be performed using Encapsulation, which prevents the external classes to access the private data members.

```java
class AccountDetails {
	private int accountNumber;
	private String accountType;

	AccountDetails(int accountNumber,String accountType){
		this.accountNumber = accountNumber;
		this.accountType = accountType;
	}

	public void getAccountDetails(){
		// Logic
	}
	
	public int getAccountNumber(){
		return this.accountNumber;
	} 
}
```

Here in the above example, The Data member *accountNumber* is made private and can be only accessed using the *getAccountDetails()* method,
This is how *Data Hiding* is achieved using Encapsulation.

