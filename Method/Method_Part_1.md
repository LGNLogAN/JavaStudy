# 메소드

다른 프로그래밍 언어에서는 함수가 별도로 존재합니다.  
허나 자바는 클래스를 떠나 존재하는 것은 있을 수 없기에 자바의 함수는 따로 존재하지 않고 클래스 내에 존재합니다.  
이러한 클래스 내부의 함수를 메소드(Method)라고 합니다.  

메소드를 번역하면 "방법"을 의미합니다.  
어떠한 입력값을 가지고 어떠한 일을 수행 후 결과값을 내어놓는것을 메서드라고 합니다.

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

