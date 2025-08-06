---
type: learn
created: 2025-08-06(수) / 20:48
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

## ✅ 병합 정렬(Merge Sort)

### 🔤 용어 해석

- Merge: 병합, 합치다  
- 👉 [[Merge Sort|병합 정렬]]은 **리스트를 분할한 뒤 정렬하며 병합하는 [[Divide and Conquer|분할 정복]] 기반의 정렬 알고리즘**

---

### 🧩 병합 정렬이란?

| 항목         | 설명                                                                                  |
| ---------- | ----------------------------------------------------------------------------------- |
| **정의**     | [[Merge Sort]]는 리스트를 절반씩 나누어 각각을 재귀적으로 정렬하고, **정렬된 리스트들을 병합하여 전체 정렬을 완성하는 알고리즘**이다. |
| **정렬 방식**  | 리스트 분할 → 각 부분 정렬 → 정렬된 리스트 병합                                                       |
| **핵심 전략**  | [[Divide and Conquer]] (분할 → 정복 → 병합)                                               |
| **시간 복잡도** | 최선/평균/최악 모두 O(n log n)                                                              |
| **공간 복잡도** | O(n) — 추가 메모리 필요                                                                    |
| **정렬 안정성** | ✅ **안정 정렬(Stable Sort)**                                                            |

---

### 🧪 예시: 병합 정렬(Merge Sort) – [5, 3, 8, 4, 2]

병합 정렬은 **배열을 반으로 쪼개서 정렬한 뒤**, 두 개의 정렬된 배열을 **병합(Merge)** 하는 **분할 정복(Divide and Conquer)** 기반 알고리즘이야.

---

## ✅ 단계별 수행

---

### 📌 Step 1: 분할 (Divide)

원래 배열:  
[5, 3, 8, 4, 2]

1차 분할 →  
[5, 3] / [8, 4, 2]

2차 분할 →  
[5] [3] / [8] [4, 2]

3차 분할 →  
[4] [2]

---

### 📌 Step 2: 정렬된 상태로 병합 (Merge)

- [5], [3] → [3, 5]
    
- [4], [2] → [2, 4]
    
- [2, 4], [8] → [2, 4, 8]
    

---

### 📌 Step 3: 전체 병합

- [3, 5], [2, 4, 8] 병합  
    → 작은 수부터 비교하여 하나씩 배열에 넣음
    

➡️ 최종 결과: [2, 3, 4, 5, 8]

---

## 🧠 요약

|항목|설명|
|---|---|
|방법|반으로 나눈 뒤 정렬하며 병합|
|특징|**안정 정렬**, **재귀 기반**, **추가 메모리 필요**|
|시간 복잡도|`O(n log n)` 항상 일정함|
|공간 복잡도|`O(n)` (병합 시 임시 배열 필요)|

---

### 💻 코드 예시 (Python)

```python
def merge_sort(arr):
    if len(arr) <= 1:
        return arr
    mid = len(arr) // 2
    left  = merge_sort(arr[:mid])
    right = merge_sort(arr[mid:])
    return merge(left, right)

def merge(left, right):
    result = []
    i = j = 0
    while i < len(left) and j < len(right):
        if left[i] <= right[j]:
            result.append(left[i])
            i += 1
        else:
            result.append(right[j])
            j += 1
    result += left[i:]
    result += right[j:]
    return result
````

---

### 💡 실무 팁

- **입력 크기가 클수록 안정적 성능 발휘**
    
- 메모리 사용을 줄인 **in-place merge sort**는 복잡도 증가
    
- [[Timsort]] 내부에도 병합 정렬의 원리가 사용됨
    
- 안정 정렬이 필요한 금융/회계 시스템에서 유리
    

---

### 🔗 관련 개념 비교

|개념|설명|
|---|---|
|[[Merge Sort]]|분할 → 정복 → 병합, 안정적이고 예측 가능한 성능|
|[[Quick Sort]]|피벗 기반 분할, 평균 빠르지만 불안정|
|[[Heap Sort]]|완전 이진트리 기반, 공간 효율적|
|[[Bubble Sort]]|느리지만 구조가 단순한 정렬|
|[[Divide and Conquer]]|문제를 분할해 해결하는 알고리즘 전략|