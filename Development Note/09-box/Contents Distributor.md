---
type: learn
created: 2025-08-05(화) / 00:44
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
## ✅ 콘텐츠 배포자(Contents Distributor)

### 🔤 용어 해석

- Contents Distributor: 콘텐츠 유통자  
- 👉 [[Contents Distributor]]는 **DRM이 적용된 콘텐츠를 사용자에게 전달하는 유통 역할의 구성 요소**

---

### 🧩 Contents Distributor란?

| 항목 | 설명 |
|------|------|
| **정의** | [[Contents Distributor]]는 [[DRM]] 시스템에서 암호화된 콘텐츠를 **다운로드 또는 스트리밍 방식으로 사용자에게 제공**하는 역할을 수행하는 유통 채널이다. |
| **주요 기능** | DRM 콘텐츠 전달, 다운로드 처리, 스트리밍 전송, 접근 요청 전달 |
| **연계 대상** | [[Packager]], [[DRM Controller]], 사용자 클라이언트 |
| **콘텐츠 형태** | 암호화된 영상(HLS/DASH), 음악 파일, 전자책, 문서 등 |
| **기술 예시** | CDN(Content Delivery Network) 또는 웹 서버 기반의 전송 시스템

---

### 🧠 특징 요약

- **유통 중개자**: 암호화된 콘텐츠 파일을 사용자에게 제공
- **접근 제어 반영**: DRM Controller의 권한 판단에 따라 제공 여부 결정
- **전송 최적화**: CDN과 연동하여 지역별 빠른 콘텐츠 전송 가능

---

### 💡 실무 팁

- OTT 서비스에서는 스트리밍 속도 및 품질 조절(adaptive bitrate)을 위한 HLS/DASH 필수
- DRM 적용 상태를 유지하면서도 네트워크 효율성을 고려한 설계 필요
- 다중 CDN 구조로 글로벌 서비스 대응

---

### 🔗 관련 개념 비교

| 개념 | 설명 |
|------|------|
| [[Contents Distributor]] | 암호화된 콘텐츠를 사용자에게 전달 |
| [[Packager]] | 콘텐츠 암호화 및 포맷 가공 |
| [[DRM Controller]] | 사용자 접근 권한 판단 |
| [[CDN]] | 콘텐츠 전송을 위한 전송 네트워크 |
| [[Streaming Service]] | 콘텐츠 배포와 재생을 포함하는 서비스 구조 |
