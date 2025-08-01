---
type: learn
created: 2025-08-02(토) / 00:58
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-08-02
review_success: false
related_concepts: []
---
## ✅ 화이트박스 테스트(White Box Testing)

### 🔤 용어 해석

- **White Box**: 내부가 들여다보이는 투명한 상자
- 👉 화이트박스 테스트는 **소스코드의 내부 로직과 흐름을 모두 고려하여 수행하는 테스트 기법**

---

### 🧩 화이트박스 테스트란?

| 항목 | 설명 |
|------|------|
| **정의** | 프로그램의 **내부 구조, 로직, 경로를 기준**으로 수행하는 테스트 |
| **목적** | 코드 흐름을 따라 **숨겨진 논리 오류나 결함**을 조기에 발견 |
| **수행 주체** | 주로 개발자 |
| **대상** | 함수, 메서드, 조건문, 반복문, 분기 등 코드 내부 구성 |

---

### 🧱 주요 테스트 기법

| 기법                              | 설명                                     |
| ------------------------------- | -------------------------------------- |
| **문장 커버리지(Statement Coverage)** | 모든 코드 문장이 최소 1회 이상 실행되도록               |
| **분기 커버리지(Branch Coverage)**    | if, switch 등의 모든 분기 조건의 참/거짓을 검사       |
| **조건 커버리지(Condition Coverage)** | 복합 조건의 각 조건이 참/거짓인 경우 모두 검사            |
| **경로 커버리지(Path Coverage)**      | 가능한 모든 실행 경로를 테스트                      |
| **루프 테스트(Loop Testing)**        | 반복문 내 동작을 0회, 1회, 여러 번 반복 등 다양한 경우로 검사 |

---

### 📚 예시로 이해하기

- `if (a > 10 && b < 5)` 조건문이 있는 경우:
  - `a > 10`이 true/false
  - `b < 5`가 true/false
  - 이 조합을 모두 만족시키는 테스트 케이스 작성

---

### 🧠 특징 요약

| 항목 | 설명 |
|------|------|
| **적용 단계** | 주로 [[Unit Test]] 시점 |
| **관점** | 내부 구현 중심 (소스코드 의존) |
| **테스트 범위** | 조건, 반복, 분기, 경로 등 로직 구조 |
| **한계** | 사용자 관점에서의 요구사항 검증은 어려움 |

---

### 🎯 실무 팁

- 테스트 대상 모듈은 **작고 독립적일수록 효과적**
- **Mock, Stub** 활용해 외부 의존성 제거
- **코드 커버리지 도구** 활용 시 문장/분기 달성률 확인 가능 (예: JaCoCo, Istanbul, Coverage.py)

---

### 🧩 블랙박스 테스트와 비교

| 항목 | [[White Box Testing]] | [[Black Box Testing]] |
|------|------------------------|------------------------|
| 중심 관점 | 내부 코드 로직 | 외부 입력과 출력 |
| 수행자 | 개발자 | QA, 사용자 |
| 테스트 대상 | 제어 흐름, 조건문, 루프 등 | 요구사항 명세 기반 기능 |
| 테스트 접근 | 구조적 | 기능적 |
