---
type: learn
created: 2025-08-12(화) / 21:10
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

## ✅ 개체 무결성(Entity Integrity)

### 🔤 용어 해석

- Entity: 개체, 엔터티
    
- Integrity: 무결성
    
- 👉 테이블의 **각 행(Row)은 반드시 유일하게 식별 가능**해야 함
    

---

### 🧩 개체 무결성이란?

|항목|설명|
|---|---|
|**정의**|기본키(PK)는 **NULL이거나 중복될 수 없으며**, 테이블의 각 튜플을 **유일하게 식별**해야 한다는 제약조건|
|**목적**|엔터티(행)의 식별성과 정확성 확보|
|**분류**|[[무결성 제약조건]] 중 하나, 필수 조건|

---

### 🧱 적용 방식

|요소|조건|
|---|---|
|기본키(PK)|반드시 NOT NULL + UNIQUE|
|중복 금지|동일한 키값이 존재할 수 없음|
|NULL 금지|식별 불가능한 행은 존재 불가|

---

### 📚 예시로 이해하기1

```plaintext
학생 테이블  
학번(PK) 컬럼이 중복되거나 NULL이면 개체 무결성 위반

(1001, 홍길동)  
(1001, 이몽룡) → ❌ 중복된 PK  
(NULL, 성춘향) → ❌ 식별 불가
```

---

### 📚 예시로 이해하기2

```sql
CREATE TABLE student (
  id INT PRIMARY KEY,     -- 개체 무결성 보장: NOT NULL + UNIQUE
  name VARCHAR(50)
);
```

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|핵심 키 제약|[[Primary Key]]를 통해 강제|
|중복 불가|테이블 내 유일 식별 보장|
|NULL 금지|행을 식별할 수 없는 상태 방지|
|DB 설계 기본|모든 테이블은 개체 무결성 필요|

---

### 🎯 실무 팁

- PK 설정이 없으면 DB 구조가 **비정상 설계**
    
- 식별자 컬럼을 반드시 명시하고 **중복/NULL 검사 필수**
    
- PK 복합키일 경우 각 컬럼 조합이 유일해야 함
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Entity Integrity]]|PK는 NULL/중복 불가|
|[[Referential Integrity]]|FK는 참조 무결성 보장|
|[[Primary Key]]|개체 무결성을 위한 도구|
|[[Unique]]|중복 금지 제약, NULL은 허용 가능|

---