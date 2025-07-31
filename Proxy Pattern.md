---
type: learn
created: 2025-08-01(금) / 01:25
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
## ✅ 프록시 패턴 (Proxy Pattern)

### 🔤 용어 해석  
- [[Proxy Pattern|프록시 패턴]]: 실제 객체에 접근하기 전 **대리 객체를 통해 제어**하는 구조적 디자인 패턴

---

### 📌 개념 정리  
프록시는 **접근 제어, 지연 로딩, 로깅, 보안** 등 부가 기능을 제공하며, 실제 객체를 대신해 동작하거나, 실제 객체 생성/호출 시점을 지연시킨다.

---

### ⚙️ 구성 요소  
- Subject: 공통 인터페이스  
- RealSubject: 실제 객체  
- Proxy: 대리 객체, RealSubject에 접근 제어

---

### 💬 실무 예시  
- 가상 프록시: 이미지 로딩 지연 처리  
- 보호 프록시: 관리자 권한 확인 후 실행  
- 원격 프록시: 네트워크 통신 처리

---

### 🎯 핵심 요약  
- **접근 제어 또는 부가기능 추가 목적**  
- 실제 객체 대신 **프록시 객체가 우선 응답**  
- 지연 로딩, 보안, 로깅 등에 활용