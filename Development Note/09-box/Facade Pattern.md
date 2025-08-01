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
## ✅ 퍼사드 패턴 (Facade Pattern)

### 🔤 용어 해석  
- [[Facade Pattern|퍼사드 패턴]]: 복잡한 서브시스템을 **단순한 인터페이스로 감싸는** 구조적 디자인 패턴

---

### 📌 개념 정리  
퍼사드는 여러 클래스와 메서드로 이루어진 복잡한 로직을 **하나의 진입점 인터페이스로 단순화**하여 제공한다. 클라이언트는 내부 구조를 몰라도 된다.

---

### ⚙️ 구성 요소  
- Facade: 단순화된 인터페이스  
- Subsystems: 실제 로직을 수행하는 여러 클래스들  
- Client: 퍼사드만 사용

---

### 💬 실무 예시  
- 스프링 프레임워크의 JdbcTemplate  
- 비디오 플레이어에서 Facade 객체가 디코더, 사운드, UI 등 묶어서 처리

---

### 🎯 핵심 요약  
- 복잡한 내부 구조를 **단일 인터페이스로 캡슐화**  
- 클라이언트-서브시스템 의존도 감소  
- 단순화, 접근 제한 목적

---