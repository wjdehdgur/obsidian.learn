---
type: learn
created: 2025-07-23(수) / 01:23
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

## ✅ DBMS (Database Management System)

### 🔤 용어 해석

- **Database**: 데이터베이스, 구조화된 데이터 모음
    
- **Management**: 관리
    
- **System**: 시스템  
    → 데이터베이스를 **생성, 저장, 수정, 검색, 삭제**하는 소프트웨어
    

---

### 📌 개념 정리

- 사용자와 데이터베이스 사이에서 데이터를 **효율적이고 안전하게 관리**하는 프로그램
    
- **데이터 중복 최소화, 보안 유지, 무결성 보장, 동시 처리 가능**
    
- SQL 같은 언어를 통해 데이터 조작 가능
    

---

### ⚙️ 주요 기능

|기능 구분|설명|
|---|---|
|**정의 기능**|스키마, 테이블 등의 데이터 구조 생성 (`CREATE`, `ALTER`)|
|**조작 기능**|데이터 조회, 삽입, 수정, 삭제 (`SELECT`, `INSERT` 등)|
|**제어 기능**|사용자 권한 관리, 보안 설정 (`GRANT`, `REVOKE`)|
|**무결성 유지**|제약 조건 적용 (PRIMARY KEY, NOT NULL 등)|
|**동시성 제어**|여러 사용자가 동시에 접근할 때 충돌 방지 (트랜잭션 처리)|
|**회복 기능**|장애 발생 시 복구 (Undo, Redo, Log 기반)|

---

### 💬 실무 예시

- 쇼핑몰 DB:
    
    - 상품, 회원, 주문 테이블을 **MySQL DBMS**로 운영
        
    - SQL로 `SELECT * FROM 주문 WHERE 배송상태 = '출고대기';`
        
- PostgreSQL, Oracle, SQL Server 등 다양한 DBMS 존재
    

---

### 🔁 관련 개념 비교

|구분|DB (데이터베이스)|DBMS|
|---|---|---|
|역할|데이터를 저장한 공간|DB를 관리하는 소프트웨어|
|상태|수동적|능동적, 동작 수행|
|예시|테이블, 스키마 등|MySQL, Oracle, SQLite 등|

---

### 🎯 핵심 요약

- **DBMS는 데이터베이스를 조작·제어하는 시스템 소프트웨어**
    
- 사용자와 DB 사이에서 **안정성·보안·성능을 보장**
    
- 모든 DB는 반드시 DBMS 위에서 작동함
    

---

### 🧠 학습 메모

- SQL 기능과 함께 묶어 출제됨 (`DML`, `DDL`, `DCL`, `TCL`)
    
- 트랜잭션 처리, 회복, 보안 기능까지 포함된 종합 시스템임
    
- 시험에서는 DB vs DBMS 차이 자주 물어봄
    

---