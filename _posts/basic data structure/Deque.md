## Deque (  Double Ended Queue:양 끝이 앞이 되는 큐  )
양쪽 끝에서 삽입과 삭제가 모두 가능한 자료구조로 스택과 큐의 장점만 따서 구성한 것이다.

데크는 어떤 쪽으로 입력하고 어떤 쪽으로 출력하느냐에 따라서 스택으로 사용할수도, 큐로 사용할 수도 있다.

특히, 한 쪽으로만 입력 가능하도록 설정한 덱을 스크롤(scroll)이라고 하며, 한 쪽으로만 출력 가능하도록 설정한 덱을 셸프(shelf)라고 한다.
- front: 데크의 맨 앞 
- last: 데크의 맨 뒤

### 데크 사용법


| 맨 앞에 추가 | 맨 뒤에 추가 |
| --- | --- |
| push(e) | add(e) |
| addFirst(e) | addLast(e) |
| offerFirst(e) | offer(e) |
|  | offerLast(e) |

```java

import java.util.Deque;
import java.util.LinkedList;

public class Test {
    public static void main(String[] args) {
        Deque<String> deque = new LinkedList<String>();

        // 큐를 추가하는 여러가지 방법

        deque.add("큐1 (끝)");          // 끝에 추가
        deque.addFirst("큐2 (처음)");   // 앞에 추가
        deque.addLast("큐3 (끝)");      // 끝에 추가
        deque.push("큐4 (처음)");       // 앞에 추가
        deque.offer("큐5 (끝)");        // 끝에 추가
        deque.offerFirst("큐6 (처음)"); // 앞에 추가

        System.out.println(deque + "\n");
        
        // 데크 값의 삭제는 맨 앞이나 맨 끝에 있는 항목만 삭제 가능하다.
        deque.removeFirst();
        deque.removeLast();
        System.out.println("맨 앞과 맨 뒤 항목을 삭제한 데크" + deque);

//        출력 결과: 
//        [큐6 (처음), 큐4 (처음), 큐2 (처음), 큐1 (끝), 큐3 (끝), 큐5 (끝)]
//
//        맨 앞과 맨 뒤 항목을 삭제한 데크: [큐4 (처음), 큐2 (처음), 큐1 (끝), 큐3 (끝)]
    }
}


```

추천문제: https://www.acmicpc.net/problem/10866
