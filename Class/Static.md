# Static

Static 은 '정적인 고정된'이라는 뜻을 가지고있습니다. Static 은 메서드나 변수에 사용이 됩니다.


Static 의 특징을 살펴보자면  
1. 메모리에 고정적으로 할당
2. 객체 생성 없이 사용할 수 있다.
3. 프로그램이 시작되면 메모리의 Static 영역에 적재된다. 주로 클래스들이 Static 영역에 할당된다.  
   (New 연산자로 생성한 객체는 Heap영역에 적재) 프로그램이 종료될 때 해체 됩니다.  
   Static 영역은 모든 객체가 메모리를 공유하는 특징이있고  
   Heap 영역같은 경우는 메모리를 공유하지 않는 특징이있다.


아래 int num 을 6으로 만드는 예제로 정적변수가 뭔지에 대해 알아보았다.  

정적변수 ( Static Variables ) 사용 예시  
```java
public class StaticVariables {
	static int num = 5;

	public static void main(String[] args) {
   		 StaticVariables.num = 6;
	}
}
```
정적변수 ( Static Variables ) 미사용 예시  
```java
public class NoStaticVariables {
	int num = 5;

	public static void main(String[] args) {
		NoStaticVariables NoStatic = new NoStaticVariables();
		NoStatic.num = 6;
	}
}
```

정적변수를 사용했을 경우에는 메모리가 Static 영역으로 저장되어 클래스를 호출해서 (StaticVariables.num=6;) 변경할 수 있다.  
허나 정적변수를 사용하지 않은 경우에는 메모리를 공유하지 않는 특성때문에 객체를 생성하여 변경을 해주어야한다.

