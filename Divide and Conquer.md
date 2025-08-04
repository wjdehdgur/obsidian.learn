---
type: learn
created: 2025-08-05(화) / 00:46
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-08-05
review_success: false
related_concepts: []
---
## ✅ 분할 정복(Divide and Conquer)

### 🔤 용어 해석

- Divide: 나누다  
- Conquer: 정복하다  
- 👉 [[Divide and Conquer|분할 정복]]은 **문제를 더 작은 하위 문제로 분할하고, 각각을 해결한 뒤 결과를 결합하는 알고리즘 설계 전략**

---

### 🧩 분할 정복이란?

| 항목        | 설명                                                                                                                                                                                      |
| --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **정의**    | [[Divide and Conquer]]는 복잡한 문제를 **더 작고 유사한 문제로 나누어 해결**하고, 그 해답을 결합하여 전체 문제를 해결하는 방식이다.                                                                                                 |
| **단계**    | ① Divide: 문제를 작게 나눈다  <br>② Conquer: 나눠진 문제를 재귀적으로 푼다  <br>③ Combine: 부분 해를 모아 전체 해로 만든다                                                                                                |
| **적용 예시** | - [[Quick Sort]]  <br>- [[Merge Sort]]  <br>- [[Binary Search]]  <br>- [[Closest Pair of Points]]  <br>- [[Karatsuba Algorithm]] (빠른 곱셈)  <br>- [[Strassen's Matrix Multiplication]] \| |


---

### 📌 주요 예시

#### ✅ 예시 1: 퀵 정렬 (Quick Sort)
- **Divide**: 피벗을 기준으로 좌/우 그룹으로 나눔  
- **Conquer**: 각 그룹에 대해 재귀적으로 퀵 정렬  
- **Combine**: 좌측 + 피벗 + 우측을 합침 (암시적으로)

#### ✅ 예시 2: 병합 정렬 (Merge Sort)
- **Divide**: 배열을 절반으로 나눔  
- **Conquer**: 나뉜 배열을 각각 정렬  
- **Combine**: 두 정렬된 배열을 병합

#### ✅ 예시 3: 이진 탐색 (Binary Search)
- **Divide**: 중간 인덱스를 기준으로 절반으로 나눔  
- **Conquer**: 원하는 값이 있는 쪽만 탐색  
- **Combine**: 해당 값의 인덱스를 리턴 (결합은 필요 없음)

---

### 💡 실무 팁

- 병렬 처리에 유리한 구조 (서로 독립적인 하위 문제)  
- 재귀 깊이 관리 필요 → Tail Recursion, 반복문으로 변환 가능  
- `Divide`가 단순하고 `Combine`이 빠를수록 성능이 좋음

---

### 🔗 관련 개념 비교

| 개념 | 설명 |
|------|------|
| [[Divide and Conquer]] | 문제를 나누고 해결 후 합치는 전략 |
| [[Dynamic Programming]] | 하위 문제 결과를 저장하여 중복 계산 제거 |
| [[Greedy Algorithm]] | 매 단계에서 최적 선택으로 전체 최적 해 추구 |
| [[Recursive Function]] | 분할 정복 구현의 기본 도구 |
| [[Parallel Algorithm]] | 분할된 하위 문제를 동시에 처리하는 방식 |
