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
<pre>실행값 > 
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
<pre>실행값 > 
Value of supply : 10000.0
Vat : 1000.0
Total : 11000.0
</pre>

```java
public class AccountingApp {
	public static double valueOfSupply = 10000.0;
	public static double vatRate = 0.1;
```

위 부분은 valueOfSupply , vatRate 을 AccountingApp 클래스의 직접적인 소속임을 밝혔다.  
( 만일 main 메서드에 작성을 하게된다면 지역변수로 에러가 발생한다. )  

```java
public static double getVat() {
		return valueOfSupply * vatRate;
	}
	
	public static double getTotal() {
		return valueOfSupply + getVat();
	}
```

위 부분은 위에서 AcountingApp 클래스의 직접적으로 선언한 변수 ValueOfSupply 와 vatRate를 곱한 값을 반환한 getVat() 메서드를  
getTotal() 메서드에 valueOfSupply + getVat() 으로 메서드를 직접호출해 사용한 모습이다. 
