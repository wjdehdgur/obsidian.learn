---
type: learn
created: 2025-08-06(수) / 20:50
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

## ✅ 선택 정렬(Selection Sort)

### 🔤 용어 해석

- Selection: 선택, 고르기  
- 👉 [[Selection Sort|선택 정렬]]은 **가장 작은(또는 큰) 값을 선택하여 맨 앞부터 하나씩 자리를 정해주는 정렬 알고리즘**

---

### 🧩 선택 정렬이란?

| 항목 | 설명 |
|------|------|
| **정의** | [[Selection Sort]]는 주어진 리스트에서 **가장 작은 값을 찾아 맨 앞과 교환**하는 방식으로 정렬을 반복하는 알고리즘이다. |
| **정렬 방식** | ① 가장 작은 값 선택 → ② 현재 위치와 교환 → ③ 다음 인덱스로 반복 |
| **특징** | 비교 횟수는 많지만 교환 횟수는 적음 |
| **시간 복잡도** | 최선/평균/최악 모두 O(n²) |
| **공간 복잡도** | O(1) — 추가 공간 없음 (In-place) |
| **정렬 안정성** | ❌ **불안정 정렬** (같은 값의 순서 유지 안됨)

---

### 💻 코드 예시 (Python)

```python
def selection_sort(arr):
    n = len(arr)
    for i in range(n):
        min_idx = i
        for j in range(i + 1, n):
            if arr[j] < arr[min_idx]:
                min_idx = j
        arr[i], arr[min_idx] = arr[min_idx], arr[i]
    return arr
````

---

### 💡 실무 팁

- **단순하지만 비효율적**이므로 실제 사용은 거의 없음
    
- 교환 횟수가 적어 메모리 접근 비용이 높은 환경에서 유리
    
- [[Bubble Sort]], [[Insertion Sort]]와 함께 학습용으로 사용됨
    

---

### 🔗 관련 개념 비교

|개념|설명|
|---|---|
|[[Selection Sort]]|가장 작은 값을 선택해 앞으로 이동|
|[[Bubble Sort]]|인접 요소를 비교하며 큰 값을 뒤로 보냄|
|[[Insertion Sort]]|정렬된 영역에 삽입하는 방식|
|[[Heap Sort]]|선택 정렬을 힙으로 최적화한 구조|
|[[Stable Sort]]|선택 정렬은 안정 정렬이 아님|