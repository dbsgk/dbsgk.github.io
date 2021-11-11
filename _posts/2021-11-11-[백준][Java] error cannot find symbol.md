---
layout: single
title: "[백준][Java] error:cannot find symbol"
---

`Main.java:3: error: cannot find symbol`

10869: 입력을 받아서 연산하는 예제에서 에러가 났다.

![image](https://user-images.githubusercontent.com/58998646/140908159-d2d42384-a725-4bff-871c-b8587acf8fd1.png)

이유는 Scanner를 import안해줘서.

```java
// 상단에 Scanner를 import해줘야 한다.
import java.util.Scanner;

public class Main {
	public static void main(String arsg[]) {
		Scanner sc = new Scanner(System.in);
		int a, b;
		a = sc.nextInt();
		b = sc.nextInt();
		System.out.println(a + b);
		System.out.println(a - b);
		System.out.println(a * b);
		System.out.println(a / b);
		System.out.println(a % b);
		
	}
}
```