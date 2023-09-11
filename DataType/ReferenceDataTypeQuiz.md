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
int[] a2 = new int[1];
int[] b2 = new int[1];
int[] c2 = new int[1];

 a2[0] = 1; // <- a2[0] = 1의 주솟값을 갖는다
b2[0] = 2; // <- b2[0] = 2의 주솟값을 갖는다
c2 = b2; // <- c2에 b2의 주솟값을 할당, 즉 주솟값이 같다

c2[0] = 3; // <- c2 와 b2의 주솟값이 같은데 c2[0]=3; 이기에 1 3 3 이 나온다
       // <- ex) 104호라는 주소값을 b2와 c2가 얻었다. 여기서 c2[0] = 3; 으로 104호의 값을 3으로 지정
       // 즉 , b2 와 c2 의 주소값이 같기에 밑에 출력은 1 3 3 이 나오는게 맞다
System.out.println("[Example.2]");
System.out.println(a2[0]);
System.out.println(b2[0]);
System.out.println(c2[0]);
System.out.println(a2[0] == c2[0]); // <- a2[0] = 3; 으로 하면 3의 주솟값은 갖기에 true 가 나온다
System.out.println();
```

<pre>
실행 값 >  
1
3
3
</pre>
