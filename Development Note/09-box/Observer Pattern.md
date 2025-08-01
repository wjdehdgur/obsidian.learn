---
type: learn
created: 2025-08-01(금) / 00:38
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

## ✅ 옵저버 패턴(Observer Pattern)

### 🔤 용어 해석

- **Observer**: 관찰자
- **Pattern**: 설계 방식
- 👉 옵저버 패턴은 **어떤 객체의 상태가 변경되었을 때, 그 객체에 의존하는 다른 객체들이 자동으로 알림을 받아 동기화되는 구조**

---

### 🧩 옵저버 패턴이란?

| 항목 | 설명 |
|------|------|
| **정의** | 한 객체의 상태 변화가 있을 때, **그 객체에 의존하는 다수의 객체에 자동으로 알림을 전달**하는 패턴 |
| **목적** | **느슨한 결합**으로 객체 간 일대다(one-to-many) 관계를 구성하여, 상태 변화 전파를 효율화 |
| **분류** | [[GOF(Gang of Four Design Patterns)]] 중 **행위(Behavioral) 패턴**

---

### 🧱 구조 구성요소

| 구성 요소 | 역할 |
|-----------|------|
| **Subject** | 상태를 가지고 있고, 옵저버를 등록/제거하며 상태 변경 시 알림 전송 |
| **Observer** | Subject의 상태 변화에 반응하는 객체 |
| **ConcreteSubject** | 실제 상태를 가지며, 변경 시 모든 옵저버에게 알림 |
| **ConcreteObserver** | 실제로 업데이트 로직을 구현하는 옵저버 객체

---

### 📚 예시로 이해하기 (Java 스타일)

```java
interface Observer {
    void update(String message);
}

class ConcreteObserver implements Observer {
    public void update(String message) {
        System.out.println("알림 수신: " + message);
    }
}

class Subject {
    private List<Observer> observers = new ArrayList<>();
    private String state;

    public void attach(Observer o) { observers.add(o); }
    public void detach(Observer o) { observers.remove(o); }

    public void setState(String newState) {
        this.state = newState;
        notifyObservers();
    }

    private void notifyObservers() {
        for (Observer o : observers) o.update(state);
    }
}
````

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|**적용 상황**|이벤트 기반 시스템, GUI 알림 시스템, 메시지 브로커 구조|
|**장점**|느슨한 결합, 확장성 우수, 변경 시 자동 동기화|
|**단점**|옵저버 수가 많을 경우 성능 저하, 디버깅 어려움|

---

### 🎯 실무 팁

- UI 프레임워크의 **이벤트 리스너(Event Listener)** 구현에 많이 사용됨
    
- Java의 `java.util.Observer` 인터페이스, JavaScript의 `EventEmitter`, RxJS 등에서 구현 형태로 자주 등장
    
- **Pub/Sub 구조**와 매우 유사하지만, 옵저버 패턴은 **주체(Subject)가 직접 옵저버를 알고 있는 점**에서 다름
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Strategy Pattern]]|알고리즘을 동적으로 교체|
|옵저버 패턴|상태 변화 발생 시 자동 알림|
|[[Mediator Pattern]]|다수 객체 간 복잡한 의존 관계를 중재자 객체로 단순화|