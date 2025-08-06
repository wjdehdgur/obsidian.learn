---
type: learn
created: 2025-08-05(화) / 00:28
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-08-05
review_success: false
related_concepts: []
---

## ✅ 클린 코드(Clean Code)

### 🔤 용어 해석

- Clean Code: 읽기 쉽고, 변경에 강하며 오류 가능성이 낮은 코드  
- 👉 [[Clean Code]]는 **가독성, 일관성, 단일 책임, 중복 제거, 의존성 최소화** 등의 원칙을 따르는 코드 작성 철학

---

### 🧩 클린 코드란?

| 항목 | 설명 |
|------|------|
| **정의** | [[Clean Code]]는 동작만 하는 코드가 아닌, **이해하기 쉽고 수정하기 쉬우며 오류 가능성이 적은 코드**를 의미한다. |
| **핵심 철학** | "사람이 읽기 좋은 코드가 좋은 코드다" – 로버트 C. 마틴 |
| **적용 대상** | 변수명, 함수 구조, 클래스 책임, 주석, 의존성, 조건문 등 코드 전반 |
| **참고 도서** | 《Clean Code: A Handbook of Agile Software Craftsmanship》 by Robert C. Martin |

---

### 🧠 클린 코드 작성 원칙

| 원칙              | 설명                                       |
| --------------- | ---------------------------------------- |
| [[Readability]] | 코드는 사람을 위한 문서처럼 읽히도록 작성                  |
| [[Duplication]] | 같은 코드를 반복하지 않고 함수, 모듈로 추출                |
| [[Dependency]]  | 외부 모듈/라이브러리에 불필요하게 얽히지 않음                |
| 함수는 짧고 명확하게     | 하나의 함수는 한 가지 일만 해야 함 (SRP)               |
| 명확한 네이밍         | 변수와 함수명은 동작/의도를 명확히 표현                   |
| 주석 최소화          | 잘 쓴 코드는 주석이 필요 없음. **오해를 줄이는 코드** 자체가 중요 |
| 불필요한 코드 제거      | 쓰지 않는 코드, 불필요한 조건, 미사용 변수 제거             |

---

### 💡 실무 팁

- `Boolean isActive()`처럼 **의도를 드러내는 네이밍** 사용  
- `if (isEmpty(list))` 처럼 **조건문 명확화**  
- `main`, `test`, `config` 디렉토리 구조와 **레이어 구분 철저히**  
- 리팩토링 도구나 [[Static Analysis|정적 분석 도구]] 적극 활용 (SonarQube, ESLint 등)

---

### 🔗 관련 개념 비교

| 개념                                  | 설명                                 |
| ----------------------------------- | ---------------------------------- |
| [[Clean Code]]                      | 유지보수성과 의도 전달 중심의 코드                |
| [[Refactoring]]                     | 기능은 그대로, 구조만 개선                    |
| [[Code Smell]]                      | 개선이 필요한 나쁜 코드 징후                   |
| [[YAGNI(You Aren't Gonna Need It)]] | 필요하지 않은 기능은 만들지 않기                 |
| [[KISS(Keep It Simple, Stupid]]     | Keep It Simple, Stupid – 단순하게 설계하라 |
