---
type: learn
created: 2025-08-05(화) / 00:25
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
## ✅ 젠킨스(Jenkins)

### 🔤 용어 해석

- Jenkins: Hudson에서 파생된 오픈소스 자동화 서버  
- 👉 [[CI/CD]] 파이프라인 구현을 위한 **자동화 빌드·테스트·배포 도구**

---

### 🧩 Jenkins란?

| 항목 | 설명 |
|------|------|
| **정의** | [[Jenkins]]는 소프트웨어 개발에서 빌드, 테스트, 배포 등 일련의 과정을 **자동으로 실행**하기 위해 사용하는 오픈소스 [[CI/CD]] 서버이다. |
| **주요 기능** | 자동 빌드, 테스트, 배포, 스케줄링, 알림 연동, 플러그인 기반 확장 |
| **지원 도구** | [[Git]], [[Gradle]], [[Maven]], [[Docker]], [[Slack]] 등과 통합 가능 |
| **사용 언어** | Java 기반 (웹 UI 제공) |
| **실행 방식** | Job 단위 정의 → 트리거 조건 설정(Cron, Git push 등) → 빌드 실행

---

### 🧠 특징 요약

- **자동화 중심**: 수동 작업을 줄이고, 배포 품질과 일관성을 보장
- **플러그인 기반 구조**: 수백 개의 플러그인을 통해 다양한 환경 통합
- **분산 빌드**: 마스터-에이전트 구조로 병렬 처리 가능
- **UI + 코드 정의 가능**: Declarative/Scripted Pipeline 방식으로 정의 가능

---

### 💡 실무 팁

- **Pipeline as Code**: `Jenkinsfile`에 CI 파이프라인 명시 → Git에 함께 버전 관리
- 배포 자동화 예시: GitHub push → Jenkins 빌드 → 테스트 → Docker 이미지 배포
- Slack, 메일 등으로 **빌드 결과 알림** 연동 필수
- [[Docker]] 기반으로 Jenkins 서버 구성하면 유지보수 용이

---

### 🔗 관련 개념 비교

| 개념 | 설명 |
|------|------|
| [[Jenkins]] | CI/CD 서버, Job/Pipeline 기반 자동화 |
| [[GitHub Actions]] | GitHub 통합 CI 도구 |
| [[Build Automation Tool]] | Jenkins가 제어하는 외부 빌드 도구 (Gradle, Maven 등) |
| [[Pipeline]] | 빌드·테스트·배포 과정을 정의한 Jenkins 프로세스 |
| [[Webhook]] | Git 이벤트(예: push)를 Jenkins에 알리는 트리거 방식 |
