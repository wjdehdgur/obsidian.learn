---
type: learn
created: 2025-08-18(월) / 23:19
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-08-18
review_success: false
related_concepts: []
---
---

## ✅ 알고리즘 복잡도(Algorithm Complexity)

### 🔤 용어 해석

- Complexity: 복잡도
    
- 👉 알고리즘의 **성능을 수학적으로 분석**하여 입력 크기에 따른 **처리 시간 또는 메모리 사용량**을 측정한 개념
    

---

### 🧩 복잡도란?

|항목|설명|
|---|---|
|**정의**|입력 크기 `n`에 따라 **알고리즘이 얼마나 자원(시간/공간)을 사용하는지** 표현한 지표|
|**목적**|알고리즘의 효율성 비교 및 최적 선택|
|**표현법**|[[빅오 표기법(Big-O Notation)]]|

---

### 🧱 복잡도 종류

|구분|설명|
|---|---|
|시간 복잡도(Time Complexity)|입력 크기에 따른 **연산 횟수 증가량** 측정|
|공간 복잡도(Space Complexity)|입력 크기에 따른 **메모리 사용량 증가량** 측정|

---

### 📚 대표 복잡도 예시

|표기|의미|설명|
|---|---|---|
|O(1)|상수 시간|입력 크기와 무관하게 항상 일정한 시간|
|O(log n)|로그 시간|이진 탐색처럼 입력이 절반씩 줄어듦|
|O(n)|선형 시간|입력 크기에 비례|
|O(n log n)|준선형 시간|정렬 알고리즘(병합정렬, 퀵정렬)|
|O(n²)|이차 시간|이중 반복문|
|O(2ⁿ), O(n!)|지수/팩토리얼|아주 비효율적인 알고리즘|

---

### 📚 예시로 이해하기

```python
# O(1)
def get_first(data):
    return data[0]

# O(n)
def find_max(data):
    max_val = data[0]
    for v in data:
        if v > max_val:
            max_val = v
    return max_val

# O(n²)
def print_all_pairs(data):
    for i in data:
        for j in data:
            print(i, j)
```

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|최악의 경우 기준|Big-O는 일반적으로 **Worst Case 기준**|
|비효율 탐지|큰 입력에서 성능 병목 원인 찾기|
|코드 작성 시 고려|알고리즘 선택의 핵심 기준|
|공간 vs 시간|더 빠른 속도를 위해 메모리를 더 사용할 수도 있음|

---

### 🎯 실무 팁

- 입력 데이터 크기(`n`)를 예측한 뒤 **허용 가능한 복잡도** 선택
    
- 인터뷰/시험에서는 항상 O()를 붙여 시간 복잡도 명시
    
- 정렬, 탐색, 순회 등 기본 알고리즘의 복잡도를 암기해두면 좋음
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Time Complexity]]|실행 시간 증가율 측정|
|[[Space Complexity]]|메모리 사용량 증가율 측정|
|[[Big-O Notation]]|복잡도 표현 방식|
|[[Algorithm]]|복잡도를 고려한 문제 해결 절차|

---