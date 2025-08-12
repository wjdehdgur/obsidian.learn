---
type: learn
created: 2025-08-12(화) / 21:00
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

## ✅ 격리성(Isolation)

### 🔤 용어 해석

- Isolation: 격리, 독립
    
- 👉 **트랜잭션이 수행되는 동안 다른 트랜잭션과의 간섭 없이 독립적으로 실행**되어야 함
    

---

### 🧩 격리성이란?

|항목|설명|
|---|---|
|**정의**|여러 트랜잭션이 동시에 실행될 때, 각 트랜잭션이 **다른 트랜잭션의 중간 상태를 볼 수 없도록 격리하는 성질**|
|**목적**|동시 실행 시 **정합성 및 무결성 보장**|
|**분류**|[[ACID]]의 세 번째 특성|

---

### 🧱 트랜잭션 격리 수준 (Isolation Level)

|수준|설명|
|---|---|
|READ UNCOMMITTED|다른 트랜잭션의 변경사항을 커밋 전에도 읽을 수 있음 (Dirty Read 발생)|
|READ COMMITTED|커밋된 데이터만 읽을 수 있음 (Non-repeatable Read 발생 가능)|
|REPEATABLE READ|한 트랜잭션 내 동일 쿼리는 동일 결과 (Phantom Read 발생 가능)|
|SERIALIZABLE|완전한 격리, 트랜잭션 직렬 처리 (가장 안전하지만 성능 낮음)|

---

### 📚 예시로 이해하기1

```plaintext
A 트랜잭션이 UPDATE 중인데  
→ B 트랜잭션이 중간 데이터를 SELECT해서 사용 → 비일관성 발생

→ 격리성 미보장 상태
```

---

### 📚 예시로 이해하기2

```sql
SET TRANSACTION ISOLATION LEVEL REPEATABLE READ;

BEGIN;
SELECT * FROM account WHERE id = 'A';
-- 다른 트랜잭션이 UPDATE 해도 읽은 값은 유지됨
COMMIT;
```

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|독립 실행|트랜잭션 간 간섭 차단|
|동시성 제어|[[Lock]], [[MVCC]] 등의 기법 사용|
|성능 ↔ 안정성|격리 수준 높을수록 안정성 증가, 성능 저하|
|오류 방지|Dirty Read, Phantom Read, Non-repeatable Read 예방|

---

### 🎯 실무 팁

- 실무에서는 대부분 `READ COMMITTED` 또는 `REPEATABLE READ` 사용
    
- **성능과 안정성 균형 고려하여 격리 수준 선택**
    
- [[Lock]] 충돌이나 데드락 감지 기능 확인 필요
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Isolation]]|트랜잭션 독립 실행 보장|
|[[Atomicity]]|트랜잭션 전체 성공/실패 단위|
|[[Durability]]|커밋 후 영구 반영|
|[[Concurrency Control]]|동시성 문제 해결 위한 기법들|

---