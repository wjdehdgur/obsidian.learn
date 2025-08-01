---
type: learn
created: 2025-08-01(금) / 00:13
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-08-01
review_success: false
related_concepts: []
---

## ✅ 싱글톤 패턴(Singleton Pattern)

### 🔤 용어 해석

- **Singleton**: 단 하나의 인스턴스
- **Pattern**: 설계 방식, 반복 구조
- 👉 싱글톤 패턴은 **클래스의 인스턴스를 오직 하나만 생성하고, 그 인스턴스에 어디서든 접근할 수 있게** 하는 생성 패턴

---

### 🧩 싱글톤 패턴이란?

| 항목 | 설명 |
|------|------|
| **정의** | 클래스의 **인스턴스를 하나만 생성**하도록 제한하고, 그 인스턴스를 전역적으로 공유할 수 있도록 설계 |
| **목적** | 전역 상태 관리, 자원 낭비 방지, 동일 객체 공유 |
| **분류** | [[GOF(Gang of Four Design Patterns)]] 중 **생성(Creational) 패턴**에 속함 |

---

### 🧱 주요 특징

| 항목 | 설명 |
|------|------|
| **인스턴스 제한** | 생성자를 외부에서 호출할 수 없도록 **private으로 제한** |
| **정적 접근** | 클래스 내부에 생성된 단일 인스턴스를 **정적 메서드로 반환** |
| **전역 접근** | 시스템 전역에서 동일 객체로 접근 가능 |
| **스레드 안전성 고려** | 다중 스레드 환경에선 동기화 처리 필요

---

### 📚 예시로 이해하기 (Java 스타일)

```java
public class Singleton {
    private static Singleton instance = null;

    private Singleton() { } // 생성자 비공개

    public static Singleton getInstance() {
        if (instance == null) {
            instance = new Singleton(); // 최초 1회만 생성
        }
        return instance;
    }
}
````

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|**용도**|설정 관리, DB 연결, 로그 시스템 등 공유 자원 관리|
|**장점**|메모리 절약, 일관된 접근, 객체 생성 비용 절감|
|**단점**|전역 상태로 인한 테스트 어려움, 다중 스레드 환경에선 위험 가능성 존재|

---

### 🎯 실무 팁

- 단일 책임 원칙(SRP)을 어기지 않도록 주의: **싱글톤이 너무 많은 역할을 가지지 않게 분리**
    
- 멀티스레드 환경에선 **Double-Checked Locking**, **Enum Singleton** 등의 기법 고려
    
- 테스트 시 Mock 주입 어려움 → 필요 시 **인터페이스 분리**로 대체 가능
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Factory Method Pattern]]|객체 생성을 서브클래스에 위임|
|싱글톤 패턴|객체를 단 하나로 제한|
