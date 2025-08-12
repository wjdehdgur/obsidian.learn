---
type: learn
created: 2025-08-12(화) / 17:46
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

## ✅ DCL(Data Control Language)

### 🔤 용어 해석

- DCL: Data Control Language
    
- 👉 [[SQL]]에서 **사용자의 데이터 접근 권한을 제어**하는 언어
    

---

### 🧩 DCL이란?

|항목|설명|
|---|---|
|**정의**|데이터베이스 사용자에게 권한을 **부여하거나 회수**하는 명령어 집합|
|**목적**|데이터 보안 및 사용자 권한 관리|
|**분류**|[[SQL]] 하위 언어 (DDL, DML, DCL, TCL)|

---

### 🧱 주요 명령어

|명령어|설명|
|---|---|
|`GRANT`|특정 객체에 대한 접근 권한 부여|
|`REVOKE`|이전에 부여된 권한 회수|

---

### 📚 예시로 이해하기1

- 관리자가 일반 사용자에게 `SELECT` 권한만 부여
    
- 필요 시 해당 권한을 다시 회수
    

---

### 📚 예시로 이해하기2

```sql
GRANT SELECT, INSERT ON employee TO userA;

REVOKE INSERT ON employee FROM userA;
```

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|보안 중심|데이터 접근 권한을 제어|
|객체 단위 적용|테이블, 뷰, 시퀀스 등에 적용 가능|
|사용자 단위 관리|유저, 롤 단위로 설정|
|DCL 실행 주체|보통 DBA 또는 권한이 있는 사용자만 가능|

---

### 🎯 실무 팁

- 최소 권한 원칙 적용: 필요한 권한만 부여
    
- `WITH GRANT OPTION`: 다른 사용자에게 권한 재부여 가능
    
- 사용자 그룹 단위(롤)로 권한 관리하면 효율적
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[DCL]]|권한 부여 및 회수|
|[[DDL]]|테이블 등의 구조 정의|
|[[DML]]|테이블의 데이터 조작|
|[[TCL]]|트랜잭션 제어 (예: COMMIT, ROLLBACK)|

---