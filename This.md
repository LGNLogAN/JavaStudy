# This 예약어

This는 간단하게 설명하면 생성된 인스턴스 자기 스스로를 가르키는 예약어라고 생각하면 된다.  
간단 예제를 보고 설명해보겠다.  

```java
class ThisEx{

 String a = "안녕";
 ThisEx(String a) {
   this.a = a;
  }
}	  
public class ThisExample{

public static void main(String[] args){
    ThisEx te = new ThisEx("안녕하세요");
    System.out.println(te.a);  
    }
} 
```
위에 말했듯 this는 생성된 인스턴스 자기 자신을 나타내는것이다.  
```java
String a = "안녕";
 ThisEx(String a) {
   this.a = a; // <- 여기서 this는 String a 를 나타내는 것이다.
  }
```

만일 윗 코드를 this 가 없이 작성하려면 ?

```java
class ThisEx{

 String a = "안녕";
 ThisEx(String a_2) {
  a = a_2;
  }
}	  
public class ThisExample{

public static void main(String[] args){
    ThisEx te = new ThisEx("안녕하세요");
    System.out.println(te.a);  
    }
} 
```

이 처럼 생성자가 받는 매개변수의 이름을 바꿔주면 된다.

