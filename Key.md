---
type: learn
created: 2025-08-18(월) / 23:25
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-08-18
review_success: false
related_concepts: []
---
---

## ✅ 키(Key)

### 🔤 용어 해석

- Key: 키, 식별자
    
- 👉 **릴레이션 내의 튜플을 유일하게 식별**하기 위한 속성 또는 속성의 집합
    

---

### 🧩 키란?

|항목|설명|
|---|---|
|**정의**|하나의 튜플(행)을 **다른 튜플과 구분하기 위한 기준값**으로 사용되는 속성|
|**목적**|데이터 **식별, 무결성 유지, 참조 연결**|
|**분류**|[[Super Key]], [[Candidate Key]], [[Primary Key]], [[Foreign Key]] 등|

---

### 🧱 주요 키 종류

| 키 종류              | 설명                                          |
| ----------------- | ------------------------------------------- |
| [[Super Key]]     | 유일성을 만족하는 모든 키 후보 (속성이 많아도 허용)              |
| [[Candidate Key]] | Super Key 중 **최소성(불필요한 속성 없음)**을 만족하는 키     |
| [[Primary Key]]   | Candidate Key 중 **대표 키로 선정된 것**, NULL/중복 불가 |
| [[Foreign Key]]   | 다른 릴레이션의 Primary Key를 참조, 참조 무결성 유지         |
| Alternate Key     | Primary로 선택되지 않은 Candidate Key              |
| Composite Key     | 두 개 이상의 속성으로 구성된 키                          |

---

### 📚 예시로 이해하기1

```plaintext
학생(학번, 주민번호, 이름)

- Super Key: {학번}, {주민번호}, {학번+이름}, ...
- Candidate Key: {학번}, {주민번호}
- Primary Key: {학번}
- Foreign Key: 예) dept_code → department.code
```

---

### 📚 예시로 이해하기2

```sql
CREATE TABLE student (
  id INT PRIMARY KEY,           -- Primary Key
  name VARCHAR(50),
  dept_code CHAR(4),
  CONSTRAINT fk_dept FOREIGN KEY (dept_code) REFERENCES department(code) -- Foreign Key
);
```

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|유일성|모든 키는 튜플을 유일하게 식별해야 함|
|최소성|Candidate Key는 최소 조건 만족|
|NULL 여부|Primary Key는 NULL 불가, Foreign Key는 NULL 가능|
|참조 관계|Foreign Key는 다른 테이블의 Primary Key와 연결됨|

---

### 🎯 실무 팁

- **식별자 선택 시 중복 가능성 낮고 의미 있는 값 선택**
    
- 복합키보다 **단일 키 선호**, 불가피할 경우만 복합 구성
    
- Foreign Key 설정 시 **참조 무결성 위반 예외처리 필수**
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Primary Key]]|테이블 고유 식별자 (NOT NULL + UNIQUE)|
|[[Foreign Key]]|다른 테이블을 참조하는 외래 키|
|[[Candidate Key]]|유일성과 최소성 만족, PK 후보|
|[[Super Key]]|유일성만 만족하는 모든 키 집합|

---