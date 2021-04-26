# Map과 List의 차이

Map과 List의 공통점은 데이터를 저장하는 자료구조 인 점입니다.

똑같이 데이터를 저장하지만, 데이터를 저장하는 구조는 다릅니다.

## List

List는 메모리안의 특정한 동일 공간에 뭉텅이로 저장됩니다.

내부구현은 배열로 돼있기 때문입니다. 

그래서 알맞는 데이터 저장공간만 있다면 데이터 저장속도는 빠릅니다.

또한, 순차적으로 데이터를 저장하므로, 

데이터 특징이 포지션별로 의미가 있을 때 사용하는 것이 좋습니다.

아래는 자바로 작성한 예시입니다.

List와 Map의 프로그래밍적으로 개념은 같기때문에 어떤 언어든간에

똑같이 이해하면 됩니다.

```java
**ArrayList<String> arrayList = new ArrayList<>();

arrayList.add("0번 아이템 입니다.");
arrayList.add("1번 아이템 입니다.");
arrayList.add("2번 아이템 입니다.");
arrayList.add("3번 아이템 입니다.");
arrayList.add("4번 아이템 입니다.");
arrayList.add("5번 아이템 입니다.");

int index = 0;
for(String tempItem : arrayList){
System.out.println((index++)+"번 : " + tempItem);
}

-------------------Consol---------------------------

0번 : 0번 아이템 입니다.
1번 : 1번 아이템 입니다.
2번 : 2번 아이템 입니다.
3번 : 3번 아이템 입니다.
4번 : 4번 아이템 입니다.
0번 : 5번 아이템 입니다.**
```

foreach문을 썼지만 , 일반 for문으로 arrayList.get(position); 메서드를 써도 무방합니다.

데이터가 6개 필요하므로 배열의 크기가 6을 충족하는 메모리 공간만 있으면

그곳에 배열자체를 저장합니다. (JDK 1.7 아래 버전은 디폴트 배열 크기가 10입니다.)

consol 출력처럼 포지션별로 의미가 있을때 유리합니다.

예를 들어 쇼핑몰 페이지에서  쇼핑몰 아이템들을 화면에 나열 한다고 생각해봅시다.

단순히 저장된 아이템 전부를 화면에 나열할 필요가 있으므로,

순차적으로 저장된 데이터를 순차적으로 화면에 배치시키면 되는 것 입니다.

이러한 경우는 ArrayList가 좋습니다. 

하지만, ArrayList안에 있는 데이터를 삽입/삭제가 빈번할때, 비효율적인 경우가 있습니다.

추가는 단순히 ArrayList 내부 배열의 크기를 바꾸고 기존 배열의 데이터를 추가하는데 그치지만,

원하는 포지션(인덱스)의 삽입/삭제는 이야기가 다릅니다.

삽입/ 삭제는 해당 포지션 아래의 데이터들을 Copy 해야합니다. 

(새로운 배열을 만든후, 기존 배열의 값을 포지션별로 다시 채워야합니다.)

기존 배열의 크기를 늘린후 삽입/삭제 데이터를 처리하고 Copy된 데이터를 다시 붙입니다.

따라서 ArrayList의 size가 큰 경우는 많은 양의 요소들을 Copy해야 하므로 내부적으로 성능이

떨어질 수 있는 것입니다.

정리하자면, ArrayList는 아이템의 빈번한 변경 없이,

데이터를 순차적으로 받고, 특정 데이터가 아닌 원하는 데이터 범위를 순차적으로 표현할때 유리한 자료구조라 볼 수 있습니다.

## Map

Map을 이용해 저장할때는 List처럼

뭉텅이로 저장하는것이 아니라, Map에 아이템을 저장할때마다, 빈 공간을 찾아 저장합니다.

따라서 List보다는 데이터 저장속도가 느릴 수 있습니다.  Map의 가장 큰 특징이라면,

쌍을이루는 Key와 Value값을 이용한다는 것입니다.

따라서 단순한 포지션(0~10 같은 인덱션)보다는, 저장하고 싶은 데이터가 특별한 Key값을

가질때 Map을 사용하는것이 좋다. 아래의 예시는 자바언어로 작성하였습니다.

```java
HashMap<String,String> hashMap = new HashMap<>();
hashMap.put("Key1" , " 키값이 Key1인 Value 입니다. ");
hashMap.put("Key2" , " 키값이 Key2인 Value 입니다. ");
hashMap.put("Key3" , " 키값이 Key3인 Value 입니다. ");
hashMap.put("Key4" , " 키값이 Key4인 Value 입니다. ");

System.out.println(hashMap.get("key1");
System.out.println(hashMap.get("key2");
System.out.println(hashMap.get("key3");
System.out.println(hashMap.get("key4");

------------- consol -----------------

키값이 Key1인 Value 입니다.
키값이 Key2인 Value 입니다.
키값이 Key3인 Value 입니다.
키값이 Key4인 Value 입니다.
```

위의 예시는 key값을 String으로 데이터도 String으로 작성하였습니다.

만약 동일한 Key값을 사용하면 기존의 Key값을 가지고 있는 value가 사라지고

후에 저장한 value 값이 셋팅이 됩니다. 

Key만 다르다면 value 값이 중복되도 상관 없습니다.

Map은 콘솔에 찍힌거와 같이 키값이 의미가 있을때 좋은 자료구조 입니다.

ArrayList안에 원하는 데이터를 검색하는 경우에는 0번부터 해당 데이터가 있을때까지

검색을 해야하지만, (원하는 데이터의 index를 모르는 경우) hashMap의 경우는

Key값을 통해서 빠르게 데이터를 검색합니다.

요소의 추가 삭제는 List보다 성능이 나을때가 많습니다. 

따라서, 검색성능은 기본적으로 Map이 좋습니다.

정리하자면,  Map 은빈번한 검색과, 범위데이터가 아닌 특정 데이터를 순간마다 캐치해야할 때 유리한 자료구조입니다.

출처: 

[List와 Map의 차이 (1)](https://mommoo.tistory.com/33)