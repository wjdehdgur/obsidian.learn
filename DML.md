---
type: learn
created: 2025-08-12(화) / 17:45
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

## ✅ DML(Data Manipulation Language)

### 🔤 용어 해석

- DML: Data Manipulation Language
    
- 👉 [[SQL]]에서 **테이블의 데이터를 조회하거나 조작하는 명령어 집합**
    

---

### 🧩 DML이란?

|항목|설명|
|---|---|
|**정의**|테이블에 저장된 데이터를 **조회(읽기), 삽입, 수정, 삭제**하는 명령어 집합|
|**목적**|데이터 레코드의 실질적인 관리|
|**분류**|[[SQL]] 하위 언어 중 하나 (DDL, DML, DCL, TCL)|

---

### 🧱 주요 명령어

|명령어|설명|
|---|---|
|`SELECT`|데이터 조회|
|`INSERT`|데이터 삽입|
|`UPDATE`|기존 데이터 수정|
|`DELETE`|데이터 삭제|

---

### 📚 예시로 이해하기1

- 사원 테이블에서 "홍길동"의 정보를 조회하거나 수정/삭제하는 행위는 모두 DML
    

---

### 📚 예시로 이해하기2

```sql
SELECT * FROM employee;

INSERT INTO employee (id, name) VALUES (1, '홍길동');

UPDATE employee SET name = '이몽룡' WHERE id = 1;

DELETE FROM employee WHERE id = 1;
```

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|트랜잭션 대상|`COMMIT`, `ROLLBACK` 가능 (자동 저장 아님)|
|실행 대상|테이블의 **데이터(행)**|
|WHERE 절 중요|조건 없이 실행 시 전체 행 영향 가능|
|권한 필요|INSERT/UPDATE/DELETE는 별도 권한 필요|

---

### 🎯 실무 팁

- 반드시 `WHERE` 조건을 명확히 설정
    
- 변경 전 `SELECT`로 대상 확인 후 실행
    
- 대량 조작 시 `TRANSACTION` 처리 필수
    
- `SELECT`는 가장 많이 사용되는 SQL 문장
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[DML]]|테이블의 행(데이터)을 조작|
|[[DDL]]|테이블 등의 구조(스키마)를 정의|
|[[DCL]]|권한 관리|
|[[TCL]]|트랜잭션 처리 (`COMMIT`, `ROLLBACK`)|

---