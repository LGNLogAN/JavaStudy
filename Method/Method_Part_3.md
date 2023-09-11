# 메서드

## Method_Part_1,2 심화

[ AcountingApp_1.java ]

```java
public class AccountingApp{
	public static void main(String[] args){
		double valueOfSupply = 10000.0;
		double vatRate = 0.1;
		
		double vat = valueOfSupply*vatRate;
		
		double total = valueOfSupply + vat;
		
		System.out.println("Value of Supply : " + valueOfSupply);
		System.out.println("Vat : " + vat);
		System.out.println("Total : " + total);
	}
}
```
<pre>실행값> 
Value of supply : 10000.0
Vat : 1000.0
Total : 11000.0
</pre>
위 코드는 세금을 계산해주는 코드이다. 이 단순한 코드에 메서드를 활용해서 작성해보았다.  

```java
public class AccountingApp {
	public static double valueOfSupply = 10000.0;
	public static double vatRate = 0.1;
	
	public static double getVat() {
		return valueOfSupply * vatRate;
	}
	
	public static double getTotal() {
		return valueOfSupply + getVat();
	}

	public static void main(String[] args) {;
	
		System.out.println("Value of supply : " + valueOfSupply);
		System.out.println("Vat : "+ getVat());
		System.out.println("Total : " + getTotal());
	}

}
```
