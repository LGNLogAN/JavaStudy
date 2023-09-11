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
          System.out.println((char)ch3); // 변수 ch3을 자료형으로 출력하려고 하면 정수값에 해당되는 문자를 출력한다.
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

컴퓨터는 내부에서 어떠한 문자를 표현할때 특정 정수값을 정하자고 약속합니다.   
예를 들어 A 라는 문자를숫자값으로 나타내면 65 가 나오게되는데 이런 코드 값을   
모아 둔 것을 '문자 세트'라고 합니다.   
정해진 코드 값을 변환하는 것을 '문자 인코딩'(encoding)이라고하고   
반대로 코드 값을 다시 문자로 변환하는 것을 '문자 디코딩'(decoding)이라고합니다.   
이 예제는 이러한 특성을 가지고 문자형 연습을 한것입니다.
