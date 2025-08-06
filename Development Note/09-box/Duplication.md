---
type: learn
created: 2025-08-05(화) / 00:34
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
## ✅ 중복(Duplication)

### 🔤 용어 해석

- Duplication: 반복, 중복  
- 👉 [[Duplication]]은 **같은 코드, 로직, 데이터 또는 구조가 여러 곳에 반복되어 존재하는 현상**

---

### 🧩 중복이란?

| 항목 | 설명 |
|------|------|
| **정의** | [[Duplication]]은 동일하거나 유사한 코드, 쿼리, 문서, 설정 등이 **여러 위치에 반복되어 존재**하는 것을 의미하며, 유지보수성과 안정성을 해치는 대표적 코드 냄새(Code Smell) 중 하나다. |
| **문제점** | 버그 발생 가능성 증가, 수정 누락 위험, 파일 크기 증가 |
| **원인** | 복붙(copy-paste), 구조화 부족, DRY 원칙 위반 |
| **대표 예시** | 조건문, 유틸 함수, 설정 값, SQL 쿼리 등이 여러 곳에 동일하게 존재 |

---

### 🧠 특징 요약

- **DRY(Don’t Repeat Yourself)** 원칙 위반 사례
- **수정 비용 증가**: 한 번 수정할 때 여러 곳을 동시에 고쳐야 함
- **버그 위험 증가**: 일부 누락 또는 불일치로 인해 오류 발생
- **리팩토링 대상 1순위**: 함수/클래스 추출로 개선 가능

---

### 💡 실무 팁

- 중복된 코드는 함수/모듈로 추출  
- 설정 값은 `.env`, `config.js`, `application.yml` 등 외부화  
- SQL 쿼리는 별도 DAO 또는 Repository 객체로 분리  
- SonarQube, ESLint, IntelliJ Inspect 같은 도구로 중복 탐지 자동화 가능

---

### 🔗 관련 개념 비교

| 개념 | 설명 |
|------|------|
| [[Duplication]] | 동일한 로직/데이터가 여러 곳에 반복 |
| [[DRY]] | 중복을 피하라는 프로그래밍 원칙 |
| [[Refactoring]] | 중복 제거, 가독성 개선 등을 위한 코드 개선 작업 |
| [[Modularization]] | 중복 제거를 위한 구조화 기법 |
| [[Code Smell]] | 리팩토링이 필요한 코드의 특징적인 냄새 (중복 포함) |
