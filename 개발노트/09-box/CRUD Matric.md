---
type: learn
created: 2025-07-23(수) / 01:38
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

## ✅ CRUD 매트릭스 (CRUD Matrix)

### 🔤 용어 해석

- **CRUD**:
    
    - **C**reate (생성)
        
    - **R**ead (조회)
        
    - **U**pdate (수정)
        
    - **D**elete (삭제)
        
- → 시스템이 **데이터에 대해 어떤 작업을 수행하는지**를 표로 정리한 것
    

---

### 📌 개념 정리

- **기능(프로세스)**와 **데이터(엔티티)** 간의 **접근 관계**를 매트릭스로 표현
    
- 어떤 기능이 어떤 데이터에 **무슨 연산(C/R/U/D)**을 수행하는지 한눈에 파악 가능
    
- **정보공학 방법론(IE)**에서 사용되는 도구 중 하나
    

---

### ⚙️ 구성 방식

|       | 회원 엔티티 | 주문 엔티티 | 상품 엔티티 |
| ----- | ------ | ------ | ------ |
| 회원 등록 | C      |        |        |
| 회원 조회 | R      |        |        |
| 주문 생성 |        | C      | R      |
| 주문 취소 |        | D      |        |
| 상품 수정 |        |        | U      |

- **행(Row)**: 기능/프로세스
    
- **열(Column)**: 데이터 엔티티
    
- **셀(Cell)**: 해당 기능이 데이터에 하는 작업 (C, R, U, D)
    

---

### 💬 실무 예시

- 쇼핑몰 시스템의 CRUD 매트릭스
    
    - 주문 처리 기능 → 주문(C), 상품(R)
        
    - 재고 수정 기능 → 상품(U)
        
    - 회원 탈퇴 기능 → 회원(D)
        

---

### 🔁 관련 개념 비교

|구분|CRUD 매트릭스|E-R 다이어그램|
|---|---|---|
|초점|**기능과 데이터의 연결**|**데이터 구조와 관계**|
|표현 대상|프로세스 ↔ 데이터 조작|개체 ↔ 개체 간 관계|
|사용 시점|**업무 분석/요구 정리** 단계|**개념적 설계** 단계|

---

### 🎯 핵심 요약

- CRUD 매트릭스는 기능과 데이터 사이의 **처리 관계를 표로 정리**
    
- 기능별로 어떤 데이터에 무슨 조작이 필요한지 명확하게 파악
    
- **요구분석과 시스템 설계 연결 고리** 역할
    

---

### 🧠 학습 메모

- 시험에선 “어떤 도구로 기능-데이터 간 관계를 표현?” → CRUD 매트릭스
    
- 각 셀에 여러 연산이 들어갈 수도 있음 (예: CR, RU 등)
    
- 정보공학 방법론(IE)에서 **중요 도구**로 분류됨
    

---