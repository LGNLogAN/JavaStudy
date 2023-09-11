# 참조자료형 퀴즈
[ ReferenceDateTypeQuiz.java ]  

1 번 문제  
```java
int a = 1;
int b = 2;
int c = b;
c = 3;

System.out.println(a);
System.out.println(b);
System.out.println(c);
```

<pre>
실행 값 >  
1
2
3
</pre>

이는 기본자료형인 int 자료형을 사용해서 실제 값을 갖게 된다. 따라서 a = 1 , b = 2 , c = b -> c = 3 이런 식으로 각 변수에 값이 할당된다.  

2 번 문제  

```java
int[] a = new int[1];
int[] b = new int[1];
int[] c = new int[1];

a[0] = 1;
b[0] = 2;
c = b;
c[0] = 3;

System.out.println(a[0]);
System.out.println(b[0]);
System.out.println(c[0]);
System.out.println(a[0] == c[0]);
```

<pre>
실행 값 >  
1
3
3
false
</pre>

위 문제는 참조자료형을 사용한 문제이다. 참조자료형은 데이터가 저장된 메모리의 주소 값을 갖는 자료형이다.  
int[] a = new int[1] 으로 new 연산자를 사용하여 a 변수에 int[1] 만큼의 데이터 Array를 생성했다.  

```java
a[0] = 1; // <- a2[0] = 1의 주솟값을 갖는다
b[0] = 2; // <- b2[0] = 2의 주솟값을 갖는다
c = b; // <- c에 b의 주솟값을 할당, 즉 주솟 값이 같다

c[0] = 3; // <- c 와 b 가 3이라는 데이터가 있는 메모리 주소 값이 같으니 b[0] 은 3의 주소값을 갖게 되고 c[0] 도 3의 주소값을 갖게된다
System.out.println(a[0] == c[0]); // a[0] 과 c[0] 은 갖고있는 데이터 실제값은 다르다. 따라서 주소값도 다르기에 False 가 출력된다.
                                  // 예외적ㅇ로 a[0] = 3; 을 입력하게된다면 동일한 주소값을 갖게되어 True 가 출력된다.
```
