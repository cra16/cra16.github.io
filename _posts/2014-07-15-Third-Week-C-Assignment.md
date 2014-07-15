---
layout: post
title: 3주차 C 언어 과제
tags: C
---

## 스무고개

### Level 1

> 컴퓨터가 0 - 99 사이의 숫자를 결정한다. 사람이 답을 입력할 때, 컴퓨터는 '정답보다 크다, 작다, 일치' 3가지 대답을 할 수 있다. 사람이 맞출 수 있는 기회는 20번이다.

#### 이걸 어떻게 짤까?

0 - 99 임의의 숫자 결정: ```x = rand() % 100;```

컴퓨터의 대답: 정답과 입력 값을 비교(if, case 등)

20번의 기회: 반복문 사용(for, while, do while 등)

#### Flowchart

![](/images/twenty-hill.png)

### Level 2

> 사람이 문제를 내고, 컴퓨터가 맞춰라!

컴퓨터는 이진탐색(Binary search) 알고리즘을 사용해서 문제를 맞출 수 있다.

#### 이진탐색 알고리즘

	initially, left = 0, right = n - 1 // (n은 총 길이)
	middle = (left + right) / 2
	compare middle with x

	case1: x < middle, set right = middle - 1
	case2: x == middle, return middle
	case3: x > middle, set left = middle + 1

> 자세한 내용은 구글 검색!

### 가위 바위 보





### 구구단을 외자


이번 과제에서는 특수문자(Escape Character)의 활용과 ```printf()``` 함수의 서식 지정 활용법을 연습해본다.

{% gist wbqd/a610b8839eb5d1140406 %}

위 소스 코드를 토대로 다음과 같은 결과를 출력하는 프로그램을 작성해라. ```printf()``` 함수 8개의 빈칸을 채우면 된다.

![Alt text](/images/assignment-2-result.png)

#### 주의 사항

- 다른 부분은 수정하지 말 것.

- 스페이스로 빈칸을 띄우지 말 것.

- Value 열의 값은 %d 등을 사용해서 표시 것.

- Sizeof() 열의 값은 해당 함수를 사용할 것.