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

```
CUSTOMER.java

package bankApp

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

```
SBI.java 

package bankApp

public class SBI
{

String password;
}
```

---

# use of constructor in java?
⦁	to initialize the objects 



```

CUSTOMER.java



package bankApp



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

```
SBI.java

package bankApp

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



```
MAHESH.java

package bankApp

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



```
SSC.java

package bankApp

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

```
B.java

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

```
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

```

SCORE.java



package marksApp



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

```

MARKS.java

package bankApp

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

```
A.java

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

```
B.java

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

```
C.java
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
```
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

```
A.java

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

```
B.java

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

```
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
<pre>
```
D.java
package demo;
public class D {


public static void main(String[]  args){
C b = new C();
b.add();
}
}
```
</pre>

















