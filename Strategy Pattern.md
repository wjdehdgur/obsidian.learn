---
type: learn
created: 2025-08-02(토) / 01:14
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-08-02
review_success: false
related_concepts: []
---

## ✅ 전략 패턴(Strategy Pattern)

### 🔤 용어 해석

- **Strategy**: 전략, 방식, 알고리즘 선택
- 👉 전략 패턴은 **동일한 문제를 해결하는 다양한 알고리즘(전략)을 정의하고, 실행 시점에 그 중 하나를 선택**할 수 있게 해주는 패턴

---

### 🧩 전략 패턴이란?

| 항목 | 설명 |
|------|------|
| **정의** | 알고리즘군을 정의하고, **각 알고리즘을 캡슐화하여 상호 교체 가능**하도록 만든 패턴 |
| **목적** | 조건에 따라 실행 알고리즘을 **유연하게 교체**하면서 코드 중복 제거 및 결합도 최소화 |
| **분류** | [[GOF(Gang of Four Design Patterns)]] 중 **행위(Behavioral) 패턴**

---

### 🧱 구조 구성요소

| 구성 요소 | 역할 |
|-----------|------|
| **Context** | 전략을 사용하는 클라이언트. 어떤 전략을 사용할지 결정 |
| **Strategy (인터페이스)** | 공통 알고리즘 인터페이스 정의 |
| **ConcreteStrategy** | 실제 알고리즘을 구현한 클래스

---

### 📚 예시로 이해하기 (Java 스타일)

```java
// 전략 인터페이스
interface PaymentStrategy {
    void pay(int amount);
}

// 전략 구현
class CreditCardPayment implements PaymentStrategy {
    public void pay(int amount) {
        System.out.println("신용카드로 " + amount + "원 결제");
    }
}
class PaypalPayment implements PaymentStrategy {
    public void pay(int amount) {
        System.out.println("PayPal로 " + amount + "원 결제");
    }
}

// Context
class PaymentService {
    private PaymentStrategy strategy;
    public PaymentService(PaymentStrategy strategy) {
        this.strategy = strategy;
    }
    public void executePayment(int amount) {
        strategy.pay(amount);
    }
}
````

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|**장점**|알고리즘 교체가 쉽고, 코드 재사용 가능, OCP(개방-폐쇄 원칙) 적용 가능|
|**단점**|전략 클래스가 많아질 수 있음, 클라이언트가 전략을 알아야 함|
|**적용 대상**|실행 조건에 따라 알고리즘이 바뀌는 경우 (예: 정렬 방식, 결제 수단 등)|

---

### 🎯 실무 팁

- if-else 또는 switch 문으로 분기된 알고리즘을 분리하고 싶을 때 유용
    
- [[Dependency Injection]]으로 전략 객체를 주입하면 유연성과 테스트 용이성 극대화
    
- 정책이 자주 바뀌는 시스템(결제, 로그인 방식, 할인 정책 등)에 매우 적합
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[State Pattern]]|상태에 따라 객체의 동작이 달라짐 (상태 중심)|
|전략 패턴|알고리즘을 캡슐화하여 선택 가능하게 함 (행위 중심)|
|[[Template Method Pattern]]|알고리즘의 구조는 고정하고, 일부 단계만 서브클래스에서 재정의|