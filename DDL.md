---
type: learn
created: 2025-08-12(화) / 17:44
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

## ✅ DDL(Data Definition Language)

### 🔤 용어 해석

- DDL: Data Definition Language
    
- 👉 [[SQL]]에서 **데이터베이스 객체의 구조를 정의, 변경, 삭제**하는 언어
    

---

### 🧩 DDL이란?

|항목|설명|
|---|---|
|**정의**|테이블, 인덱스, 뷰 등 **데이터베이스 객체의 스키마를 정의하거나 조작**하는 명령어 집합|
|**목적**|구조 설계 및 관리|
|**분류**|[[SQL]]의 하위 언어 (DDL, DML, DCL, TCL)|

---

### 🧱 주요 명령어

|명령어|설명|
|---|---|
|`CREATE`|테이블, 뷰, 인덱스 등 객체 생성|
|`ALTER`|기존 객체의 구조 수정 (컬럼 추가, 변경 등)|
|`DROP`|객체 완전 삭제|
|`TRUNCATE`|테이블 데이터 전부 삭제 (구조는 유지)|

---

### 📚 예시로 이해하기1

- `CREATE TABLE`을 통해 테이블 구조 정의
    
- `ALTER TABLE`로 컬럼 추가
    
- `DROP TABLE`로 테이블 자체 삭제
    

---

### 📚 예시로 이해하기2

```sql
CREATE TABLE employee (
  id INT PRIMARY KEY,
  name VARCHAR(50)
);

ALTER TABLE employee ADD hire_date DATE;

DROP TABLE employee;
```

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|자동 커밋|실행 즉시 변경 내용 저장됨 (`ROLLBACK` 불가)|
|구조 중심|데이터가 아닌 **객체 구조**를 다룸|
|권한 필요|일반 사용자보다 높은 권한 필요|
|복구 불가|DROP, TRUNCATE는 되돌릴 수 없음|

---

### 🎯 실무 팁

- DDL 실행 전 **백업 필수**
    
- 테스트 환경에서 구조 변경 후 운영 적용
    
- `DROP`은 신중히 사용, 보통은 `ALTER`로 변경 처리
    
- 개발 초기에는 `CREATE`, 운영 중에는 `ALTER` 사용 빈도 높음
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[DDL]]|데이터 구조 정의 및 변경|
|[[DML]]|데이터 조회 및 조작|
|[[DCL]]|권한 부여 및 회수|
|[[TCL]]|트랜잭션 처리 제어 (COMMIT, ROLLBACK)|

---