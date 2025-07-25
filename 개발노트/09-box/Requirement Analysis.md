---
type: learn
created: 2025-07-23(수) / 01:13
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-07-23
review_success: false
related_concepts: []
---
---

## ✅ 요구사항 분석 (Requirement Analysis)

### 🔤 용어 해석

- **Requirement**: 요구, 필요 조건
    
- **Analysis**: 분석, 구조화  
    → 사용자의 요구를 **정확히 이해하고 문서화하는 작업**
    

---

### 📌 개념 정리

- 시스템이 **무엇을 해야 하는지**를 이해하고 정리하는 과정
    
- 고객/사용자가 원하는 기능과 제약 조건을 **개발자가 이해할 수 있도록 구체화**
    
- 개발 전 가장 중요한 단계. 잘못되면 전체 프로젝트에 영향
    

---

### ⚙️ 구성 요소

|구분|설명|
|---|---|
|기능적 요구|시스템이 **무엇을 해야 하는가**에 대한 요구 (예: 로그인 기능)|
|비기능적 요구|성능, 보안, 품질, 제약 조건 등 (예: 응답시간 3초 이내, 암호화)|
|사용자 요구|고객이 직접 말하는 니즈나 목적 (자연어 기반, 구체적이지 않을 수 있음)|
|시스템 요구|사용자 요구를 **구체적인 시스템 기능과 동작**으로 변환한 것|

---

### 🧭 흐름 / 절차

1. **요구사항 수집**
    
    - 인터뷰, 설문, 문서 분석 등으로 사용자/이해관계자 의견 수집
        
2. **요구사항 분석**
    
    - 요구의 **충돌, 중복, 누락 여부 검토**
        
    - 기능 / 비기능 요구로 분류
        
3. **요구사항 명세(Specification)**
    
    - 자연어를 UML, 유스케이스, 명세서 등으로 문서화
        
4. **요구사항 검증**
    
    - 요구사항이 **명확하고 일관되며 현실적인지** 확인
        
    - 사용자가 확인하고 서명
        

---

### 💬 실무 예시

- 고객: “결제를 빠르게 하고 싶어요”  
    → 기능적 요구: 결제 API 연동  
    → 비기능 요구: 3초 이내 응답, 실패율 1% 미만  
    → 분석 결과: `결제 기능`, `에러 처리`, `로딩 표시`
    

---

### 🔁 관련 개념 비교

| 구분     | 요구사항 분석                                                            | 설계 단계                               |
| ------ | ------------------------------------------------------------------ | ----------------------------------- |
| 중심 질문  | 무엇을 해야 하는가?                                                        | 어떻게 구현할 것인가?                        |
| 주요 결과물 | [[Use Case Diagram\|유스케이스]], [[Requirement Specification\|요구 명세서]] | 구조도, [[Class Diagram\|클래스 다이어그램]] 등 |
| 시점     | 개발 초기                                                              | 분석 후, 구현 전                          |

---

### 🎯 핵심 요약

- 요구사항 분석은 **무엇을 만들 것인지 정확히 정의하는 단계**
    
- 기능/비기능 요구로 구분
    
- 사용자의 말을 시스템 언어로 바꾸는 **해석 + 정리 과정**
    

---

### 🧠 학습 메모

- 시험에서는 “비기능적 요구 vs 기능적 요구” 구분 자주 출제
    
- `요구사항 검증 = 일관성/완전성/현실성 체크`
    
- `요구사항 명세 = 문서화 단계`, `도출 = 수집 단계`
    

---