---
type: learn
created: 2025-08-18(월) / 23:47
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
## ✅ 파이썬(Python)

### 🔤 용어 해석

- Python: 파이썬, 고급 프로그래밍 언어
    
- 👉 간결하고 직관적인 문법으로 다양한 분야에서 사용되는 범용 언어
    

---

### 🧩 파이썬이란?

|항목|설명|
|---|---|
|**정의**|인간 친화적인 문법을 가진 고수준의 범용 프로그래밍 언어|
|**목적**|코드 생산성 향상, 쉬운 학습, 다양한 분야의 확장성 확보|
|**분류**|[[Interpreter Language]], [[High-Level Language]], [[Object-Oriented Language]]|

---

### 🧱 구성 요소

|구성 요소|설명|
|---|---|
|자료형|정수형, 실수형, 문자열, [[List]], [[Tuple]], [[Dictionary]], [[Set]] 등|
|제어문|`if`, `elif`, `else`, `while`, `for`|
|함수|`def`, `return`, `lambda` 등|
|내장 함수|`print()`, `range()`, `len()`, `type()`, `input()` 등|
|기타|리스트 컴프리헨션, 슬라이싱, 예외 처리, 모듈 import 등|

---

### 📚 예시로 이해하기1(이해하기 쉬운 직관적인 예시)

- 리스트에서 짝수만 추출하려면?  
    → 리스트 컴프리헨션: `[x for x in range(10) if x % 2 == 0]`
    

---

### 📚 예시로 이해하기2 (언어 명시)

```python
# 리스트 슬라이싱
data = [10, 20, 30, 40, 50]
print(data[1:4])  # [20, 30, 40]

# 함수 정의와 호출
def greet(name):
    return f"Hello, {name}!"

print(greet("Alice"))

# 람다 함수 사용
add = lambda x, y: x + y
print(add(3, 5))  # 8
```

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|문법|간결하고 들여쓰기로 블록 구성|
|생산성|적은 코드로 많은 기능 구현 가능|
|확장성|웹, AI, 데이터 분석, 시스템 등 활용 범위 넓음|
|인터프리터|실행 즉시 해석, 디버깅이 쉬움|
|커뮤니티|방대한 오픈소스 생태계|

---

### 🎯 실무 팁

- 기본 문법은 **100문제 실습**으로 체득,  
    `collections`, `itertools`, `os`, `re` 모듈은 **실무 전 필수 학습**
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[C]]|저수준 언어로 하드웨어 제어 및 컴파일 기반|
|파이썬(Python)|고수준 언어로 간결한 문법과 높은 생산성을 지님|