# 참조 자료형
참조 자료형이란, 크기가 정해진 기본자료형 ( int , char , float , double 등 )으로 선언하는 변수가 있고  
클래스 자료형으로 선언하는 참조자료형이 있다.  
---
1) 기본자료형 (Primitive Data Type)
<pre>데이터를 저장하기 위해 사용되는 자료형을 의미하며 변수에 <b>"실제 값"</b>을 가지는것을 의미</pre>

2) 참조자료형 (Reference Data Type)
<pre>실제 값을 갖는것이 아닌 데이터의 저장된 메모리의 <b>"주소 값"</b>을 가지는 자료형이다.  
해당 값은 객체를 참조하는 변수타입을 의미합니다.</pre>

# 참조자료형의 종류
1. String     : 문자열을 저장하는 데 사용되는 클래스  
2. ArrayList  : 동적 배열을 나타내는 클래스  
3. HashMap    : 키 - 값 쌍을 저장하는 데 사용되는 클래스  
4. HashSet    : 고유한 요소를 저장하는 데 사용되는 클래스  
5. LinkedList : 연결 리스트를 나타내는 클래스  
6. Queue      : 큐를 나타내는 인터페이스  
7. Stack      : 스택을 나타내는 클래스  


# 참조자료형 예시
<br><br>
[ ReferenceDateType.java ]<br>
```java
Class Person{
  String name;
  int age;
}

Person person1 = new Person();
person1.name = "john";
person1.age = 25;
```

위 코드는 Person 이란 클래스를 만들고 이 클래스는 다른 곳에서 new 연산자를 사용하여 person1 변수를 생성했다.   
Person 클래스를 참조하고 있는 person1 변수를 참조 자료형이라고 합니다.
