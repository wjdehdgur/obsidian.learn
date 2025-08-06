---
type: learn
created: 2025-08-06(수) / 20:46
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
## ✅ 정렬 알고리즘(Sorting Algorithm)

### 🔤 용어 해석

- Sorting: 순서대로 정렬  
- 👉 [[Sorting Algorithm|정렬 알고리즘]]은 **데이터를 특정 기준에 따라 순서대로 나열하기 위한 알고리즘**

---

### 🧩 정렬 알고리즘이란?

| 항목 | 설명 |
|------|------|
| **정의** | [[Sorting Algorithm]]은 리스트나 배열에 있는 데이터를 **오름차순 또는 내림차순 등 일정한 순서대로 정렬하는 알고리즘**을 의미한다. |
| **목적** | 검색 성능 향상, 데이터 처리 간소화, 사용자 가독성 확보 |
| **종류** | 내부 정렬, 외부 정렬 / 비교 기반, 비비교 기반 정렬 등 |
| **판단 기준** | 시간 복잡도, 공간 복잡도, 안정성(Stable), 정렬 방식 등 |

---

### 🧠 대표 알고리즘 비교

| 알고리즘 | 시간 복잡도 (평균) | 안정 정렬 | 특징 |
|----------|---------------------|------------|------|
| [[Bubble Sort]] | O(n²) | ✅ | 인접한 요소 반복 비교, 느리지만 구조 단순 |
| [[Insertion Sort]] | O(n²) | ✅ | 거의 정렬된 배열에 효율적 |
| [[Merge Sort]] | O(n log n) | ✅ | 분할 정복 기반, 추가 메모리 필요 |
| [[Quick Sort]] | O(n log n) | ❌ | 피벗 기반, 평균 빠름, 최악 O(n²) |
| [[Heap Sort]] | O(n log n) | ❌ | 완전 이진트리 기반, 공간 효율적 |

---

### 💡 실무 팁

- 데이터가 거의 정렬되어 있을 경우 → [[Insertion Sort]] 추천  
- 메모리 여유 있고 안정 정렬이 필요한 경우 → [[Merge Sort]]  
- 속도 우선, 메모리 제한이 있는 경우 → [[Quick Sort]] or [[Heap Sort]]  
- 실제 환경에서는 [[Timsort]] (Merge + Insertion 혼합) 사용됨

---

### 🔗 관련 개념 비교

| 개념 | 설명 |
|------|------|
| [[Sorting Algorithm]] | 데이터를 정해진 순서로 배열 |
| [[Stable Sort]] | 동일한 값의 상대적 순서를 유지 |
| [[Divide and Conquer]] | Merge/Quick Sort 등에서 사용되는 전략 |
| [[Time Complexity]] | 알고리즘 성능 분석 기준 |
| [[Comparison Sort]] | 요소 간 크기를 비교하는 정렬 방식 |
