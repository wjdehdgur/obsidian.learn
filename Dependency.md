---
type: learn
created: 2025-08-05(화) / 00:35
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
## ✅ 의존성(Dependency)

### 🔤 용어 해석

- Dependency: 의존성, 종속 관계  
- 👉 [[Dependency]]는 **어떤 모듈이나 요소가 다른 요소에 기대어 동작**하는 관계를 의미함

---

### 🧩 의존성이란?

| 항목 | 설명 |
|------|------|
| **정의** | [[Dependency]]는 소프트웨어 구성 요소 간에 **한 요소가 다른 요소의 기능, 자원 또는 결과에 의존**하여 동작하는 관계를 의미한다. |
| **종류** | 코드 레벨(클래스 간), 패키지 레벨(라이브러리), 시스템 레벨(API, DB 등) |
| **예시** | A 클래스가 B 클래스를 생성하거나 메서드를 호출할 때 → A는 B에 의존 |
| **문제점** | 지나친 의존은 테스트 어려움, 결합도 상승, 변경에 취약함 |
| **해결 기법** | [[Dependency Injection]], [[Interface]], [[Loose Coupling]] 등으로 해결 가능 |

---

### 🧠 특징 요약

- **결합도(Coupling)와 직결**: 의존성이 높을수록 결합도가 높고 유연성이 낮음
- **의존성 주입**: 의존 객체를 외부에서 주입해 제어권을 넘김
- **모듈화와 테스트**: 의존성을 줄이면 단위 테스트와 재사용성이 좋아짐
- **빌드 의존성**: [[Maven]], [[Gradle]] 등의 빌드 도구에서 외부 라이브러리 설정 시 사용

---

### 💡 실무 팁

- 인터페이스 사용으로 구현체에 대한 직접 의존 회피  
- [[Spring Framework]]에서는 의존성 주입(DI)을 통한 의존성 관리 제공  
- Gradle에서는 `implementation`, `api`, `compileOnly` 등 의존성 범위 명확히 설정  
- 의존성 순환(Circular Dependency) 발생 시 설계 재검토 필요

---

### 🔗 관련 개념 비교

| 개념 | 설명 |
|------|------|
| [[Dependency]] | 한 요소가 다른 요소에 기대어 동작하는 관계 |
| [[Coupling]] | 두 모듈 간의 연결 강도 |
| [[Dependency Injection]] | 의존 객체를 외부에서 주입해 결합도 감소 |
| [[Modularization]] | 의존성과 결합도를 고려한 구조 분리 |
| [[Library]] | 코드에서 사용하는 외부 의존 자원 |
