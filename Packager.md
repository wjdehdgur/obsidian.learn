---
type: learn
created: 2025-08-05(화) / 00:43
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
## ✅ 패키저(Packager)

### 🔤 용어 해석

- Packager: 패키징 도구, 포장기  
- 👉 [[Packager]]는 **디지털 콘텐츠에 DRM을 적용하고, 암호화 및 메타데이터를 삽입하는 구성 요소**

---

### 🧩 Packager란?

| 항목 | 설명 |
|------|------|
| **정의** | [[Packager]]는 [[DRM]] 시스템 내에서 콘텐츠를 **암호화하고, 식별자 및 라이선스 정보 같은 메타데이터를 삽입**하여 유통 가능한 형태로 가공하는 역할을 수행한다. |
| **주요 기능** | 콘텐츠 암호화, 메타데이터 삽입, 포맷 변환 |
| **연계 대상** | [[DRM Controller]], [[Clearing House]], [[Contents Distributor]] |
| **처리 대상** | 영상 스트림(MP4, HLS, DASH 등), 문서(PDF), 오디오(MP3 등) |
| **기술 예시** | MPEG-CENC(Common Encryption), FairPlay, Widevine, PlayReady 암호화 방식 사용

---

### 🧠 특징 요약

- **DRM 암호화 핵심**: 콘텐츠 자체를 암호화하여 불법 복제 방지
- **메타데이터 포함**: 콘텐츠 ID, 만료일, 사용자 제한 정보 포함
- **포맷 대응 필요**: 스트리밍(HLS, DASH 등) 특화 포맷으로 변환 가능

---

### 💡 실무 팁

- 영상 DRM 적용 시 Packager가 스트림을 HLS/DASH로 분할 및 암호화
- 교육 콘텐츠에서는 슬라이드 자료(PDF)도 암호화 가능
- [[Jenkins]]와 연동하여 자동 빌드-패키징 파이프라인 구축 가능

---

### 🔗 관련 개념 비교

| 개념 | 설명 |
|------|------|
| [[Packager]] | 콘텐츠 암호화 및 메타데이터 삽입 |
| [[DRM Controller]] | 접근 정책 및 권한 통제 |
| [[Clearing House]] | 사용 기록 및 정산 관리 |
| [[Contents Distributor]] | 암호화된 콘텐츠 유통 담당 |
| [[Encryption]] | Packager가 수행하는 기술적 핵심 작업 |
