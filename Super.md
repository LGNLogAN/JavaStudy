# Super

super 는 두 가지 종류가 있다.  

   <b>Super</b> 키워드  
Super 키워드는 자신이 상속 받은 부모클래스를 가르키는 참조변수입니다.  

   <b>Super()</b> 메서드  
Super() 메서드는 자신이 상속 받은 부모클래스를 가르키는 메소드입니다.  

이렇게 두 가지가 있다.  
상속이 부모클래스의 속성과 기능을 상속받는 것이라고 했다.  
하지만 자식클래스의 변수와 부모클래스의 변수나 메서드명이 같으면 자신의 변수나 메서드를 사용하게 되는데  
<b>Super</b>를 쓰게 된다면 부모클래스를 호출해 쓸 수 있다.

아래는 그 예제이다.

```java
class ExampleNum{
	int num = 5;
}

class Inheritance extends ExampleNum{
	int num = 4;
	void test() {
		System.out.println(num);
	}
}

public class Inheritance_1 {
	public static void main(String[] args) {
		Inheritance it = new Inheritance();
		it.test();
	}
}

```
<pre>실행 값 >
4</pre>

이 처럼 상속받은 부모클래스의 변수가 출력되지않고 자식클래스의 변수를 따로 선언했더니 4가 출력됐다.  

아래는 Super 키워드를 활용한 예제이다.
```java
class ExampleNum{
	int num = 5;
}
class Inheritance extends ExampleNum{
	int num = 4;
	void test() {
		System.out.println(super.num);
	}
}
public class Inheritance_1 {
	public static void main(String[] args) {
		Inheritance it = new Inheritance();
		it.test();
	}
}
```

<pre>실행 값 >
5</pre>

이 처럼 super 키워드를 활용하여 부모클래스의 변수를 호출해서 5가 출력되는걸 알 수 있다.

---

```java
class ExampleNum{
	int num = 5;
}
class SuperKeywordTest extends ExampleNum{
	int num = 10;
	// super.num = 20; <- super 는 상위 클래스를 호출하는 키워드여서 상위클래스의 변수를 수정할 수 없다.
	void SuperTest(){
		super.num = 20; // <- 상위클래스의 실제값은 바뀌지않는다.
		System.out.println(num);
		System.out.println(this.num);
		System.out.println(super.num);
	}
}
public class SuperKeyWordExample {
	public static void main(String[] args) {
		SuperKeywordTest skt = new SuperKeywordTest();
		skt.SuperTest();
		firstNum fn = new firstNum();
		System.out.println(fn.a); // <- 상위클래스 변수의 실제 값이 수정되었는지 확인
    
	}
}
```
<pre>실행 값 >
10
10
19
5</pre>

