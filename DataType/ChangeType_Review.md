
```java
package DataType;

public class ChangeType {

public static void main(String[] args) {
	int n = 10;
	double dnum = n;
	System.out.println(dnum);
	
	double dnum2 = 20;
	int n2 = dnum2; <- 오류발생
	int n2 = (int)dnum2;
	
	System.out.println(n2);
	}
}
```
