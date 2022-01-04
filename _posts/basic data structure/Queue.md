## Queue
줄을 지어 순서대로 처리되는, 먼저 들어간 자료가 먼저 나오는 FIFO(First In First Out) 자료구조 형태.
- front(프론트): 큐의 맨 앞 쪽. 삭제 연산만 수행함.
- rear(리어): 큐의 맨 뒤 쪽. 삽입 연산만 수행함.  
- empty(공백): 큐에 요소가 하나도 들어있지 않은 상태.
- full(포화): 큐가 꽉 차서 더이상 요소를 집어넣지 못하는 상태.



                                [1 2 3 4] <- 5(Enqueue)    
                 1(Dequeue)  <- [2 3 4 5]
  
  
Enqueue: 큐 맨 뒤에 데이터 추가. 큐가 포화(full) 상태인지 확인해야 함.

Dequeue: 큐 맨 앞쪽의 데이터 삭제. 큐가 공백(empty) 상태인지 확인해야 함.

### 큐의 특징
- 그래프의 넓이 우선 탐색(BFS)에서 사용.
- 컴퓨터 버퍼에서 주로 사용. 버퍼(큐)를 만들어 대기 시킴.



### 큐 사용법

#### 메소드별 차이점
| 문제 상황에서 | 예외 발생 | 값 리턴 |
| --- | --- | --- |
| 추가(Enqueue) | add(e) | offer(e) |
| 삭제(Dequeue) | remove() | poll() |
| 검사(peek) | element() | peek() |

```java

import java.util.LinkedList;
import java.util.Queue;

public class Test {
    public static void main(String[] args) {
        Queue<Integer> queue = new LinkedList<>(); //int형 queue 선언, linkedlist 이용
        queue.add(1);       // queue에 값 1 추가. 큐가 꽉 찼다면 예외 발생.
        queue.offer(3);     // queue에 값 3 추가. 큐가 꽉 찼다면 false 반환.

        queue.remove();     // queue의 첫번째 값 제거. 비어있다면 예외 발생.
        queue.poll();       // queue의 첫번째 값을 반환하고 제거. 비어있다면 null

        queue.element();    // queue의 첫번째 값을 반환. 비어있다면 예외 발생.
        queue.peek();       //queue의 첫번째 값을 반환. 비어있다면 null
        
        queue.clear();      // queue 초기화

    }
}


```
