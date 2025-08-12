---
type: learn
created: 2025-08-12(화) / 20:59
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

## ✅ 원자성(Atomicity)

### 🔤 용어 해석

- Atomic: 원자적인, 더 이상 나눌 수 없는
    
- 👉 [[Transaction]] 내 작업은 **모두 수행되거나 전혀 수행되지 않아야 함**
    

---

### 🧩 원자성이란?

|항목|설명|
|---|---|
|**정의**|트랜잭션 내의 연산이 **부분적으로 실행되거나 중간에 멈추는 일 없이**, 모두 실행되거나 모두 무효 처리되어야 하는 성질|
|**목적**|오류 발생 시 데이터 일관성 보장 및 **부분 갱신 방지**|
|**분류**|[[ACID]]의 첫 번째 속성|

---

### 🧱 적용 방식

|방법|설명|
|---|---|
|ROLLBACK|트랜잭션 중 오류 발생 시 모든 작업 취소|
|로그 기록|Undo/Redo 로그를 기반으로 작업 복원 또는 무효화|
|장애 복구|시스템 실패 시 트랜잭션 복원 또는 제거 가능|

---

### 📚 예시로 이해하기1

```plaintext
계좌 이체 트랜잭션
1. A 계좌 -100만원  
2. B 계좌 +100만원

→ 중간에 오류 발생 시 전체 취소 (A 계좌도 복원됨)
```

---

### 📚 예시로 이해하기2

```sql
BEGIN;
UPDATE account SET balance = balance - 100 WHERE id = 'A';
-- 오류 발생
UPDATE account SET balance = balance + 100 WHERE id = 'B';
ROLLBACK; -- 모든 작업 취소
```

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|전체 성공 or 전체 실패|중간 상태 없음|
|예외 발생 시 취소|부분 결과 저장 불가|
|ROLLBACK과 밀접|무조건 전 단계로 되돌림|
|일관성 유지|데이터 무결성 보장|

---

### 🎯 실무 팁

- 트랜잭션 내 모든 작업은 **하나의 묶음**으로 취급
    
- 예외 처리 시 반드시 `ROLLBACK` 수행
    
- 원자성을 위해 DBMS는 **로그와 트랜잭션 관리자**를 항상 사용
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Atomicity]]|전부 실행 or 전부 취소|
|[[Durability]]|커밋된 결과는 영구히 보존|
|[[Consistency]]|트랜잭션 전후 무결성 유지|
|[[Rollback]]|트랜잭션 전체 무효화 수단|

---