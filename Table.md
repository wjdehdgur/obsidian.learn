---
type: learn
created: 2025-08-12(화) / 17:42
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-08-12
review_success: false
related_concepts: []
---
---

## ✅ 테이블(Table)

### 🔤 용어 해석

- Table: 표, 표 형식 구조
    
- 👉 [[RDBMS]]에서 데이터를 **행(Row)과 열(Column)**의 구조로 저장하는 기본 단위
    

---

### 🧩 테이블이란?

| 항목     | 설명                                             |
| ------ | ---------------------------------------------- |
| **정의** | 데이터를 **2차원 구조(행과 열)**로 구성하여 저장하는 가장 기본적인 저장 단위 |
| **목적** | 데이터를 구조화하여 저장하고, 효율적으로 관리 및 검색                 |
| **분류** | [[Base Table]], [[View]], [[Temporary Table]]  |

---

### 🧱 주요 구성 요소

|구성 요소|설명|
|---|---|
|컬럼(Column)|속성, 필드명 (ex: 이름, 나이 등)|
|행(Row, Tuple)|실제 데이터 한 건|
|스키마(Schema)|테이블의 구조와 제약조건 정의|
|키(Key)|[[Primary Key]], [[Foreign Key]], [[Candidate Key]] 등|

---

### 📚 예시로 이해하기1

- 학생 테이블  
    | 학번 | 이름 | 전공 |  
    |------|------|------|  
    | 1001 | 홍길동 | 컴퓨터공학 |  
    | 1002 | 이몽룡 | 전자공학 |
    

---

### 📚 예시로 이해하기2

```sql
CREATE TABLE student (
  id INT PRIMARY KEY,
  name VARCHAR(50),
  major VARCHAR(50)
);
```

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|정형 데이터|명확한 컬럼 정의와 타입 필요|
|무결성 제약|NOT NULL, UNIQUE, PRIMARY KEY 등 설정 가능|
|관계 정의|[[Foreign Key]]로 테이블 간 관계 구성|
|공간 차지|물리적 공간을 사용 (뷰는 사용하지 않음)|

---

### 🎯 실무 팁

- [[Index]] 설정을 통해 성능 최적화
    
- 컬럼 수는 가독성과 성능을 고려해 최소화
    
- 정규화된 구조 → 필요 시 비정규화로 성능 조정
    
- 필드명/타입/제약조건은 설계 단계에서 명확히 정의
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Table]]|실제 데이터를 저장하는 기본 구조|
|[[View]]|SELECT 결과를 저장하지 않는 가상 테이블|
|[[Temporary Table]]|세션 또는 쿼리 실행 동안만 존재하는 임시 테이블|
|[[Materialized View]]|SELECT 결과를 저장하는 뷰의 특수 형태|

---