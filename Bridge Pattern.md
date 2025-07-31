---
type: learn
created: 2025-08-01(금) / 01:22
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
## ✅ 브리지 패턴 (Bridge Pattern)

### 🔤 용어 해석  
- [[Bridge Pattern|브리지 패턴]]: **구현부(Implementation)와 추상화(Abstraction)를 분리**하여 독립적으로 확장 가능하게 만드는 구조적 디자인 패턴

---

### 📌 개념 정리  
브리지 패턴은 **기능 계층(Abstraction)**과 **구현 계층(Implementor)**을 별도로 나누어, 서로 영향을 주지 않고 독립적으로 변경하거나 확장할 수 있게 한다.  
다양한 조합의 클래스 구조를 효율적으로 구현할 때 유리하며, **클래스의 다형성과 위임을 활용**한다.

---

### ⚙️ 구성 요소  
- **Abstraction**: 기능 계층의 인터페이스 정의 (예: Remote)  
- **RefinedAbstraction**: Abstraction을 확장한 구체 클래스  
- **Implementor**: 구현 계층의 인터페이스 (예: Device)  
- **ConcreteImplementor**: 실제 구현 클래스 (예: TV, Radio)

---

### 🧭 흐름 / 방향성  
1. 클라이언트는 Abstraction 계층을 사용  
2. Abstraction은 내부적으로 Implementor 인터페이스에 위임  
3. 구현은 Implementor 계층에서 담당  
→ 기능과 구현을 분리하여 **독립적인 확장 가능**

---

### 💬 실무 예시  
- 다양한 리모컨(Remote, 기능 계층)과 여러 기기(TV, Radio 등 구현 계층)를 조합  
- UI 프레임워크에서 윈도우 시스템마다 다른 그래픽 구현을 위임  
- DB 연결 라이브러리에서 다양한 DB 드라이버에 대한 인터페이스 분리

---

### 🔁 관련 개념 비교

| 항목           | 브리지 패턴           | 어댑터 패턴            |
|----------------|------------------------|-------------------------|
| 목적           | 추상화와 구현 분리     | 인터페이스 호환        |
| 사용 시점      | 처음부터 구조 설계 시  | 기존 클래스 재사용 시   |
| 관계 방식      | 위임(Delegate)         | 변환(Wrapper)           |
| 유연성         | 매우 높음              | 낮음 (기존 구조 제약)   |

---

### 🎯 핵심 요약  
- **기능과 구현을 분리하여 유연한 구조 제공**  
- 다형성과 위임을 활용한 **구조적 디자인 패턴**  
- 클래스 조합이 많은 경우 매우 효과적

---

### 🧠 학습 메모  
- 기출 표현 주의: “추상화와 구현의 독립적 확장”, “위임”, “다형성”  
- Adapter는 변환이고, Bridge는 구조 분리임
