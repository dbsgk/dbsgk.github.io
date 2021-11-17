---
layout: single
title: "[JavaScript] 객체 참조값 비교하기"
---

## 객체 참조값 비교:  obj1 === obj2

```jsx
var obj1 = {
	p:1,
	sz:10
}
var obj2 = obj1;
console.log('obj1 === obj2 : '+ obj1 === obj2) // true
```

### 🚫 자바스크립트는 메모리값을 출력해볼 수 없음. 참조값 비교로 확인만 가능.