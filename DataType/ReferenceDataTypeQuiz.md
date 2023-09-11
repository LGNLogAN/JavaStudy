# 참조자료형 퀴즈
[ ReferenceDateTypeQuiz.java ]  

# 1 번 문제  
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

# 2 번 문제  

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

c[0] = 3; // <- c 와 b 가 3이라는 데이터가 있는 메모리 주소 값이 같으니 b[0] 은 3의 주소값을 갖게 되고 c[0]도 3의 주소값을 갖게된다.
System.out.println(a[0] == c[0]); // a[0] 과 c[0] 은 갖고있는 데이터 실제값은 다르다. 따라서 주소값도 다르기에 False 가 출력된다.
                                  // 예외적으로 a[0] = 3; 을 입력하게된다면 동일한 주소값을 갖게되어 True 가 출력된다.
```


# 3 번 문제  

```java
String stringA = "A";
String stringB = "A";

System.out.println(stringA == stringB);
System.out.println(stringA.equals(stringB));

String stringC = "A";
String StringD = new String("A");

System.out.println(stringC == stringD);
System.out.println(stringC.equals(stringD));
```

<pre>
실행 값 >  
True
True
False
True
</pre>

위 문제를 풀기전 Java Heap 메모리 구조와 String Pool이 어떤것인지 알아야한다.  
Java 에서 String stringA = "A" 이런식으로 하게되면 String Pool 에 저장되고 주소값을 받게된다.  
허나 new String("A"); , new 연산자를 사용하게 되면 Heap 메모리에 객체를 생성하게 된다. ( Heap 메모리 안에 String Pool 이 존재 )  
따라서 참조자료형은 주소값을 받게되는 자료형이여서 둘의 주소값이 다르게 된다.  

```java
String stringA = "A"; // String Pool 에 저장된 주소 값 할당
String stringB = "A"; // String Pool 에 저장된 주소 값 할당

System.out.println(stringA == stringB); // 주소값이 같기에 True 가 출력된다.
System.out.println(stringA.equals(stringB)); // equals 는 주소값에 있는 실제값을 비교해서 Boolean 형식으로 나타내는 메소드이다.
                                             // 둘의 실제 값 "A" 는 같기에 True 출력

String stringC = "A"; // String Pool 에 저장된 주소 값 할당
String StringD = new String("A"); // Heap 메모리에 저장된 주소 값 할당

System.out.println(stringC == stringD); // 주소 값이 다르게 False 가 출력된다.
System.out.println(stringC.equals(stringD)); // 위에 설명에 따라 True 가 출력되게 된다.
```
