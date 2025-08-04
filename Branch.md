---
type: learn
created: 2025-08-04(월) / 23:36
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-08-04
review_success: false
related_concepts: []
---
## ✅ 브랜치(Branch)

### 🔤 용어 해석

- Branch: 가지, 분기  
- 👉 독립적으로 작업을 진행할 수 있도록 **프로젝트의 흐름을 분기**하는 기능

---

### 🧩 브랜치란?

| 항목 | 설명 |
|------|------|
| **정의** | [[Branch]]는 버전 관리 시스템(Git 등)에서 **기존 코드와 분리된 독립된 작업 공간**을 생성하여 병렬 개발을 가능하게 하는 구조이다. |
| **목적** | 새로운 기능 개발, 버그 수정, 실험 등을 메인 코드에 영향 없이 진행 |
| **기본 브랜치 예시** | `main`, `master`, `develop` |
| **작업 브랜치 예시** | `feature/login`, `bugfix/header`, `hotfix/payment` 등 |
| **활용 도구** | [[Git]], SVN, Mercurial 등에서 사용 가능 |

---

### 🧠 특징 요약

- **병렬 개발 가능**: 여러 사람이 동시에 다른 기능 개발 가능
- **충돌 최소화**: 메인 브랜치에 영향을 주지 않고 실험 가능
- **병합(Merge) 기반**: 작업 완료 후 메인 브랜치로 병합하는 구조

---

### 💡 실무 팁

- Git 브랜치 생성: `git branch 브랜치명` 또는 `git checkout -b 브랜치명`
- 브랜치 전략 추천:
  - `main` (배포용), `develop` (통합 개발), `feature/*`, `hotfix/*`, `release/*`
- Pull Request(PR) 기반으로 병합 시 코드 리뷰 필수

---

### 🔗 관련 개념 비교

| 개념 | 설명 |
|------|------|
| [[Branch]] | 독립된 작업 흐름을 위한 분기 |
| [[Merge]] | 브랜치의 변경 내용을 다른 브랜치에 통합 |
| [[Tag]] | 특정 시점(예: 배포 버전 등)을 명확히 식별 |
| [[Versioning]] | 버전 식별 및 관리 방식 |
| [[Fork]] | 원본 저장소를 통째로 복사해 독립적으로 사용하는 Git 방식 |
