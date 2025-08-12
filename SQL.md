---
type: learn
created: 2025-08-12(화) / 17:26
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

## ✅ SQL(Structured Query Language)

### 🔤 용어 해석

- SQL: Structured Query Language
    
- 👉 관계형 데이터베이스에서 데이터를 **정의, 조작, 제어, 질의**하기 위한 언어
    

---

### 🧩 SQL이란?

|항목|설명|
|---|---|
|**정의**|[[RDBMS]]에서 데이터 관리를 위한 **표준 질의 언어**|
|**목적**|데이터 생성, 조회, 수정, 삭제, 권한 부여 등 모든 데이터 처리 기능 수행|
|**분류**|[[DDL]], [[DML]], [[DCL]], [[TCL]] 등으로 기능 구분|

---

### 🧱 주요 분류 및 명령어

|분류|기능|대표 명령어|
|---|---|---|
|[[DDL]]|데이터 구조 정의|`CREATE`, `ALTER`, `DROP`|
|[[DML]]|데이터 조회/조작|`SELECT`, `INSERT`, `UPDATE`, `DELETE`|
|[[DCL]]|권한 제어|`GRANT`, `REVOKE`|
|[[TCL]]|트랜잭션 제어|`COMMIT`, `ROLLBACK`, `SAVEPOINT`|

---

### 📚 예시로 이해하기1

- `SELECT name FROM users WHERE age > 30;`  
    → users 테이블에서 나이가 30 초과인 name 컬럼 조회
    

---

### 📚 예시로 이해하기2

```sql
SELECT team, COUNT(*) 
FROM player 
GROUP BY team 
HAVING COUNT(*) >= 3;
```

→ 팀별 선수 수를 세고, 3명 이상인 팀만 출력

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|비절차적 언어|원하는 결과 중심으로 기술|
|ANSI/ISO 표준|다양한 DBMS에서 사용 가능|
|강력한 질의 기능|[[JOIN]], [[GROUP BY]], [[SUBQUERY]] 등|
|보안 제어|`GRANT`, `REVOKE` 등으로 권한 관리 가능|

---

### 🎯 실무 팁

- 성능 고려: **[[Index]] 활용**, `WHERE` 조건 최적화 필요
    
- 뷰([[View]])를 통해 복잡한 쿼리를 단순화
    
- 집계 함수 사용 시 `GROUP BY`와 `HAVING`의 차이 명확히 구분할 것
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[DDL]]|테이블, 인덱스, 뷰 등의 구조 정의|
|[[DML]]|테이블의 실제 데이터 조작|
|[[DCL]]|사용자 권한 부여 및 회수|
|[[TCL]]|트랜잭션 처리 제어 (롤백, 커밋 등)|

---