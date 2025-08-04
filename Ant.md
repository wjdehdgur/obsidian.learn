---
type: learn
created: 2025-08-05(화) / 00:24
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
## ✅ 앤트(Ant)

### 🔤 용어 해석

- Ant: Another Neat Tool  
- 👉 Java 환경의 **최초의 [[Build Automation Tool|빌드 자동화 도구]]**, XML 기반 명령어 나열 방식 사용

---

### 🧩 Ant란?

| 항목 | 설명 |
|------|------|
| **정의** | [[Ant]]는 Apache에서 개발한 **XML 기반의 빌드 자동화 도구**로, 자바 프로젝트에서 컴파일, 테스트, 배포 등을 스크립트로 정의해 자동화할 수 있게 해준다. |
| **기반 구조** | 명령어(task)를 XML 파일(`build.xml`)에 나열하여 순차 실행 |
| **장점** | 구조가 단순하고 유연함, 커스터마이징 쉬움 |
| **단점** | XML 기반으로 빌드 로직이 장황하고 유지보수 어려움, 의존성 관리 기능 없음 |
| **사용 예시** | `ant compile`, `ant test`, `ant dist` 등의 태스크 실행 |

---

### 🧠 특징 요약

- **초기 빌드 자동화 도입 도구**: Maven, Gradle 이전의 표준
- **절차지향적**: 명령어 순서를 직접 정의
- **의존성 관리 없음**: Ivy 등의 별도 도구 필요
- **실행 속도 빠름**: 구조가 단순한 프로젝트에서 유리

---

### 💡 실무 팁

- 대규모 프로젝트보다는 **단일 프로젝트**나 **레거시 유지보수용**으로 사용
- Gradle이나 Maven으로 **점진적 마이그레이션**이 추천됨
- 커맨드라인 태스크 자동화 또는 Jenkins 빌드 태스크로 활용 가능

---

### 🔗 관련 개념 비교

| 개념 | 설명 |
|------|------|
| [[Ant]] | 명령어 나열식, XML 기반 |
| [[Maven]] | 선언적 구조, 라이프사이클 중심 |
| [[Gradle]] | 태스크 기반, Groovy/Kotlin DSL |
| [[Build Script]] | Ant의 `build.xml` 같은 자동화 정의 파일 |
| [[Ivy]] | Ant용 의존성 관리 플러그인 |
