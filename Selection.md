---
type: learn
created: 2025-08-06(수) / 23:42
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-08-06
review_success: false
related_concepts: []
---

## ✅ 선택(Selection)

### 🔤 용어 해석

- Selection: 선택, 분기
- 👉 **조건에 따라 코드 흐름이 갈라지는 구조**를 의미하며, 제어문에서 필수적인 개념

---

### 🧩 선택(Selection)이란?

| 항목            | 설명                                                         |
| ------------- | ---------------------------------------------------------- |
| **정의**        | 특정 조건의 참/거짓 여부에 따라 **다른 코드 블록이 실행되는 구조**                   |
| **구현 방식**     | [[if-else]], [[switch-case]], 삼항 연산자 등                     |
| **프로그램 내 역할** | 조건 분기 처리, 유연한 흐름 제어                                        |
| **위치**        | [[Control Structure]]의 하나로, 반복(loop), 순차(sequence)와 함께 구성됨 |
| **종류**        | 단일 선택, 이중 선택, 다중 선택 등                                      |

---

### 🧱 구조 및 예시

#### 1. 단일 선택 구조 (if문)

```python
if score >= 90:
    print("A학점")
````

#### 2. 이중 선택 구조 (if-else)

```c
if (score >= 90)
    printf("A학점");
else
    printf("B학점 이하");
```

#### 3. 다중 선택 구조 (if-elif-else 또는 switch-case)

```java
switch(grade) {
    case 'A': System.out.println("Excellent"); break;
    case 'B': System.out.println("Good"); break;
    default: System.out.println("Retry");
}
```

#### 4. 삼항 연산자 (조건 ? 참 : 거짓)

```javascript
let result = (age >= 18) ? "성인" : "미성년자";
```

---

### ✅ 특징 요약

- 프로그램의 흐름을 **조건에 따라 분기**
    
- 선택 구조는 **논리 판단**을 기반으로 동작
    
- 다양한 언어에서 if, switch 등을 통해 지원됨
    

---

### 🛠 실무 팁

- 단순한 조건은 삼항 연산자로 축약 가능하지만, **가독성 우선**
    
- 다중 조건일수록 switch 문 또는 if-else 체계적으로 정리 필요
    

---

### 🔗 관련 개념 비교

|개념|설명|
|---|---|
|[[Sequence|순차(Sequence)]]|
|선택(Selection)|조건에 따라 실행 흐름이 나뉨|
|[[Loop|반복(Loop)]]|