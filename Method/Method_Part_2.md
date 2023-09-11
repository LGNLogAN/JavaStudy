# 메서드

## Method_Part_1 을 보고 간단한 만든 프로그램



[ 평균 구하기 프로그램 ]

```java
public class Method_Part_2 {
	public static int subjectAvg(int subjectint , int korean , int math , int english) {
		int total = 0;
		total += korean;
		total += math;
		total += english;
		total/=subjectint;
		
		return total;
}
	
	public static void main(String[] args) {
		System.out.println(subjectAvg(3,100,80,90));
	}

}
```

<pre>
실행 값 >
90
</pre>

int 형을 반환해주는 subjectAvg 의 메서드 생성했다. 매개변수에는 과목의 개수 , 국어점수 , 수학점수 , 영어점수를  입력받을 수 있게 했습니다. 
total 변수에 3개의 과목점수를 다 더한 후 subjectint 매개변수를 통해 나눠서 평균을 구할 수 있습니다.
