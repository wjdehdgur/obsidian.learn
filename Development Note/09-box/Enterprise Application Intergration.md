---
type: learn
created: 2025-08-01(금) / 01:36
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-08-01
review_success: false
related_concepts: []
---
## ✅ EAI (Enterprise Application Integration)

### 🔤 용어 해석  
- [[Enterprise Application Integration|EAI]]: 기업 내의 서로 다른 애플리케이션, 시스템, 데이터 등을 **하나의 통합된 시스템처럼 연결**하여 유기적으로 연동되도록 하는 기술

---

### 📌 개념 정리  
- 기업 내부의 다양한 정보 시스템(ERP, CRM, SCM 등) 간의 **데이터 통합 및 프로세스 연계**를 위한 기술  
- 포인트 투 포인트 연결이 아닌, **허브/버스 구조 기반의 통합 플랫폼**을 통해 시스템 간 **중복 개발 방지, 실시간 연동, 데이터 일관성 확보**가 가능함

---

### ⚙️ 구성 요소  
1. **Adapter**: 개별 애플리케이션과 EAI 플랫폼 간 데이터 포맷 및 통신 규약 변환기  
2. **Platform (EAI Server)**: 통합 처리, 변환, 경로 설정을 담당하는 중앙 허브  
3. **Broker**: 데이터 변환 및 경로 제어 기능 담당  
4. **Monitoring & Management Tool**: 전체 연계 상태 모니터링 및 장애 감지

---

### 🧭 흐름 / 방향성  
1. 시스템 A에서 이벤트 발생  
2. Adapter가 해당 이벤트를 EAI 서버로 전달  
3. EAI 서버에서 다른 시스템 B의 규격에 맞게 변환  
4. Adapter를 통해 시스템 B로 전달  
→ **비동기 또는 동기 처리 가능**

---

### 💬 실무 예시  
- ERP와 물류 시스템 간 실시간 재고 정보 연동  
- POS 시스템과 회계 시스템 간 매출 데이터 자동 전달  
- 보험사 콜센터와 고객 DB 시스템 간 정보 연동

---

### 🔁 관련 개념 비교

| 항목             | EAI                          | ESB (Enterprise Service Bus) |
|------------------|-------------------------------|-------------------------------|
| 구조             | 허브 또는 버스 기반          | 메시지 버스 중심              |
| 통합 범위        | 애플리케이션 중심             | 서비스 중심 (SOA 기반)       |
| 유연성           | 중간                          | 높음                         |
| 사용 기술        | XML, API, Adapter             | Web Service, SOAP, REST 등   |

---

### 🎯 핵심 요약  
- **이기종 시스템 간 통합 및 연동을 위한 미들웨어 플랫폼**  
- Adapter와 Broker 구조를 통해 유연한 데이터 흐름 지원  
- SOA/ESB의 기반이 되는 전통적 통합 아키텍처

---

### 🧠 학습 메모  
- 기출 키워드: “이기종 통합”, “중앙 통합 서버”, “Adapter”, “Broker”  
- ESB와의 비교는 반드시 암기
