# abstract | 추상 클래스

 ## 추상클래스란 ?

 추상클래스는 말그대로 추상적인 클래스이다.  
 보통 클래스는 어떠한 객체를 생성해내기위한 설계도를 말한다.  
 간단하게 말하자면 설계도를 만들기 위한 설계도를 추상클래스라고 한다.  


추상클래스는 이러한 방식으로 만든다.  

```java
abstract class A{ }
```
기존에 클래스를 만드는 방식에서 <b>abstract</b> 라는 키워드를 붙여 만든다.  
추상클래스 안에는 추상메서드또한 존재한다.  
```java
abstract class A{
  public int JustMethod(){
    return 4;
}
  public abstract int Move();
}
```
이런식으로 껍대기만 존재는 메서드이다. 위 코드에서 보다싶이 메서드는 추상적으로 있는 메서드이다.
어떠한 기능을 구현하지않지만 메서드이름을 보면 Move 인거처럼 추상적으로 어떠한 기능을 하는지 알 수 있다.
또한 일반메서드와 추상클래스가 같은 클래스에서 사용되는걸 알 수 있다.  


추상클래스는 메서드멤버들 중 하나라도 추상메서드가 존재하면 그 클래스는 무조건적으로 추상클래스가 된다.
그리고 추상클래스는 인스턴스화를 시킬 수 없다.

# 추상클래스 상속
```java
abstract class A{
    public abstract int b();
    public void d(){
        System.out.println("world");
    }
}
class B extends A{}
```
추상클래스는 상속할 수 있다. 허나 위에 예제는 오류가 발생한다.  
이유는 추상클래스 A 에는 추상메서드가 존재하기 때문이다. 따라서 상속받은 클래스 B가 b() 메서드를 구현을 해줘야만 한다.
```java
abstract class A{
	int a = 2;
    public abstract int b();
    public void d(){
        System.out.println("world");
    }
}
class B extends A{
    public int b(){return 1;}
}
class C extends A{
  public String b(){ return "안녕하세요"; }
}
public class abstract_1 {
    public static void main(String[] args) {
        B obj = new B();
        System.out.println(obj.b());
    }
}
```
<pre>실행 값 >
1</pre>

추가적으로 C클래스를 보면 A 클래스를 상속하여 추상메서드를 B클래스와는 다르게 기능을 구현했다.  
이 처럼 재사용률과 유지보수의 편의성을 높일 수 있다.  
