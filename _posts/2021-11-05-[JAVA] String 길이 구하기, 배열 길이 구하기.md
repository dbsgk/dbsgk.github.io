---
layout: single
title: "[Java] String 길이 구하기, 배열 길이 구하기"
---

프로그래머스 문제를 푸는데 생각지도 못한 부분에서 에러가 떴다.

```java
String str = "A";
...
str.charAt(str.length-1);
```

str.length 부분이었다. 

요즘 JavaScript만 써서 length구하는 법도 까먹어서 정리하게 됐다.

## 1. 배열 길이 구하는 법: length

return array.length;

```java
char[] array = ['A','B','C','D','E'];
System.out.println(array.length); // 5
```

## 2. String(문자열) 길이 구하는 법: length()

```java
String str = "ABCDEFG";
System.out.println(str.length()); // 7
```

## 3. [컬렉션](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/util/Collection.html) 타입 길이(크기) 구하는 법: size()

```java
// NoteDTO dto
...
List<NoteDTO> list = noteService.getList(dto) ;
System.out.println(list.size());
```

### 🚫Wrapper Class.size는 비트수 반환하는 메소드

:길이 구하는 메소드가 아니라 비트수 반환하는 메소드니 주의!

![image](https://user-images.githubusercontent.com/58998646/140760199-f7ab28b4-3971-4f4e-9282-6498969c297c.png)
