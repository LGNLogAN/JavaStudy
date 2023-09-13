# OverLoading

오버라이딩 과 오버로딩은 느낌상 비슷하다.  
하지만 상속과 관련있는 오버라이딩과는 다르게 오버로딩은 상속과 관련이 없다.  

자바는 메서드의 이름이 같아도 상관이 없다. 형태만 다르면 된다. 

```java
class Cal{
	public int sum(int a , int b){
		return a+b;
	}
  public int sum(int a , int b , int c){
		return a+b+c;
	}
}
```

이 처럼 형태가 다른 메서드를 생성하는 것을 오버로딩 ( Overloading ) 이라고 한다.

