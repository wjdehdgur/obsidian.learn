---
type: learn
created: 2025-08-12(화) / 21:02
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

## ✅ TCL(Transaction Control Language)

### 🔤 용어 해석

- TCL: Transaction Control Language
    
- 👉 [[SQL]]에서 **트랜잭션의 시작, 저장, 완료, 복구를 제어**하는 명령어 집합
    

---

### 🧩 TCL이란?

|항목|설명|
|---|---|
|**정의**|[[Transaction]]의 수행 결과를 **DB에 확정하거나 되돌리는** 명령어로 구성된 제어 언어|
|**목적**|트랜잭션의 **정합성, 안정성, 복구 가능성** 확보|
|**분류**|[[SQL]]의 하위 언어 (DDL, DML, DCL, TCL)|

---

### 🧱 주요 명령어

|명령어|설명|
|---|---|
|`COMMIT`|트랜잭션의 모든 작업을 영구 저장|
|`ROLLBACK`|트랜잭션 수행 도중의 변경 내용을 취소|
|`SAVEPOINT`|트랜잭션 내 특정 시점 저장, 이후 해당 지점까지 ROLLBACK 가능|
|`SET TRANSACTION`|트랜잭션 속성(격리 수준 등) 설정|

---

### 📚 예시로 이해하기1

```plaintext
1. 재고 차감  
2. 주문 정보 저장  
3. 결제 실패 발생  
→ ROLLBACK으로 전체 트랜잭션 취소
```

---

### 📚 예시로 이해하기2

```sql
BEGIN;
UPDATE stock SET qty = qty - 1 WHERE item_id = 'A01';
SAVEPOINT step1;
INSERT INTO order VALUES (...);
ROLLBACK TO step1;
COMMIT;
```

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|트랜잭션 제어|실행, 취소, 저장 시점 관리|
|ROLLBACK|오류 발생 시 전체 또는 일부 취소|
|SAVEPOINT|다단계 트랜잭션 복구 처리에 유리|
|COMMIT|커밋 후에는 [[Durability]] 보장됨|

---

### 🎯 실무 팁

- 트랜잭션 단위로 COMMIT/ROLLBACK을 명확히 구분
    
- 긴 작업일수록 SAVEPOINT 적극 활용
    
- `SET TRANSACTION ISOLATION LEVEL`로 [[Isolation]] 수준 조정 가능
    
- 트랜잭션 누락 → 데이터 불일치, 중복 입력 위험
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[TCL]]|트랜잭션 제어 언어|
|[[DML]]|데이터를 조작하는 명령어|
|[[ACID]]|트랜잭션이 만족해야 할 4가지 특성|
|[[Rollback]]|TCL 명령 중 하나, 작업 취소 역할|

---