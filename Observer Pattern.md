---
type: learn
created: 2025-08-01(금) / 00:38
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
## ✅ Observer Pattern (옵저버 패턴)

### 🔤 용어 해석
- Observer Pattern: 객체 상태 변화에 따라 **연관된 객체들이 자동으로 알림을 받도록** 구성하는 행동 패턴

---

### 📌 개념 정리
옵저버 패턴은 **하나의 주체(Subject)**의 상태 변화가 있을 때, 이를 **구독하고 있는 여러 옵저버(Observer)**들에게 자동으로 알림이 전달되도록 하는 구조이다. **느슨한 결합**과 **이벤트 기반 설계**에 적합하다.

---

### ⚙️ 구성 요소
- **Subject (발행자)**: 상태를 보유하고 옵저버를 등록/해제/알림
- **Observer (구독자)**: Subject의 상태 변화에 반응
- **ConcreteSubject / ConcreteObserver**: 실제 동작을 구현한 클래스

---

### 🧭 흐름 / 방향성
1. 옵저버가 Subject에 등록 (`subscribe`)
2. Subject의 상태가 변경되면
3. 모든 등록된 Observer에게 알림 전달
4. 각 Observer는 알림에 따라 동작 수행

---

### 💬 실무 예시
- UI: 버튼 클릭 시 여러 이벤트 핸들러가 동작
- SNS: 팔로우 중인 계정의 새 글 알림
- 데이터 바인딩: Model의 값 변경 → View 자동 갱신 (ex. React `useEffect`)
- RxJS, EventEmitter 등 이벤트 라이브러리

---

### 🔁 관련 개념 비교
| 구분             | Observer Pattern                  | [[MVC]]                                |
|------------------|------------------------------------|----------------------------------------|
| 목적             | 이벤트 기반 알림 분산              | 관심사 분리 및 UI 아키텍처             |
| 구성 요소        | Subject, Observer                  | Model, View, Controller                |
| 적용 대상        | 비동기 이벤트, 상태 변화 감지       | 전체 UI 구조 설계                     |

---

### 🎯 핵심 요약
- 옵저버 패턴은 **1:N 관계에서 상태 변화 자동 알림**
- 느슨한 결합을 통한 **유지보수성 강화**
- 이벤트 기반 UI 및 데이터 연동에 효과적

---

### 🧠 학습 메모
- Java의 `Observer`, 자바스크립트의 `EventListener`, RxJS의 `Observable`이 대표 구현
- [[Publisher-Subscriber|퍼블리셔-서브스크라이버 패턴]]과 유사하나, 옵저버는 더 직접적인 참조 구조
