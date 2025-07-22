---
type: learn
created: 2025-07-22(화) / 22:49
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-07-22
review_success: false
related_concepts: []
---
### 🔹 스택(Stack)

**스택**은 **나중에 들어온 데이터가 먼저 나가는 구조(LIFO: Last-In First-Out)**의 선형 자료구조다.

---

### ✅ 특징

- **후입선출(LIFO)** 구조
    
- **입력(삽입)**: `push()` — 맨 위에 쌓음
    
- **출력(삭제)**: `pop()` — 맨 위에서 꺼냄
    

---

### ✅ 주요 연산

|연산|설명|
|---|---|
|`push()`|데이터를 스택의 맨 위에 삽입|
|`pop()`|스택의 맨 위 요소 제거 및 반환|
|`peek()` or `top()`|맨 위 요소를 반환 (삭제 X)|
|`isEmpty()`|스택이 비어있는지 확인|
|`isFull()`|(고정 크기일 경우) 가득 찼는지 확인|

---

### ✅ 구현 예시 (Python)

```python
stack = []
stack.append('A')  # push
stack.append('B')
print(stack.pop()) # pop → 'B'
print(stack)       # ['A']
```

---

### ✅ 사용 예시

- **함수 호출 스택 (재귀)**
    
- **웹 브라우저 뒤로 가기**
    
- **문자열 괄호 검사**
    
- **DFS(깊이 우선 탐색)**
    
- **수식 계산기 (후위표기법)**
    

---

### 🔸 스택 vs 큐

|항목|스택(Stack)|큐(Queue)|
|---|---|---|
|구조|LIFO (후입선출)|FIFO (선입선출)|
|삽입 위치|top (위)|rear (뒤)|
|삭제 위치|top (위)|front (앞)|

스택은 **최근 작업부터 되돌아가야 하는 상황**에 최적화된 자료구조다.