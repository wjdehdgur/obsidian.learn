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
## ✅ 플라이웨이트 패턴 (Flyweight Pattern)

### 🔤 용어 해석  
- [[Flyweight Pattern|플라이웨이트 패턴]]: 메모리 사용을 줄이기 위해 **공유 가능한 객체를 재사용**하는 구조적 디자인 패턴

---

### 📌 개념 정리  
동일하거나 유사한 객체가 많이 필요할 때, 중복 객체 생성을 피하고 **공통 상태는 공유**하고 **개별 상태만 분리**함으로써 성능을 최적화한다.

---

### ⚙️ 구성 요소  
- Flyweight: 공유 객체 인터페이스  
- ConcreteFlyweight: 실제 공유 객체  
- FlyweightFactory: 공유 객체를 생성하고 캐싱  
- Client: 외부 상태를 전달

---

### 💬 실무 예시  
- 텍스트 에디터에서 글꼴(Font) 객체 공유  
- 게임에서 배경 나무 객체 수천 개를 하나의 인스턴스로 공유

---

### 🎯 핵심 요약  
- 메모리 절약 목적  
- **공유 가능한 객체는 캐싱 후 재사용**  
- **외부 상태**만 개별로 보관

---