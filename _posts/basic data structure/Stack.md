## Stack
한 쪽 끝에서만 자료를 넣고 뺄 수 있는 LIFO(Last In First Out) 형식의 자료 구조.


#### 스택의 연산
- pop(): 스택에서 가장 위에 있는 항목을 제거한다.
- push(item): item 하나를 스택의 가장 윗 부분에 추가한다.
- peek(): 스택의 가장 위에 있는 항목을 반환한다.
- isEmpty(): 스택이 비어 있을 때에 true를 반환한다.


#### 스택의 사용 사례
- 재귀적(Recursion) 함수를 호출 할 때 사용.   
- 웹 브라우저 방문기록(뒤로가기)
- 실행 취소(undo)
- 수식의 괄호 검사(연산자 우선순위 표현을 위한 괄호 검사)
    - 올바른 괄호 문자열(VPS, Valid Parenthesis String)판단하기
- 후위 표기법 계산
    - 후위 표기법: AB+ (피연산자를 먼저 표시하고 연산자를 나중에 표시하는 방법). 
    - 참고) 전위 표기법: +AB, 중위 표기법: A+B
- 그래프의 깊이 우선 탐색(DFS)에서 사용.


#### 스택 사용법
```java

import java.util.Stack;

public class Test {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>(); //int형 스택 선언
        stack.push(1);     // stack에 값 1 추가
        stack.push(2);     // stack에 값 2 추가
        stack.push(3);     // stack에 값 3 추가
        stack.contains(1); // stack에 1이 있는지 check (있다면 true)
        stack.search(1); // 1의 위치를 반환 (없으면 -1)
        while (!stack.empty()) { // stack이 비어있는지 check (비어있다면 true)
            stack.peek(); // stack의 가장 상단의 값 출력
            stack.pop();       // stack에 값 제거
        }
        stack.clear();     // stack의 전체 값 제거 (초기화)

    }
}


```
