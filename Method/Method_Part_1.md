# 메서드

다른 프로그래밍 언어에서는 함수가 별도로 존재합니다.  
허나 자바는 클래스를 떠나 존재하는 것은 있을 수 없기에 자바의 함수는 따로 존재하지 않고 클래스 내에 존재합니다.  
이러한 클래스 내부의 함수를 메서드(Method)라고 합니다.  

메서드를 번역하면 "방법"을 의미합니다.  
어떠한 입력값을 가지고 어떠한 일을 수행 후 결과값을 내어놓는것을 메소드라고 합니다.


[ SoEasyMethod.java ]
```java
public class EasyMethod {
	public static void a() {
		System.out.println("Hello World");
	}
	public static void main(String[] args) {
		a();
	}

}
```

<pre>
실행 값 >  
Hello World
</pre>

위 코드는 a() 라는 메소드를 생성하고 그 안에 "Hello World" 를 출력하는 코드입니다.

[ EasyMethod.java ]

```java
public class EasyMethod {
	public static int add(int a , int b) {
		return a + b;
	}
	public static void main(String[] args) {
		System.out.println(add(2,6));
	}
}
```

<pre>
실행 값 >
8
</pre>

위 코드는 간단한 더하기를 해주는 메소드를 만들어 출력한 코드입니다.  
SoEasyMethod.java 예제와 다르게 int 값을 돌려주기 위해 함수반환형에 void 가 아닌 int 를 입력해주었습니다.  
void 는 말 그대로 '반환 할 값'이 없다는 뜻의 예약어 입니다.
