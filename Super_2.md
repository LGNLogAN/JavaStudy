# Super

Super_2 장에서는 상속과 생성자에 대해 알아보겠다.



```java
class Calculator{
	int a , b;
	public void sum(int a , int b) {
		System.out.println(a+b);
  }
}
```

자바에서는 이러한 클래스가 있을 때 기본적으로 존재하는 생성자가 있다.
```java
Calculator(){}
```
위 예제는 이 기본생성자가 아닌 생성자를 따로 정의를 한 모습이다.  
이렇게 된다면 기본적으로 자동으로 만들어지는 기본생성자는 더 이상 자동적으로 만들어지지 않는다.  


```java
class Calculator{
	int a , b;
	public Calculator(int a, int b) {
		this.a = a;
		this.b = b;
	}
	public void sum(int a , int b) {
		System.out.println(a+b);
	}
}
class Calculator2 extends Calculator{
	public Calculator2(int a, int b) {
    this.a = a;
    this.b = b;
  }
}
```
<pre>
Implicit super constructor Calculator() is undefined. Must explicitly invoke another constructor
</pre>

"암시적인 슈퍼 생성자 Calculator()는 정의되지 않았습니다. 다른 생성자를 명시적으로 호출해야 합니다."  

위 예제는 오류가 발생하게 된다. Calculator 라는 클래스에서 생성자를 정의를 해서 기본적인 생성자는 자동적으로 생성되지 않는다.  
Calculator2 클래스가 Calculator 클래스를 상속받고 Calculator2 클래스의 생성자를 호출하기 전에 Calculator 클래스에서 생성자를 먼저 호출해야한다.  
하지만 기본적인 생성자가 없으므로 이와같이 수정해줘야한다.

```java
class Calculator{
	int a , b;
	public Calculator(int a, int b) {
		this.a = a;
		this.b = b;
	}
	public void sum(int a , int b) {
		System.out.println(a+b);
	}
  Calculator(){}
}
class Calculator2 extends Calculator{
	public Calculator2(int a, int b) {
    this.a = a;
    this.b = b;
  }
}
```

다른 방법으로는

```java
class Calculator{
	int a , b;
	public Calculator(int a, int b) {
		this.a = a;
		this.b = b;
	}
	public void sum(int a , int b) {
		System.out.println(a+b);
	}
}
class Calculator2 extends Calculator{
	public Calculator2(int a, int b) {
    super(a,b);
  }
}
public class SuperInstance {
	public static void main(String[] args) {
		Calculator cal = new Calculator2(5, 6);
		cal.sum();
	}
}
```
<pre>실행 값 >
11</pre>

Super 메서드를 활용한 방법이 있다. 부모클래스의 생성자를 명시적으로 호출하기 때문이다.  
Super 메서드를 쓸 때 주의할 점이 있는데
변수를 초기화든 뭘 하든 무조건 super 메서드 아래에 작성해야한다는것이다. 
```java
class Calculator{
	int a , b;
	public Calculator(int a, int b) {
		this.a = a;
		this.b = b;
	}
	public void sum2(int a , int b) {
		System.out.println(a+b);
	}
}
class Calculator2 extends Calculator{
	
	public Calculator2(int a , int b) {
		super(a,b);  
		this.a = 10; // <- super 메서드 아래 작성 super 메서드 위에 작성할 시 에러발생
	}
	public void sum() {
		System.out.println(this.a + this.b);
	}
}
public class SuperInstance {
	public static void main(String[] args) {
		Calculator2 cal2 = new Calculator2(2,3);
		cal2.sum2(2, 3);
		cal2.sum();
	}
}
```

<pre>실행 값 >
5
13</pre>
