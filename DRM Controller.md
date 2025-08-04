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
## ✅ DRM 컨트롤러(DRM Controller)

### 🔤 용어 해석

- DRM Controller: 디지털 권한 관리 제어기  
- 👉 [[DRM Controller]]는 **콘텐츠에 대한 사용 정책과 접근 권한을 중앙에서 제어하는 핵심 제어 모듈**

---

### 🧩 DRM Controller란?

| 항목 | 설명 |
|------|------|
| **정의** | [[DRM Controller]]는 [[DRM]] 시스템 내에서 **콘텐츠 사용 권한을 판단하고, 사용자 요청에 따라 접근을 허가 또는 제한하는 정책 제어 장치**이다. |
| **주요 역할** | 콘텐츠 사용 허용/거부 판단, 정책 적용, 사용자 권한 검사 |
| **연계 대상** | [[Clearing House]], [[Packager]], [[Contents Distributor]], 클라이언트 단말 등 |
| **통제 요소** | 사용자 인증, 콘텐츠 유형, 기간/횟수 제한, 디바이스 허용 여부 등 |
| **기술 예시** | JWT 토큰 발급, 접근 토큰 검증, 정책 기반 룰 처리

---

### 🧠 특징 요약

- **DRM 정책 집행자**: "이 사용자가 이 콘텐츠를 사용할 수 있는가?"를 결정
- **중앙 제어 기반**: DRM 시스템의 핵심 로직이 집중됨
- **콘텐츠 접근 제어**: 단말/기간/지역 제한 등 다양한 조건을 적용 가능

---

### 💡 실무 팁

- OTT, eBook 등에서 사용권 제한 (예: 3일 시청, 1개 디바이스) 구현에 핵심 역할
- 정책 변경 시에는 [[Clearing House]] 및 사용자 클라이언트와 동기화 필요
- 일반적으로 별도 API 서버 또는 마이크로서비스 형태로 구현됨

---

### 🔗 관련 개념 비교

| 개념 | 설명 |
|------|------|
| [[DRM Controller]] | 콘텐츠 접근 정책과 사용 권한 제어 담당 |
| [[Clearing House]] | 사용 내역 기록 및 정산 처리 |
| [[Packager]] | 콘텐츠 암호화 및 메타데이터 삽입 |
| [[Contents Distributor]] | DRM 적용 콘텐츠 유통 담당 |
| [[Access Control]] | 시스템 전반의 접근 제어 모델 (RBAC, ABAC 등) |
