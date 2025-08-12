---
type: learn
created: 2025-08-12(화) / 20:58
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

## ✅ 트랜잭션(Transaction)

### 🔤 용어 해석

- Transaction: 거래, 처리 단위
    
- 👉 데이터베이스에서 **하나의 논리적 작업 단위를 구성하는 최소 실행 단위**
    

---

### 🧩 트랜잭션이란?

|항목|설명|
|---|---|
|**정의**|데이터베이스에서 여러 연산을 하나의 작업 단위로 묶어 **모두 성공하거나 모두 실패해야 하는 처리 단위**|
|**목적**|데이터 무결성 유지, 오류 발생 시 전체 작업 원자적으로 복구|
|**분류**|[[TCL]]의 주요 적용 대상 (COMMIT, ROLLBACK 등)|

---

### 🧱 상태 변화 단계

|상태|설명|
|---|---|
|Active|트랜잭션 실행 중|
|Partially Committed|마지막 명령 실행 완료, COMMIT 대기|
|Committed|성공적으로 완료되어 변경 사항 확정|
|Failed|중간 오류 발생|
|Aborted|전체 작업 취소, ROLLBACK 수행됨|

---

### 📚 예시로 이해하기1

- 계좌 이체: A → B로 100만원 이체
    
    - A 잔액 차감
        
    - B 잔액 증가  
        → 둘 다 성공해야만 트랜잭션 완료, 하나라도 실패 시 ROLLBACK
        

---

### 📚 예시로 이해하기2

```sql
BEGIN;
UPDATE account SET balance = balance - 100 WHERE id = 'A';
UPDATE account SET balance = balance + 100 WHERE id = 'B';
COMMIT;
```

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|[[Atomicity]]|전부 수행 또는 전부 취소|
|[[Consistency]]|실행 전후 상태가 일관성 유지|
|[[Isolation]]|트랜잭션 간 간섭 금지|
|[[Durability]]|COMMIT 후에는 영구 반영|

---

### 🎯 실무 팁

- 트랜잭션 중에는 **자동 커밋 방지** 설정 확인
    
- 복잡한 로직일수록 **예외 처리와 ROLLBACK 전략** 중요
    
- [[Lock]] 및 [[Isolation Level]] 설정은 동시성 처리에 직접 영향
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Transaction]]|논리적 작업 단위|
|[[ACID]]|트랜잭션의 네 가지 특성|
|[[TCL]]|트랜잭션 제어 언어 (COMMIT, ROLLBACK 등)|
|[[Concurrency Control]]|다중 사용자 동시 작업 시 충돌 방지 기법|

---