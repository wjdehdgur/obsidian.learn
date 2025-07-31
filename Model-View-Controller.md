---
type: learn
created: 2025-08-01(금) / 00:36
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
## ✅ MVC (Model-View-Controller)

### 🔤 용어 해석
- MVC: **Model-View-Controller**, 사용자 인터페이스를 **세 가지 역할로 분리**하는 아키텍처 패턴

---

### 📌 개념 정리
MVC는 애플리케이션을 세 가지 구성 요소로 나눠 **관심사의 분리(Separation of Concerns)**를 실현하는 설계 패턴이다. 각 요소는 다음과 같은 역할을 가진다:
- **Model**: 데이터와 비즈니스 로직
- **View**: 사용자 인터페이스
- **Controller**: 사용자 입력 처리 및 흐름 제어

---

### ⚙️ 구성 요소
- **Model**: DB, API 등에서 가져온 데이터의 상태와 처리 로직 담당
- **View**: 사용자에게 보여지는 UI 담당 (HTML, 화면 출력)
- **Controller**: 사용자 입력을 받고 Model을 제어하며 View에 반영

---

### 🧭 흐름 / 방향성
1. 사용자가 View에서 이벤트(입력) 발생
2. Controller가 이를 받아 Model에 명령 전달
3. Model의 데이터가 변경되면 View를 통해 사용자에게 반영

---

### 💬 실무 예시
- 웹 프레임워크
  - Django (Python): MTV 구조지만 사실상 MVC
  - Spring MVC (Java)
  - Ruby on Rails
- 프론트엔드
  - React (View 중심 라이브러리지만, 외부에 Controller-Model 역할 분리 가능)

---

### 🔁 관련 개념 비교
| 구분        | MVC                                | [[MVVM|MVVM]]                             |
|-------------|-------------------------------------|--------------------------------------------|
| Controller | 명시적으로 존재                      | 없음 (ViewModel이 제어 역할 수행)        |
| View와 Model 연결 | 간접 (Controller 통해 연결)     | 직접 바인딩 (Data Binding)                |
| 주로 사용처 | 백엔드, 서버 중심 앱                | 프론트엔드, 앱 UI                          |

---

### 🎯 핵심 요약
- MVC는 UI 애플리케이션에서 **역할 분리와 유지보수성 향상**을 위해 사용
- View, Model, Controller 간 **명확한 책임 분리**
- 대형 웹/앱 시스템의 기본 설계 패턴

---

### 🧠 학습 메모
- [[Observer Pattern|옵저버 패턴]]과 함께 자주 등장
- 비슷한 구조로 [[MVP]], [[MVVM]] 등도 정리 필요
