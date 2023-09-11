# 묵시적 형 변환 과 명시적 형 변환


[ ChangeType.java Code ]

```java
package DataType;

public class ChangeType {

public static void main(String[] args) {
	int n = 10;
	double dnum = n;
	System.out.println(dnum);
	
	double dnum2 = 20;
	int n2 = dnum2; <- 오류발생
	int n2 = (int)dnum2;
	
	System.out.println(n2);
	}
}
```
정수와 실수는 컴퓨터 내부에서 표현하는 방식이 전혀 다르다.   
따라서 정수와 실수를 더하는 상황이 오면 둘의 자료형을 동일하게 통일 한 후 연산을 해야한다.
<br>
# 묵시적 형 변환
<em>바이트 크기가 작은 자료형에서 큰 자료형으로 대입하는 경우</em>
<br>
<br>

[ ChangeType_1 Code ]
```java
int n = 10;
double dnum = n;
System.out.println(dnum);
```

실행 값
<pre>10</pre>   
<br>
<br>
<br>

[ ChangeType_2 Code ]
```java
double dnum2 = 20;
int n2 = dnum2; <- 오류발생
```
실행 값
<pre>에러발생</pre>
 
위 코드는 8byte 인 Double형인 dnum2를 4byte 인 Int 형인 num2 에 대입하려고 한다.   
이 과정에서 byte 의 용량이 더 큰 Double이 자료손실이 발생할 수 있으므로   에러가 발생하게 된다.   
반대로 4byte 인 Int 형이 8byte 인 double 형에 대입을 하는 [ ChangeType_1 Code ] 같은 코드에는 자료손실이 없다.   
<br>
# 명시적 형 변환
묵시적 형 변환과 반대의 경우  
<br>
<br>
<br>

[ ChangeType_3 Code ]
```java
double dnum2 = 20;
//int n2 = dnum2; <- 오류발생
int n2 = (int)dnum2;
```
실행 값
<pre>20</pre>

위 코드는  <strong>8byte</strong> 인 <strong>Double</strong>형인 dnum2를 <strong>4byte</strong> 인 <strong>Int</strong> 형인 num2 에 대입 하려고 했을 때 자료손실로 인한   
오류로 형변환이 불가능 했다면 

```java
int n2 = (int)dnum2;
```
이 처럼 변환할 자료형을 명시적으로 써 주는것을 강제 형 변환이라고 한다.
