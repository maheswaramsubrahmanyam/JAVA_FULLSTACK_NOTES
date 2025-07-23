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

use of constructor in java?
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














