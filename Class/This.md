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
