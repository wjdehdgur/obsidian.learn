---
type: learn
created: 2025-08-01(금) / 00:13
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
## ✅ Singleton (싱글턴)

### 🔤 용어 해석
- Singleton: 애플리케이션 전체에서 **오직 하나의 인스턴스만 존재**하도록 보장하는 디자인 패턴

---

### 📌 개념 정리
싱글턴 패턴은 클래스의 인스턴스를 **하나만 생성하고 공유**하도록 제어하는 방식이다. 전역 상태를 관리하거나 공통 자원을 다룰 때 유용하다.

---

### ⚙️ 구성 요소
- **private 생성자**: 외부에서 객체 생성을 막음
- **static 변수**: 유일한 인스턴스를 저장
- **static 메서드**: 인스턴스를 반환하는 전역 접근 지점

---

### 🧭 흐름 / 방향성
1. 객체 생성을 막기 위해 생성자를 `private`으로 선언
2. 클래스 내부에 정적 변수로 인스턴스 생성
3. 정적 메서드를 통해 외부에서 인스턴스 접근

---

### 💬 실무 예시
- DB 연결 객체 (`DBConnection.getInstance()`)
- 로그 시스템 (`Logger.getInstance()`)
- 설정 정보 관리자 (`ConfigManager.getInstance()`)

---

### 🔁 관련 개념 비교
| 구분             | Singleton                     | 일반 클래스 인스턴스             |
|------------------|--------------------------------|----------------------------------|
| 인스턴스 개수    | 단 하나                        | 여러 개 가능                     |
| 생성 제한        | 생성자 `private`                | `public` 생성자 가능              |
| 접근 방식        | `클래스명.getInstance()`       | `new` 키워드로 생성              |
| 활용 목적        | 전역 관리, 리소스 절약          | 개별 책임 수행                   |

---

### 🎯 핵심 요약
- **유일한 인스턴스**, **전역 접근**, **자원 절약** 목적
- 대표적인 [[Creational Pattern|생성 패턴]]
- 멀티스레드 환경에서는 **동기화(synchronized)** 고려 필요

---

### 🧠 학습 메모
- 자바에서는 `enum` 기반 싱글턴으로 thread-safe 구현 가능
- [[Factory Pattern|팩토리 패턴]]과 함께 사용되는 경우 많음
