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
## ✅ 그레이들(Gradle)

### 🔤 용어 해석

- Gradle: Gradual + Build의 합성어  
- 👉 [[Build Automation Tool|빌드 자동화 도구]]로, **유연하고 빠른 빌드 시스템**을 제공하는 현대적 도구

---

### 🧩 Gradle이란?

| 항목 | 설명 |
|------|------|
| **정의** | [[Gradle]]은 Groovy 또는 Kotlin DSL을 사용하여 **태스크 기반(Task-based)의 유연한 빌드 자동화 도구**로, 선언적 + 절차적 빌드 구성이 모두 가능하다. |
| **장점** | 빠른 빌드, 캐시 처리, 병렬 처리, 멀티 프로젝트 지원 |
| **의존성 관리** | Maven, Ivy 저장소와 호환되며 DSL로 관리 가능 |
| **스크립트 예시** | `build.gradle`, `settings.gradle`, `gradle.properties` 등 |
| **사용 명령어** | `gradle build`, `gradle test`, `gradle clean` 등 |

---

### 🧠 특징 요약

- **성능 최적화**: Incremental Build, Build Cache, Daemon 기반으로 빠름
- **태스크 중심 설계**: 작업 단위로 유연한 빌드 구성 가능
- **스크립트 기반 DSL**: Groovy/Kotlin 언어로 커스터마이징 가능
- **플러그인 구조**: Spring Boot, Android 등 다양한 플러그인 존재

---

### 💡 실무 팁

- `build.gradle.kts`를 사용하면 **정적 타입 검사 가능**
- **멀티 모듈 프로젝트**에서 강력한 성능 발휘
- `--info`, `--debug`, `--scan` 옵션으로 빌드 상태 디버깅
- Jenkins, GitHub Actions 등과 쉽게 연동 가능

---

### 🔗 관련 개념 비교

| 개념 | 설명 |
|------|------|
| [[Gradle]] | 태스크 기반, DSL, 빠르고 유연 |
| [[Maven]] | 선언형, 라이프사이클 기반, 구조적 |
| [[Ant]] | 명령형, 의존성 관리 없음 |
| [[Task]] | Gradle에서 실행되는 작업 단위 |
| [[Plugin]] | Gradle 기능 확장을 위한 모듈화 구성 |
