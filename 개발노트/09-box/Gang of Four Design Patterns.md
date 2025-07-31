---
type: learn
created: 2025-07-24(목) / 23:14
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-07-24
review_success: false
related_concepts: []
---
## ✅ GoF 디자인 패턴 (Gang of Four Design Patterns)

### 🔤 용어 해석  
- GoF: Gang of Four (4인조), 디자인 패턴 개념을 정립한 4명의 저자 (Erich Gamma, Richard Helm, Ralph Johnson, John Vlissides)  
- Design Pattern: 반복되는 설계 문제에 대한 **재사용 가능한 해법**

---

### 📌 개념 정리  
GoF 디자인 패턴은 1994년 《Design Patterns: Elements of Reusable Object-Oriented Software》에서 처음 제시된 객체지향 소프트웨어 설계의 표준 해법 집합이다.  
이들은 소프트웨어 설계에서 반복적으로 발생하는 문제를 **객체 간의 상호작용과 책임 분배 원칙에 따라 세 가지 범주로 분류**했다:

1. **[[Creational Pattern|생성 패턴(Creational)]]**: 객체 생성 방식에 유연성 제공  
2. **[[Structural Pattern|구조 패턴(Structural)]]**: 클래스/객체 간의 구성 구조 정의  
3. **[[Behavioral Pattern|행위 패턴(Behavioral)]]**: 객체 간의 책임 분배와 상호작용 정의

총 23가지 패턴이 정의되어 있다.

---

### ⚙️ 구성 요소  
- **패턴 이름(Name)**: 문제를 요약적으로 표현  
- **문제(Problem)**: 해결하고자 하는 반복되는 설계 문제  
- **해법(Solution)**: 설계를 유도하는 구조/객체 관계  
- **결과(Result)**: 패턴 적용 시의 장단점 및 영향  
- **클래스 다이어그램**: 객체 구성 시각화  
- **구현 코드**: 예시 또는 템플릿 형태

---

### 🧭 흐름 / 방향성  
1. 소프트웨어 설계 중 반복적인 문제 발생  
2. 유사한 상황에 맞는 GoF 패턴 선택  
3. 설계 구조에 패턴 적용  
4. 캡슐화, 의존성 감소, 유연성 향상

---

### 💬 실무 예시  
- **싱글턴(Singleton)**: 설정 정보, DB 연결 등 단일 인스턴스 보장  
- **팩토리 메서드(Factory Method)**: 객체 생성 책임 분리  
- **옵저버(Observer)**: 이벤트 기반 UI, 알림 시스템  
- **데코레이터(Decorator)**: 기능 추가 시 코드 수정 없이 확장  
- **커맨드(Command)**: 요청을 객체로 캡슐화하여 큐나 실행 취소 가능하게 함

---

### 🔁 관련 개념 비교  
| 분류 | 대표 패턴 | 설명 |
|------|-----------|------|
| 생성 패턴 | Singleton, Factory Method, Abstract Factory | 객체 생성 방식 유연화 |
| 구조 패턴 | Adapter, Composite, Decorator | 객체/클래스 간 구조 정의 |
| 행위 패턴 | Observer, Strategy, Command | 객체 간 행위와 책임 분산 |

---

### 🎯 핵심 요약  
- GoF 디자인 패턴은 객체지향 설계의 베스트 프랙티스  
- 23개의 패턴이 생성/구조/행위 패턴으로 분류됨  
- 유지보수성과 확장성을 높이기 위한 설계 전략

---

### 🧠 학습 메모  
- 시험에선 패턴 명칭, 목적, 구조 분류 많이 출제됨  
- 팩토리 vs 추상 팩토리, 옵저버 vs 퍼블리셔 등 유사 개념 구분 중요  
- UML 클래스 다이어그램 연습해두면 시각화에 도움 됨
