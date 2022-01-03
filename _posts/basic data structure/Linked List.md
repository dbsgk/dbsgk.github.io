## Linked List
각 노드가 데이터와 포인터를 가지고 한 줄로 연결되어 있는 방식의 자료구조이다.
데이터를 담고 있는 노드들이 연결되어 있고, 노드의 포인터가 이전 노드와 다음 노드와의 연결을 담당한다.


장점: 리스트 길이가 가변적. 배열의 단점을 커버. 중간에 데이터를 추가/삭제해도 전체 인덱스가 한 칸씩 밀리거나 당겨지는 일 없이 앞뒤 링크만 변경되고 나머지는 변경되지 않는다.
(ArrayList에 비해 데이터 추가/삭제 용이)


단점: 인덱스가 없기에 특정 요소에 접근하기 위해선 순차 탐색이 필요(=탐색 속도가 떨어진다).

-> 데이터가 자주 추가되거나 삭제되면 링크드리스트 사용.
(데이터 탐색, 정렬을 자주 한다면 배열을 사용)


#### LinkedList 값 검색
```java

import java.util.Arrays;
import java.util.LinkedList;

public class Test {
    public static void main(String[] args) {
        LinkedList<Integer> list = new LinkedList<Integer>(Arrays.asList(1,2,3));
        System.out.println(list.contains(1)); //list에 1이 있는지 검색 : true
        System.out.println(list.indexOf(1)); //1이 있는 index반환 없으면 -1
    }
}

```
