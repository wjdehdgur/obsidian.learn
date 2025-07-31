---
type: learn
created: 2025-08-01(금) / 00:14
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-08-01
review_success: false
related_concepts: []
---
## ✅ Factory Method (팩토리 메서드)

### 🔤 용어 해석
- Factory Method: 객체 생성을 **서브클래스에 위임**하는 디자인 패턴

---

### 📌 개념 정리
팩토리 메서드는 객체를 생성하는 **구체적인 로직을 숨기고**, 상위 클래스에서 객체 생성의 **인터페이스만 정의**하고, 실제 생성은 하위 클래스가 담당하도록 한다. [[Polymorphism]]을 활용해 객체 생성을 유연하게 한다.

---

### ⚙️ 구성 요소
- **Product (제품 인터페이스)**: 생성될 객체의 공통 인터페이스
- **ConcreteProduct**: 실제 생성되는 객체
- **Creator (팩토리)**: 팩토리 메서드를 선언하는 클래스
- **ConcreteCreator**: 팩토리 메서드를 오버라이딩하여 실제 객체를 생성하는 클래스

---

### 🧭 흐름 / 방향성
1. 클라이언트는 `Creator` 클래스를 통해 `createProduct()` 호출
2. `ConcreteCreator`가 구체적인 `Product` 객체 생성
3. 클라이언트는 구체 클래스 몰라도 객체 사용 가능

---

### 💬 실무 예시
- GUI Toolkit에서 OS별 버튼 클래스 (ex. `WindowsButton`, `MacButton`)
- 스프링의 Bean 생성에서 팩토리 메서드 사용
- 로그 생성기, 알림 시스템 등에서 다양한 타입 객체 생성

---

### 🔁 관련 개념 비교
| 구분                  | Factory Method              | Singleton                         |
|-----------------------|-----------------------------|------------------------------------|
| 생성 목적             | 다양한 객체 생성            | 단일 객체 생성                     |
| 다형성 활용           | 높음                        | 낮음                              |
| 대표 활용 방식        | 인터페이스 기반 생성 위임   | 전역 객체 관리                     |
| 하위 클래스 개입 여부 | 있음                        | 없음                              |

---

### 🎯 핵심 요약
- 객체 생성 책임을 **서브클래스에 위임**
- [[Open/Closed Principle|개방-폐쇄 원칙]]에 부합
- 유연하고 확장 가능한 구조 제공

---

### 🧠 학습 메모
- 팩토리 메서드는 [[Abstract Factory|추상 팩토리]]와 함께 자주 비교됨
- 조건문 남발을 방지하고 객체 생성을 캡슐화하는 데 효과적
