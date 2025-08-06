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

## ✅ 반복(Iteration)

### 🔤 용어 해석

- Iteration: 반복, 순환  
- 👉 **조건이 참일 동안 또는 정해진 횟수만큼 코드 블록을 반복 실행**하는 제어 구조

---

### 🧩 반복(Iteration)이란?

| 항목 | 설명 |
|------|------|
| **정의** | 동일한 명령문을 조건이 참인 동안 반복적으로 실행하는 구조 |
| **유형** | 조건 기반 반복(`while`, `do-while`), 횟수 기반 반복(`for`) |
| **제어문 종류** | `for`, `while`, `do-while`, `foreach`, `range` 등 |
| **활용 목적** | 일정 조건을 만족할 때까지 같은 작업을 반복 수행 |
| **중단/건너뛰기** | `break`, `continue` 문 등으로 흐름 제어 가능 |

---

### 🧱 구조 및 예시

#### 1. 횟수 기반 반복 (`for`)

```python
for i in range(5):
    print(i)  # 0부터 4까지 출력
````

#### 2. 조건 기반 반복 (`while`)

```c
int i = 0;
while (i < 5) {
    printf("%d\n", i);
    i++;
}
```

#### 3. 조건 후 검사 (`do-while`)

```java
int i = 0;
do {
    System.out.println(i);
    i++;
} while (i < 5);
```

---

### ✅ 특징 요약

- 반복 제어는 **조건 기반 또는 횟수 기반**으로 나뉨
    
- 반복문 내부에서 흐름 제어문(`break`, `continue`)으로 유연한 흐름 구성 가능
    
- [[Selection]]과 함께 자주 사용됨 (ex. 반복 도중 조건 판단)
    

---

### 🛠 실무 팁

- 반복 횟수가 명확할 경우 `for`, 불확실할 경우 `while` 사용
    
- 무한 루프를 피하기 위해 종료 조건 명확히 설정
    
- 컬렉션 순회에는 `foreach`, `for in`, `for of` 등 사용 권장
    

---

### 🔗 관련 개념 비교

|개념|설명|
|---|---|
|[[Sequence]]|명령이 위에서 아래로 순차 실행됨|
|[[Selection]]|조건에 따라 흐름이 분기됨|
|[[Iteration]]|특정 조건/횟수에 따라 명령을 반복 실행함|