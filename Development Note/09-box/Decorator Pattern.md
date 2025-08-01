---
type: learn
created: 2025-08-01(금) / 01:24
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
## ✅ 데코레이터 패턴 (Decorator Pattern)

### 🔤 용어 해석  
- [[Decorator Pattern|데코레이터 패턴]]: 기존 객체를 변경하지 않고 **기능을 동적으로 추가**할 수 있는 구조적 디자인 패턴

---

### 📌 개념 정리  
데코레이터는 **객체를 감싸서(Wrapper)** 기능을 덧붙이는 방식으로, **상속 대신 위임을 통해 기능 확장**이 가능하게 한다. 기능 조합을 유연하게 구성할 수 있다.

---

### ⚙️ 구성 요소  
- Component: 공통 인터페이스  
- ConcreteComponent: 실제 객체  
- Decorator: Component를 구현하고 Component를 참조  
- ConcreteDecorator: 추가 기능을 구현하는 클래스

---

### 💬 실무 예시  
- Java I/O의 BufferedInputStream, DataInputStream 등  
- 커피 주문 시 기본 커피 + 휘핑, 시럽 등 옵션을 중첩하는 구조

---

### 🎯 핵심 요약  
- 상속 없이 기능을 **동적으로 확장**  
- 감싸는 구조, 중첩 가능  
- 런타임 중 기능 조합 유연

---