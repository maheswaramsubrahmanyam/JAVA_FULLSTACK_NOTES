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

String s = m.getMarks();

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















