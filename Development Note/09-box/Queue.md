---
type: learn
created: 2025-07-22(화) / 22:48
topic: ""
category: backend
summary: ""
tags: 
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-07-22
review_success: false
related_concepts:
---
### 🔹 큐(Queue)

**큐(Queue)**는 **먼저 들어온 데이터가 먼저 나가는 구조(FIFO: First-In First-Out)**를 가지는 자료구조다.

---

### ✅ 특징

- **선입선출(FIFO)** 구조
    
- **입력(삽입)**: 뒤에서 넣음 (`enqueue`)
    
- **출력(삭제)**: 앞에서 꺼냄 (`dequeue`)
    

---

### ✅ 주요 연산

|연산|설명|
|---|---|
|`enqueue()`|데이터를 큐의 뒤쪽(Rear)에 삽입|
|`dequeue()`|데이터를 큐의 앞쪽(Front)에서 삭제|
|`peek()`|가장 앞에 있는 요소를 반환 (삭제 X)|
|`isEmpty()`|큐가 비었는지 확인|
|`isFull()`|(고정 크기 큐일 경우) 꽉 찼는지 확인|

---

### ✅ 구현 방식

- **배열 기반**: 인덱스 증가로 구현 가능. 단, 삭제 시 `shift()`로 인해 성능 저하 가능
    
- **연결 리스트 기반**: 앞, 뒤 노드를 가리키는 방식으로 효율적
    
- **원형 큐(Circular Queue)**: 고정 크기 큐에서 인덱스를 순환시켜 공간 낭비 방지
    

---

### ✅ 예시

```python
# 파이썬 큐 간단 예시
from collections import deque

queue = deque()
queue.append('A')  # enqueue
queue.append('B')
print(queue.popleft())  # dequeue → A
print(queue)            # ['B']
```

---

### ✅ 사용 예시

- **프린터 대기열**
    
- **CPU 작업 스케줄링**
    
- **네트워크 패킷 처리**
    
- **BFS (너비 우선 탐색)**
    

---

### 🔸 스택 vs 큐

| 구조  | [[Stack\|스택(Stack)]] | 큐(Queue)  |
| --- | -------------------- | --------- |
| 구조  | LIFO                 | FIFO      |
| 삽입  | top                  | rear (뒤)  |
| 삭제  | top                  | front (앞) |

큐는 데이터가 **순차적으로 처리되어야 하는 경우**에 적합한 자료구조다.