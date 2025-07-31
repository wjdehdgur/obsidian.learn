---
type: learn
created: 2025-08-01(금) / 00:17
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
## ✅ Builder (빌더 패턴)

### 🔤 용어 해석
- Builder: 복잡한 객체의 생성 과정을 **단계별로 나눠서 처리**하고, 그 과정을 캡슐화하는 생성 패턴

---

### 📌 개념 정리
빌더 패턴은 복잡한 객체를 **단계별로 생성**할 수 있도록 하고, 객체의 구성 절차와 표현 방식을 **분리**하여 동일한 구성 절차로도 다양한 표현을 만들 수 있게 한다.

---

### ⚙️ 구성 요소
- **Builder**: 생성 절차를 정의하는 추상 인터페이스
- **ConcreteBuilder**: 실제 생성 절차 구현
- **Director**: 생성 순서를 지정
- **Product**: 최종 완성된 객체

---

### 🧭 흐름 / 방향성
1. 클라이언트가 `Director`에게 객체 생성을 요청
2. `Director`는 `Builder`를 통해 순차적으로 객체 생성
3. 생성이 완료되면 `Product` 반환

---

### 💬 실무 예시
- 자바의 `StringBuilder`
- JSON/XML 파서에서 복합 객체 생성
- HTML 문서 생성기
- ORM Query Builder (`QueryBuilder.select().where().orderBy()` 등)

---

### 🔁 관련 개념 비교
| 구분              | Builder                     | Abstract Factory                |
|-------------------|------------------------------|----------------------------------|
| 목적              | 복잡한 객체 조립             | 제품군 생성                      |
| 제어              | Director가 순서 제어         | 팩토리에서 생성 책임 분리       |
| 객체의 구성 방식  | 단계별로 유연하게 설정       | 미리 정의된 제품군 조합         |
| 생성물            | 단일 복합 객체               | 연관된 여러 객체                |

---

### 🎯 핵심 요약
- **단계별 객체 생성 로직을 분리**하여 유연성 확보
- 객체 생성과 표현 분리 → **같은 과정으로 다른 결과 가능**
- 생성자 인자 너무 많을 때 매우 유용

---

### 🧠 학습 메모
- 자바 Lombok의 `@Builder` 어노테이션도 이 패턴 활용
- [[Factory Method|팩토리]]는 "무엇"을 만들지만, [[Builder Pattern|빌더]]는 "어떻게" 만들지를 제어함
