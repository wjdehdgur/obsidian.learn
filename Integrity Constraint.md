---
type: learn
created: 2025-08-12(화) / 21:09
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

## ✅ 무결성 제약조건(Integrity Constraint)

### 🔤 용어 해석

- Integrity: 무결성, 정합성
    
- Constraint: 제약조건
    
- 👉 [[RDBMS]]에서 **데이터의 정확성, 일관성, 유효성**을 보장하기 위한 규칙
    

---

### 🧩 무결성 제약조건이란?

| 항목     | 설명                                                            |
| ------ | ------------------------------------------------------------- |
| **정의** | 데이터 입력, 수정, 삭제 시 **비정상적이거나 불일치된 값이 저장되지 않도록 강제하는 규칙**         |
| **목적** | 데이터의 신뢰성과 정합성 보장                                              |
| **분류** | [[개체 무결성]], [[참조 무결성]], [[도메인 무결성]], [[고유 제약조건]], [[체크 제약조건]] |

---

### 🧱 주요 제약조건 종류

| 종류                        | 설명                                      |
| ------------------------- | --------------------------------------- |
| [[Entity Integrity]]      | 기본키(PK)는 `NULL`이거나 중복되면 안 됨             |
| [[Referential Integrity]] | 외래키(FK)는 참조하는 기본키 값과 일치하거나 `NULL`이어야 함  |
| [[Domain Integrity]]      | 속성은 정의된 도메인(데이터형, 길이, 값 범위 등)을 벗어나면 안 됨 |
| [[UNIQUE]]                | 중복 불가, 단 `NULL`은 허용                     |
| [[CHECK]]                 | 컬럼의 값이 조건식에 맞는지 검사                      |
| [[NOT NULL]]              | `NULL` 값 입력 불가                          |

---

### 📚 예시로 이해하기1

```plaintext
- 학생 테이블의 학번(PK): NULL ❌, 중복 ❌  
- 외래키 dept_code → 학과 테이블의 dept_code와 반드시 일치하거나 NULL
```

---

### 📚 예시로 이해하기2

```sql
CREATE TABLE student (
  id INT PRIMARY KEY,           -- 개체 무결성
  name VARCHAR(50) NOT NULL,    -- NOT NULL 제약
  dept_code CHAR(4),
  CONSTRAINT fk_dept FOREIGN KEY (dept_code) REFERENCES department(code) -- 참조 무결성
);
```

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|데이터 품질 유지|잘못된 입력 방지|
|자동 강제|DBMS가 제약조건 위반 시 오류 반환|
|설계 단계 반영|제약조건은 테이블 생성 시 정의|
|다양한 유형 존재|구조, 관계, 데이터 수준까지 제어 가능|

---

### 🎯 실무 팁

- **기본키에는 NULL 절대 불가**, 외래키는 NULL 허용 가능
    
- NOT NULL + UNIQUE → 사실상 단일 후보키
    
- 제약조건 이름 명시(`CONSTRAINT 이름`) 시 유지보수 편리
    
- 복잡한 유효성 검사 → [[CHECK]], 간단한 유일성 → [[UNIQUE]]
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Primary Key]]|개체 무결성 보장 핵심 키|
|[[Foreign Key]]|참조 무결성 보장용 외래 키|
|[[Domain]]|도메인 무결성에서 속성 값의 범위 정의|
|[[Constraint]]|무결성 제약조건들의 총칭|

---