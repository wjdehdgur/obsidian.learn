## 🥇 상(高) 빈도 개념 - 데이터베이스 구축

---

### [[SQL]]

- **중요도**: 매우 높음
    
- **난이도**: 중
    
- **기타**: [[DDL]], [[DML]], [[DCL]]의 기능별 명령어 구분 핵심
    
- **기출 포인트**: `SELECT`, `JOIN`, `GROUP BY`, `HAVING`, `GRANT`, `REVOKE`, [[View|뷰]], [[Index|인덱스]] 활용 구문
    

---

### [[Normalization|정규화]]

- **중요도**: 매우 높음
    
- **난이도**: 중
    
- **기타**: [[1NF]], [[2NF]], [[3NF]], [[BCNF]], [[4NF]], [[5NF]]까지 단계별 특성 구분
    
- **기출 포인트**: 함수 종속성, 이상 현상 제거 목적, 정규형 비교
    

---

### [[Transaction|트랜잭션]]

- **중요도**: 매우 높음
    
- **난이도**: 중
    
- **기타**: [[ACID]] 특성([[Atomicity]], [[Consistency]], [[Isolation]], [[Durability]])을 중심으로 출제
    
- **기출 포인트**: 상태 변화 (Active → Partially Committed → Committed), 회복 기법, 동시성 제어
    

---

### [[Integrity Constraint|무결성 제약조건]]

- **중요도**: 매우 높음
    
- **난이도**: 중
    
- **기타**: [[Entity Integrity|개체 무결성]], [[Referential Integrity|참조 무결성]], [[Domain Integrity|도메인 무결성]] 등
    
- **기출 포인트**: 기본키는 NULL 불가, 외래키의 참조 일치 조건
    

---

### [[Key|키]]

- **중요도**: 매우 높음
    
- **난이도**: 하
    
- **기타**: [[Super Key]], [[Candidate Key]], [[Primary Key]], [[Foreign Key]] 비교
    
- **기출 포인트**: 유일성과 최소성, 참조 관계
    

---

### [[View|뷰]]

- **중요도**: 높음
    
- **난이도**: 중
    
- **기타**: 논리적 가상 테이블, 실제 저장 공간 없음
    
- **기출 포인트**: `CREATE VIEW`, 수정 불가한 조건, 장단점
    

---

### [[Index|인덱스]]

- **중요도**: 높음
    
- **난이도**: 중
    
- **기타**: 검색 성능 최적화 목적, [[B-Tree]], [[Hash Index]] 방식
    
- **기출 포인트**: 생성/삭제 구문, 성능 개선 여부
    

---

### [[Entity-Relationship Diagram|ER 다이어그램]]

- **중요도**: 높음
    
- **난이도**: 하
    
- **기타**: [[Entity|개체]], [[Attribute|속성]], [[Relationship|관계]] 중심 구성
    
- **기출 포인트**: 개체 간 관계 유형, [[Cardinality|카디널리티]], [[Participation|참여도]]
    

---
## 🥈 중(中) 빈도 개념 - 데이터베이스 구축

---

### [[Relational Algebra|관계 대수]]

**중요도**: 중  
**난이도**: 중  
**기타**: [[Select]], [[Project]], [[Join]], [[Division]], [[Cartesian Product]] 등 연산 구분 필요  
**기출 포인트**: 연산자 정의, 조합 예시 문제, 결과 해석, 순수 관계 연산 vs 일반 집합 연산 비교

---

### [[Functional Dependency|함수 종속]]

**중요도**: 중  
**난이도**: 중  
**기타**: 정규화 기반 핵심 개념, 추론 규칙([[반사 규칙]], [[이행 규칙]], [[결합 규칙]], [[분해 규칙]]) 숙지 필수  
**기출 포인트**: X → Y 형태 표현, 결정자/종속자 관계 해석 문제 반복 출제

---

### [[Join|조인]]

**중요도**: 중  
**난이도**: 중  
**기타**: [[Inner Join]], [[Outer Join]], [[Equi Join]], [[Natural Join]] 등 분류와 차이점  
**기출 포인트**: 조인 결과 추론, Join 조건 누락 시 결과 예측 문제 자주 출제

---

### [[Anomaly|이상 현상]]

**중요도**: 중  
**난이도**: 하  
**기타**: [[삽입 이상]], [[삭제 이상]], [[갱신 이상]] 구분  
**기출 포인트**: 비정규화된 테이블에서 이상 유발 여부 묻는 사례형 문제 출제

---

### [[DCL]]

**중요도**: 중  
**난이도**: 하  
**기타**: [[GRANT]], [[REVOKE]] 중심, 사용자 권한 관리  
**기출 포인트**: 명령어 목적과 적용 예시 구별 문제

---

### [[Recovery|회복 기법]]

**중요도**: 중  
**난이도**: 중  
**기타**: [[Deferred Update]], [[Immediate Update]], [[로그 기반 회복]], [[Check Point]] 등  
**기출 포인트**: 장애 발생 후 Rollback/Commit 처리 방식 시나리오 해석

---

### [[Concurrency Control|동시성 제어]]

**중요도**: 중  
**난이도**: 중상  
**기타**: [[Lock]], [[Timestamp Ordering]], [[Serializable Schedule]], [[Deadlock]]  
**기출 포인트**: Lock granularity, 교착 상태 회피/해결 기법 출제

---

### [[Distributed DB|분산 데이터베이스]]

**중요도**: 중  
**난이도**: 중  
**기타**: [[Location Transparency]], [[Replication Transparency]], [[Failure Transparency]]  
**기출 포인트**: 투명성 유형 비교, 분산환경 특성 문제

---

### [[Data Dictionary|데이터 사전]]

**중요도**: 중  
**난이도**: 하  
**기타**: 메타데이터 저장소 역할  
**기출 포인트**: 메타데이터, 테이블 구조/속성 조회 관련 문제

---

### [[Cartesian Product|카티션 곱]]

**중요도**: 중  
**난이도**: 중  
**기타**: 조인 전 중간 연산, 조합 수 증가에 따른 연산 비용 고려  
**기출 포인트**: 관계 연산 순서에서의 활용, 의미 비교형 문제

---

## 🥉 하(低) 빈도 개념 - 데이터베이스 구축

---

### [[Domain|도메인]]

**중요도**: 낮음  
**난이도**: 하  
**기타**: 속성(Attribute)이 가질 수 있는 값들의 집합  
**기출 포인트**: [[Domain Integrity|도메인 무결성]]과 연결, 데이터 형/제약 조건 구분

---

### [[Super Key|슈퍼키]] / [[Candidate Key|후보키]]

**중요도**: 낮음  
**난이도**: 하  
**기타**: 유일성/최소성 기준으로 [[Primary Key|기본키]]와 구분  
**기출 포인트**: 키 간 포함관계, 유일성과 최소성 판단 문제

---

### [[Check Constraint|CHECK 제약조건]]

**중요도**: 낮음  
**난이도**: 하  
**기타**: 도메인 무결성 구현 시 활용, 특정 속성 값의 범위 제한  
**기출 포인트**: 테이블 생성 시 CHECK 구문의 용법

---

### [[Outer Join|외부 조인]]

**중요도**: 낮음  
**난이도**: 중  
**기타**: [[Left Outer Join]], [[Right Outer Join]], [[Full Outer Join]] 등 세부 유형 구분 필요  
**기출 포인트**: 결과 셋에서 NULL 포함되는 구조 해석

---

### [[Subquery|서브쿼리]]

**중요도**: 낮음  
**난이도**: 중  
**기타**: 단일행 / 다중행 / 상관 서브쿼리 구분  
**기출 포인트**: `IN`, `EXISTS`, `ALL`, `ANY` 활용 시 주의사항

---

### [[Index|인덱스]] 세부 유형

**중요도**: 낮음  
**난이도**: 중  
**기타**: [[Clustered Index]], [[Non-clustered Index]] 구분  
**기출 포인트**: 성능 비교, 물리적 저장 구조 차이

---

### [[Shadow Paging|섀도 페이징]]

**중요도**: 낮음  
**난이도**: 중  
**기타**: 회복 기법 중 하나, 로그 미사용 구조  
**기출 포인트**: [[Deferred Update]]와 차이점, Write-in-place/Write-ahead log 비교

---

### [[Commit]] / [[Rollback]]

**중요도**: 낮음  
**난이도**: 하  
**기타**: 트랜잭션 완료/복구 명령어  
**기출 포인트**: 명령어 위치, 실행 결과 예상 문제

---

### [[Deadlock|교착 상태]]

**중요도**: 낮음  
**난이도**: 중  
**기타**: [[Mutual Exclusion]], [[Hold and Wait]], [[No Preemption]], [[Circular Wait]] 조건  
**기출 포인트**: 회피 기법([[Wait-Die]], [[Wound-Wait]]) 또는 예방 조건 해석

---

### [[Timestamp Ordering|타임스탬프 기법]]

**중요도**: 낮음  
**난이도**: 중  
**기타**: 트랜잭션 간 순서를 보장하는 동시성 제어 방법  
**기출 포인트**: 충돌 방지 방식, [[Read Timestamp]], [[Write Timestamp]] 해석

---