# JAVA_FULLSTACK_NOTES

src <br>
new  <br>
package  <br>

name of package  <br>

objects stored in heap area initization of objects   <br>
1.	using reference variable 
2.	using constructor 
3.	using setters method 
 <br>
using reference variable

```java
//CUSTOMER.java

package bankApp;

public class CUSTOMER 
{

public static void main(String , args[])
{
SBI sl = new SBI();
SBI s2 = new SBI();
s1.password = "123";
s2.password = "345";
System.out.println(sl.password);
System.out.println(s2.password);
}
}
```
---

```java
//SBI.java 

package bankApp;

public class SBI
{

String password;
}
```

---

# use of constructor in java?
⦁	to initialize the objects 



```java

//CUSTOMER.java



package bankApp;



public class CUSTOMER 

{



public static void main(String , args[])

{

SBI sl = new SBI();

SBI s2 = new SBI();

System.out.println(sl.password);

System.out.println(s2.password);

}
}

```

---

```java
//SBI.java

package bankApp;

public class SBI
{

String password;
SBI(String str) 
  {
     password = str;
  }
}
```
---
# Encapsulation in java

By making variable as private and using set and get method



```java
//MAHESH.java

package bankApp;

public class MAHESH
{

public static void main(String , args[])
{
SSC m = new SSC();
m.setPassword('133');
String s = m.getPassword();
System.out.println(s);
}
}
```



---



```java
//SSC.java

package bankApp;

public class SSC
{

private String password;
Public void setPassword(String s)  {
     password = s;
  }
public String getPassword(){

    return password;

}
}
```

---
# use of this keyword in java?
# difference b/w this keyword and this() constructor call?

# this keyword
whenever local and instance variables are same there is ambiguity for JVM and expected output will not be achieve and JVM provide default value as output.<br>
this keyword always refers to current class instance variable 

```java
//B.java

package demo; 
public class B 
{
 int marks;
void add(int marks)
  {
   this.marks = marks;
   sub();
  }
  void sub() 
  {
   System.out.println(marks);
  }
}
```

```java
package demo;
public class A
{
  public static void main(string , args[])
   {
    B b= new B();
    b.add(99);
   }
}
```
# this VS this() 

- this is a keyword it is used to refer current class instance variables 
- this() constructor it is used to call from one constructor to another

# 4 pilers of oops?



- class and object

- inheritance 

- polymorphism

- abstraction 

- encapsulation 

# Use of Encapsulation 

- used for data security


## Encapsulation in Java
- Wrapping up data and methods acting on that data in a single unit 

```java

//SCORE.java
package marksApp;

public class SCORE

{

public static void main(String , args\[])

{

MARKS m = new SSC();

m.setMarks(95);

int s = m.getMarks();

System.out.println(s);

}
}

```

---

```java

//MARKS.java

package bankApp;

public class MARKS

{

private int marks;

Public void setMarks(int s)  {

     marks = s;

  }

public int getMarks(){

   return marks;

}

}
```


# inhertance 

```java
//A.java

package demo;

public class A
{

void add(){
 int a=10;
 int b = 20;
 System.out.println(a+b);
}

}
```
---

```java
//B.java

package demo;
public class B extend A {

void mul(){
int a = 10;
int b = 20;
 System.out.println(a*b);
}
}
```
---

```java
//C.java
package demo;
public class c {

public static void main(String[]  args){
B b = new B();
b.add();
}
}
```

# types of inheritances 
- single Inheritance
- multilevel Inheritance
- multiple Inheritance
- Hybrid Inheritance
- Heirichal Inheritance

# Single Inheritance 
getting proporties and methods from parant class to child class is called single inheritance 

### syntax 
```java
Class A {
   variables
   method1(){
    // block of code
   }
   method2(){
    // block of code
   }
}
Class B extends A {
   variables
   method3(){
    // block of code
   }
   method4(){
    // block of code
   }
}
```
# Multilevel Inheritance

Class which extends a class and that class is further extended by another class is called as multi level inheritance 

```java
//A.java

package demo;

public class A
{

void add(){
 int a=10;
 int b = 20;
 System.out.println(a+b);
}

}
```
---

```java
//B.java

package demo;
public class B extend A {
void mul(){
int a = 10;
int b= 20;
System.out.println(a * b);
}
}
```
---

```java
C.java

package demo;
public class C extend B {

void sub(){
int a = 10;
int b= 20;
System.out.println(a - b);
}
}
```
---

```java
//D.java
package demo;
public class D {


public static void main(String[]  args){
C b = new C();
b.add();
}
}
```
# why Multiple Inheritance not possible in Java with class

becouse of ambiguty problem multiple inheritance is not supported 
> to achive multiple inheritance we use Interfaces consepts

# hirichical 
# Java Inheritance & Polymorphism Notes

##  Hierarchical Inheritance in Java

Hierarchical inheritance occurs when **multiple subclasses inherit** from a **single superclass**.

###  Example:

```java
class Animal {
    void eat() {
        System.out.println("This animal eats food.");
    }
}

class Dog extends Animal {
    void bark() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {
    void meow() {
        System.out.println("Cat meows");
    }
}

public class Main {
    public static void main(String[] args) {
        Dog d = new Dog();
        d.eat();
        d.bark();

        Cat c = new Cat();
        c.eat();
        c.meow();
    }
}
```
# Method Overloading (Compile-Time Polymorphism)
 Method Overloading means defining multiple methods with the same name but different parameters (type, number, or order) within the same class.

## Rules:
Must differ in parameter list

Can have different return types (but not only return type)

### Example:

```java
class Calculator {
    int add(int a, int b) {
        return a + b;
    }

    double add(double a, double b) {
        return a + b;
    }

    int add(int a, int b, int c) {
        return a + b + c;
    }
}

public class Main {
    public static void main(String[] args) {
        Calculator c = new Calculator();
        System.out.println(c.add(5, 10));
        System.out.println(c.add(5.5, 3.3));
        System.out.println(c.add(1, 2, 3));
    }
}
```
# Method Overriding (Run-Time Polymorphism)
Method Overriding allows a subclass to provide a specific implementation of a method already defined in its superclass.

## Rules:
- Must have same method name, return type, and parameters

> Must be in subclass

> Cannot override final or static methods

### Example:
```java
class Animal {
    void sound() {
        System.out.println("Animal makes sound");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal a = new Dog();  // Upcasting
        a.sound();             // Calls Dog's sound()
    }
}
```

# instance block

instance block called automatically during object creation before constructor call 
```java
// Demo.java
package p1;
public class Demo {
 void add(){
  System.out.println("Method");
  }
  Demo(){
  System.out.println("Constructor");
  }
  // instance block
  {
   System.out.println("Instance block");
   }
```
```java
//Demo1.java
package p1;
public class Demo1 extends Demo
{
 public static void main(String[] args){
   Demo d = new Demo();
   d.add();

}
}


```

# static block vs instance block 
static block will be excuted automatically during class loading before objcet creation 

```java
// Demo.java
package p1;
public class Demo
{
   {
     System.out.println("Static Block");
   }
   static
   {
     System.out.println("Static block1 ");
    }
    static
   {
     System.out.println("Static block2 ");
    }

}
```

```java
//Demo1.java
package p1;

public class Demo1 extends Demo
{
  public static void main(String[] args)
  {
   Demo d = new Demo();
  }
}
```
# instance block are used to initlizes instace variables and stactic blocks are used to initlize static variables 
```java
// Demo.java
package p1;
public class Demo
{
  int a;
  static int b;
   {
     a=100;
   }
   static
   {
     b=200;
    }
    void
   {
     System.out.println(a);
     System.out.println(b);
    }

}
```

```java
//Demo1.java
package p1;

public class Demo1 extends Demo
{
  public static void main(String[] args)
  {
   Demo d = new Demo();
   d.show();
  }
}
```
--- 
```java
package firstAPP;

//Demo1.java

public class Demo1 extends Demo
{
  public static void main(String[] args)
  {
   Demo d = new Demo();
   Demo d1 = new Demo();
   Demo d2 = new Demo();
  }
}
```

```java
// Demo.java
package firstAPP;
public class Demo
{
  
   {
     System.out.println("instance blcok");
   }
   

}
```
---
# private method cannot me overrided

```java
// Demo.java
package firstAPP;
public class Demo
{
  private void m1()
   {
     System.out.println("Method 2");
   }
   

}
```
```java
package firstAPP;

//Demo1.java

public class Demo1 extends Demo
{
   void m1() {
	  System.out.println("Method 1");
  }
}
```


# ststic menthod cannot be overided it is called method hiding 

```java
package firstAPP;

//Demo1.java

public class Demo1 extends Demo
{
   static void m1() {
	  System.out.println("Method 1");
  }
}

```
```java
// Demo.java
package firstAPP;
public class Demo
{
  static void m1()
   {
     System.out.println("Method 2");
   }
   

}
```
```java
package firstAPP;

public class Demo2 {
	
	public static void main(String[] args) 
		{
			Demo d = new Demo1();
			d.m1();
		
	   }
}
```


# final method cannot be overrided 
```java
// Demo.java
package firstAPP;
public class Demo
{
  final void m1()
   {
     System.out.println("Method 2");
   }
   

}
```
```java
package firstAPP;

//Demo1.java

public class Demo1 extends Demo
{
    void m1() {
	  System.out.println("Method 1");
  }
}

```
```java
package firstAPP;

public class Demo2 {
	
	public static void main(String[] args) 
		{
			Demo d = new Demo1();
			d.m1();
		
	   }
}

```
# child class method access >= parent class method access 
# public >= public true
# default >= public false

```java
// Demo.java
package firstAPP;
public class Demo
{
  public void m1()
   {
     System.out.println("Method 2");
   }
   

}
```
```java
package firstAPP;

//Demo1.java

public class Demo1 extends Demo
{
     void m1() {
	  System.out.println("Method 1");
  }
}

```
```java
package firstAPP;

public class Demo2 {
	
	public static void main(String[] args) 
		{
			Demo d = new Demo1();
			d.m1();
		
	   }
}
```
# protected >= public 


```java
// Demo.java
package firstAPP;
public class Demo
{
  protected void m1()
   {
     System.out.println("Method 2");
   }
   

}
```
```java
package firstAPP;

//Demo1.java

public class Demo1 extends Demo
{
     void m1() {
	  System.out.println("Method 1");
  }
}

```
```java
package firstAPP;

public  class Demo2 {
	
	public static void main(String[] args) 
		{
			Demo d = new Demo1();
			d.m1();
		
	   }
}
```
# final variable keyword in java 
when final keyword is used with variable that variable value will be constant and can`not be changed or updated 

```java
// Demo.java
package firstAPP;
public class Demo
{
   void add()
   {
	   final int a = 100;
	   a = 300; // error bcz final vaiable cannot be chnanged 
     System.out.println(a);
   }
   

}
```
# final  method
when final keyword is used with method that method will be constant and cannot be overrided 


```java
// Demo.java
package firstAPP;
public class Demo
{
  final void add()
   {
     int a = 100;
     System.out.println(a);
   }
   

}
```
# final class
when final keyword uded with class that class cannot be extended 

```java
// Demo.java
package firstAPP;
public final class Demo
{
   void add()
   {
     int a = 100;
     System.out.println(a);
   }
   

}
```

```java
package firstAPP;

public class Demo2 extends Demo //error {
	
	public static void main(String[] args)
           {
            Demo d = new Demo1();
            d.add();
           }
}

```

- constructor cannot be made as final but we can make it as private
- when constructor made as private we cannot be create objects for that class
- we cannot make class as private and protected but we can make class as default and public

# abstraction 
the methods which are having method bodys are called as concrate methods 
## abstract method 
the methods which are dont have method body are called as abstract methods if the method dones't have method body that method should be declared using absctarct keyword 



```java
package SBIBankAccountSystem;

public class BankAccount {
    private String accountNumber;
    private String accountHolder;
    private double balance;

    
    public BankAccount(String accountNumber, String accountHolder, double balance) {
        this.accountNumber = accountNumber;
        this.accountHolder = accountHolder;
        this.balance = balance;
    }

    public String getAccountNumber() {
        return accountNumber;
    }

    public String getAccountHolder() {
        return accountHolder;
    }

    public double getBalance() {
        return balance;
    }

    public void setAccountNumber(String accountNumber) {
        this.accountNumber = accountNumber;
    }

    public void setAccountHolder(String accountHolder) {
        this.accountHolder = accountHolder;
    }

    public void setBalance(double balance) {
        this.balance = balance;
    }

    public void deposit(double amount) {
        if (amount > 0) {
            balance += amount;
            System.out.println("Deposited: " + amount);
        } else if (amount <= 0) {
            System.out.println("Invalid deposit amount.");
        }
    }

    public void withdraw(double amount) {
        if (amount > 0 && amount <= balance) {
            balance -= amount;
            System.out.println("Withdrawn: " + amount);
        } else if (amount <= 0) {
            System.out.println("Insufficient balance.");
        }
            
    }
public static void main(String[] args) {
        
        BankAccount account = new BankAccount("123456789SBI", "Maheswaram Subrahmanyam", 11000.0);
        System.out.println("Account Number: " + account.getAccountNumber());
        System.out.println("Account Holder: " + account.getAccountHolder());
        System.out.println("Initial Balance: "  + account.getBalance());

        account.deposit(5868.0);
        System.out.println("Balance after deposit: " + account.getBalance());
        account.withdraw(2890.0);
        System.out.println("Balance after withdrawal: " + account.getBalance());
        account.withdraw(2000.0);
        System.out.println("Balance after withdrawal: " + account.getBalance());

    }
}


    
```

# Arrays in Java
## What is an Array?
An array in Java is a container object that holds a fixed number of values of the same type. It's used to store multiple values in a single variable, instead of declaring separate variables for each value.

# Features:
- Arrays are fixed in size.
- All elements must be of the same data type.
- Elements are stored in contiguous memory locations.
- Indexing starts from 0.
- Declaration and Initialization:
```java

int[] numbers; // declaration
numbers = new int[5]; // memory allocation

// initialization
numbers[0] = 10;
numbers[1] = 20;
numbers[2] = 30;
numbers[3] = 40;
numbers[4] = 50;

// or declare and initialize together
int[] numbers = {10, 20, 30, 40, 50};
```

# Accessing Elements:

```java

System.out.println(numbers[2]); // prints 30
```
# Looping Through Arrays:
```java

// using traditional for loop
for (int i = 0; i < numbers.length; i++) {
    System.out.println(numbers[i]);
}

// using enhanced for loop
for (int num : numbers) {
    System.out.println(num);
}
```
# Types of Arrays:
- One-Dimensional Array – a simple list of elements.

- Multi-Dimensional Array – an array of arrays.

## Example of a two-dimensional array:

```java

int[][] matrix = {
    {1, 2, 3},
    {4, 5, 6}
};
System.out.println(matrix[1][2]); // prints 6
```
# Common Operations:
> array.length
>> returns the size of the array.

> Arrays.sort(array)
>> sorts the array (needs import java.util.Arrays;).

> array.clone()
>> returns a copy of the array.

## Example Program:
```java

public class ArrayExample {
    public static void main(String[] args) {
        int[] marks = {90, 80, 85, 70, 95};

        for (int i = 0; i < marks.length; i++) {
            System.out.println("Mark " + (i + 1) + ": " + marks[i]);
        }
    }
}
```
