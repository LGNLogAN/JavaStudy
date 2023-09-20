# Final

Final 의 사전적 의미로는 '최종적'이라는 뜻을 가지고있습니다. 자바에서는 이러한 사전적의미와 비슷한 기능을 하게됩니다.  


# final 필드
```java
final int num = 1;
```
이 처럼 변수 앞에 final 을 붙이고 초기화를 시키면 이 변수는 더 이상 초기화가 불가능하다.  
```java
final int num = 1;
num = 3; // Error
```


# final 클래스
```java
final class Company{
    String name = "회사명";
}
class A_Company extends Company{
}
```
위 예제는 class 에 final 키워드를 붙여 클래스를 최종상태로 만들어 상속이 불가능하게 만들었습니다.


# final 메소드

```java
class Company{
    public final void print() {
        System.out.println("회사 이름은 가우비즈 입니다.");
    }
}
class A_Company extends Company{
    // 오버라이딩 불가
    public void print(){
      // 컴파일 에러
    }
}
```
final 클래스는 상속이 안 되는것이였다면 final 메소드는 final 키워드가 붙게 되면 오버라이딩이 불가능하다.

```java
class Company{
    String name = "회사명";
    public void setName(final String name) {
    	//name = "ex회사2"; //인자값으로 받은 final변수는 변경 불가능
        this.name = name;
    }
}
public class Final_ex {
    public static void main(String[] args) {
    	final Company company = new Company();
    	company.setName("ex회사");
    }
}
```

이 처럼 setName 메소드안에 매개변수로 final String name 을 받아서 아래줄인 name = "ex회사"; 로 초기화가 불가능합니다.  

# final 객체

```java
class Company{
    String name = "회사명";

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }
}

public class Final_ex {
    public static void main(String[] args) {
    	final Company company = new Company();
    	//company = new Company(); //객체를 한번 생성했다면 재생성 불가능
    	company.setName("ex회사"); //클래스의 필드는 변경가능
    }
}
```
