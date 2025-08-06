---
type: learn
created: 2025-08-07(목) / 00:03
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-08-07
review_success: false
related_concepts: []
---



## ✅ xUnit

### 🔤 용어 해석

- xUnit: 'x'는 언어를 의미하며, 다양한 언어의 단위 테스트 프레임워크를 통칭
- 👉 **단위 테스트(Unit Test)**를 지원하는 대표적인 테스트 프레임워크 계열

---

### 🧩 xUnit이란?

| 항목 | 설명 |
|------|------|
| **정의** | 다양한 프로그래밍 언어에서 **단위 테스트를 작성하고 실행하기 위한 테스트 프레임워크의 집합** |
| **목적** | 테스트 코드의 구조화, 반복 실행, 자동화를 통해 **코드 품질 확보** |
| **분류** | [[Unit Testing]]의 도구 계열 (예: JUnit, NUnit, PyTest 등)

---

### 🧱 주요 구성 요소

| 구성 요소 | 설명 |
|-----------|------|
| Test Case | 하나의 테스트 단위 |
| Test Suite | 여러 테스트 케이스의 모음 |
| Test Runner | 테스트 실행 도구 |
| Assertion | 기대 결과와 실제 결과를 비교하는 문장

---

### 📚 예시로 이해하기1 (직관적 예시)

- **예**: `add(2, 3)` 함수의 결과가 `5`인지 확인하는 단위 테스트  
→ 실패 시 코드 수정 필요 판단 가능

---

### 📚 예시로 이해하기2 (Python - PyTest 예시)

```python
def add(a, b):
    return a + b

def test_add():
    assert add(2, 3) == 5
````

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|자동화|수동 테스트 반복을 자동화|
|언어별 호환|Java(JUnit), C#(NUnit), Python(PyTest) 등|
|일관된 구조|Setup → Test → Teardown 패턴|
|CI 연동|GitHub Actions, Jenkins 등과 쉽게 연동 가능|

---

### 🎯 실무 팁

- **CI/CD 파이프라인에 필수 적용**되는 기본 테스트 프레임워크
    
- 테스트는 **작고 빠르게 실행되도록** 구성
    
- **목(Mock), 스텁(Stub)** 등과 함께 사용하여 의존성 격리
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Unit Testing]]|기능 단위로 모듈 테스트|
|xUnit|Unit Test를 위한 프레임워크 집합|
|[[STAF]]|자동화 테스트 프레임워크(시스템 간 통합 테스트 중심)|
|[[Test Driver]]|테스트 실행을 위한 임시 모듈 (xUnit 실행과는 별개)|
