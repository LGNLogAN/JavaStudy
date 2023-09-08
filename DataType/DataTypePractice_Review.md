예제 DatatypePractice.java
```java
package DataType;

  public class DataTypePractice {
      public static void main(String[] args) {
          char ch1 = 'A';
          System.out.println(ch1); // 문자 A를 int 형으로 나타내면 아스키코드 값을 출력해준다.
          System.out.println((int)ch1);
        
          char ch2 = 66;
          System.out.println(ch2); // 문자 자료형에 숫자형인 66을 넣게된다면 정수값에 해당되는 문자를 출력한다.
        
          int ch3 = 67;
          System.out.println(ch3); 
          System.out.println((char)ch3); // 숫자형인(int) 변수 ch3를 문자 자료형으로 출력하려고 하면 정수값에 해당되는 문자를 출력한다.
      }
}
```

실행값
<pre>
A
65
B
67
C
</pre>
이 예제는
