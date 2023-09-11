# 접근제어자 

접근제어자 종류는 <b>public</b> , <b>protected</b> , <b>default</b> ,<b>private</b> 가 있다.  
앞으로 객체지향을 공부하는데 알아두면 좋을거같아서 정리를 했다.  

[ accessLevelModifiers_1.java ]

```java
public class accessLevelModifiers_1 {
	public static void hi() {
		System.out.println("안녕");
	}
	public static void main(String[] args) {
		hi();
	}
}
```
<pre>실행 값 >
안녕</pre>

그냥 평범한 메서드를 생성해 만든 간단한 코드이다.  
여기서 hi() 메서드에 private 라는 접근제어자를 사용해보면 ?  

```java
public class accessLevelModifiers_1 {
	private static void hi() {
		System.out.println("안녕");
	}
	public static void main(String[] args) {
		hi();
	}
}
```
<pre>실행 값 >
안녕</pre>

아무 문제 없이 출력이 된다. 하지만 여기서 accessLevelModifiers_1 라는 클래스 말고 다른 클래스에 사용이 된다면 ?

```java
class hello{
	private static void hi() {
		System.out.println("안녕");
	}
}
public class privateMethod {
	public static void main(String[] args) {
		hello.hi();
	}
}

```
<pre>실행 값 >
에러발생</pre>

private 는 같은 클래스에서만 사용할 수 있다. 위 코드는 hello 클래스에서 private로 메서드가 생성되어서  
에러가 발생한다. private 를 public 로 변환하면 코드가 정삭적으로 실행되는걸 알 수 있다.  
