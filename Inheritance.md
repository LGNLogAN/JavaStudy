# Inheritance 상속

상속은 말 그대로 상속이다. 부모클래스의 기능을 자식클래스가 물려받을 수 있는것이다.  

```java
class Cal{
	public int sum(int a , int b){
		return a+b;
	}
}
class Cal2 extends Cal{ }
}
```

위에 코드는 Cal2 라는 클래스가 Cal 클래스의 기능을 상속받은 코드이다.  
상속을 하려면 <b>extends</b>라는 키워드가 들어간다.  

아래 예제를 통해 상속이 잘 됐는지 확인해보자.  

```java
public class InheritanceApp {
	public static void main(String[] args) {
		Cal2 c = new Cal2();
		System.out.println(c.sum(1,9));
	}
}
```

<pre>
실행 값 >  
10
</pre>

이렇게 기능을 잘 상속 받은 걸 알수있다.  
이제 그 기능을 개선하고 발전할 수 있게 해보자.

```java
class Cal{
	public int sum(int a , int b){
		return a+b;
	}
}
class Cal2 extends Cal{
	public int minus(int a , int b) {
		return a-b;
	}
}

public class InheritanceApp {
	public static void main(String[] args) {
		Cal2 c = new Cal2();
		System.out.println(c.sum(1,9));
		System.out.println(c.minus(5, 2));
	}
}
```
<pre>
실행 값>
10
3
</pre>

이렇게 기능을 추가할 수 있다.

다음은 개선이다.

```java
class Cal{
	public int sum(int a , int b){
		return a+b;
	}

}
class Cal2 extends Cal{
	public int minus(int a , int b) {
		return a-b;
	}

	public int sum(int a , int b){
    System.out.println("이것은 오버라이딩됐습니다.");
		return a+b;
	}

}
public class InheritanceApp {
	public static void main(String[] args) {
		Cal2 c = new Cal2();
		System.out.println(c.sum(1,9));

	}
}
```
<pre>실행 값 >
이것은 오버라이딩됐습니다.
10</pre>

이 처럼 부모클래스에 있는 메서드인 sum을 자식 클래스에다 다시 덮어쓰는 형식으로 사용하는것을 <b>오버라이딩 ( OverRiding )</b>이라고 한다.
