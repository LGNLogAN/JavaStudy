 # Interface

 인터페이스는 추상클래스와 같이 추상적인 개념이다. 어쩌면 비슷해보일 수 있는데 둘의 용도는 다르고 차이점 또한 많다.

 우선 간단한 예를 보자

```java
interface I{
    public void z();
}
 
class A implements I{
    public void z(){}
}
```
I 라는 인터페이스가 있고 그  안에는 추상메서드가 존재한다.  
그리고 클래스 A 가 implements 로 I 인터페이스를 구현한다고 되어있는 부분이다.  
추상클래스와 같이 추상메서드가 있으면 무조건 구현해야한다.  
하지만 여기서부터 추상클래스와 인터페이스의 차이가 있는데 추상클래스는 추상메서드와 일반메서드를 작성할 수 있지만  인터페이스는 추상메서드만 작성이 가능하다.  


아래 예제로 인터페이스를 사용하는 예시를 들어보겠다.

```java
interface Animal {
  public abstract void cry();
}
```

```java
class Cat implements Animal {
    public void cry() {
        System.out.println("냐옹냐옹!");
    }
}
class Dog implements Animal {
    public void cry() {
        System.out.println("멍멍!");
    }
}
public class AnimalCrying {
    public static void main(String[] args) {
        Cat c = new Cat();
        Dog d = new Dog();
        c.cry();
        d.cry();
    }
}
```

이 예시는 강아지 , 고양이의 울음소리를 나타내는 코드이다.  
인터페이스에는 강아지와고양이의 공통적인 특징인 '울음'이란 메서드를 구현했다.  
이러한 인터페이스를 Cat , Dog 클래스에서 implements 를 통해 기능을 구현했다.
