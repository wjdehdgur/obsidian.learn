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
## ✅ 메이븐(Maven)

### 🔤 용어 해석

- Maven: "집중적인 노력"이라는 의미에서 유래한 단어  
- 👉 [[Build Automation Tool|빌드 자동화 도구]]로, **표준화된 구조와 라이프사이클**에 기반하여 빌드, 테스트, 배포를 자동화함

---

### 🧩 Maven이란?

| 항목 | 설명 |
|------|------|
| **정의** | [[Maven]]은 Apache에서 개발한 **라이프사이클 중심의 선언적 빌드 도구**로, XML(`pom.xml`) 파일 기반으로 프로젝트 구조와 빌드 과정을 정의한다. |
| **특징** | Convention over Configuration(설정보다 관례 중심) 철학 적용 |
| **의존성 관리** | 중앙 저장소(Central Repository)를 통한 자동 의존성 관리 |
| **라이프사이클** | `validate`, `compile`, `test`, `package`, `verify`, `install`, `deploy` |
| **사용 예시** | `mvn clean install`, `mvn test`, `mvn package` 등 명령어 사용 |

---

### 🧠 특징 요약

- **표준 구조 강제**: 정형화된 프로젝트 디렉토리 구조 유도
- **자동 의존성 관리**: 버전 지정만으로 JAR 다운로드 가능
- **학습 용이성**: 대중적이고 문서가 풍부함
- **유연성 부족**: 복잡한 커스터마이징은 어렵고, XML이 장황함

---

### 💡 실무 팁

- 팀 프로젝트에서 **구조 통일성 확보**에 적합
- [[Gradle]]과 달리 **선언적 방식**으로 명확하고 안정적
- `pom.xml`은 하나의 [[Dependency Management]] 허브 역할
- Jenkins 연동 시 `mvn test`, `mvn package` 등으로 자동화 가능

---

### 🔗 관련 개념 비교

| 개념 | 설명 |
|------|------|
| [[Maven]] | 선언형, 라이프사이클 기반, XML 구성 |
| [[Gradle]] | 스크립트 기반, 유연하고 빠름 |
| [[Ant]] | 명령어 나열형, 의존성 관리 없음 |
| [[pom.xml]] | Maven 설정 파일로, 의존성, 플러그인, 메타 정보 포함 |
| [[Repository]] | Maven 중앙 저장소 또는 로컬 캐시 공간 |
