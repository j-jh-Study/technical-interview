4개의 공통점은 컬렉션 프레임워크로 묶일수 있는데 각각의 차이는

List는 인스턴스의 저장순서를 유지 , 동일한 인스턴스의 중복 저장을 허용
List의 경우에는 양방향 반복자 사용이가능! by ListIterator<E>
<details><summary>자바에서 list는 뭘로 구현됨?+순차적접근</summary>
<p>

- ArrayList : 배열기반 자료구조 -> 값이 추가되면 새롭게 크기를 다시짜야함
- LinkedList : 리스트 기반 자료구조

-Iterable을 구현하기때문 ... 정확히는 Collection이 Iterable을 상속
따라서 정확한 구조는
```java
 public interface Collection<E> extends Iterable<E>

```

iterable 메소드 사용의 장점 .. for -each 대비
조회 중간에 특정 인스턴스 삭제가 가능하다 ..! 

사실은 for-each문은 컴파일과정에서 반복자를 이용하는 코드로 수정됨

```java
for(String s : list)

for(Iterator<String> itr = list.iterator(); itr.hasNext(); )

```

</p>
</details> 


Set 의경우
- 저장 순서가 유지x
- 데이터의 중복 저장 허용x .. 값이 동일한가보다는 인스턴스가 동일한가.!!

<details><summary>동일인스턴스판단기준</summary>
<p>
Object 클래스에 정의 되어있는 두 메소드의  호출 결과를 근거로
- public boolean equals(Object obj)
- public int hashCode() 
-  적절하게 오버라이딩해서 사용하면 값을 기준으로 바꿀수도 있다 ex)String 


</p>
</details> 

Map 의경우
- key,Value 가 한쌍을 이루는 형태
- key 값은 중복허용 x 
- 컬렉션은 다 Value를 저장한다면 여기는 Value를 저장하고 찾을때 key를 사용함
- 이러한 Map 자료형을 구현하는 클래스 중 하나가 HashMap
- Hash 알고리즘 기반이 HashMap..!

[Hash와 HashMap 상세내용](https://d2.naver.com/helloworld/831311)
<details><summary>map의 순차적 조회</summary>
<p>
hashmap은 Iterable 인터페이스를 구현하지 않았기때문 반복자를 사용 x

그래서 나온 메소드
```java
 public Set<K> keySet()
```
set자료형으로 키값을 모아오는것 .. 그럼 set이니까 lterable 상속중이니 반복자 사용가능


</p>
</details> 
