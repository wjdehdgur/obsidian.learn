---
type: learn
created: 2025-08-02(토) / 01:19
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

## ✅ 미디에이터 패턴(Mediator Pattern)

### 🔤 용어 해석

- **Mediator**: 중재자, 중간 관리자
- 👉 미디에이터 패턴은 **객체들 간의 직접적인 상호작용을 제거하고, 중재자를 통해 통신하도록 구성하는 패턴**

---

### 🧩 미디에이터 패턴이란?

| 항목 | 설명 |
|------|------|
| **정의** | 여러 객체 간의 복잡한 상호작용을 **중앙 집중형 중재자 객체를 통해 통제**하는 설계 패턴 |
| **목적** | 객체 간의 결합도를 낮추고, **객체 간 통신을 단순화**하여 유지보수성을 높임 |
| **분류** | [[GOF(Gang of Four Design Patterns)]] 중 **행위(Behavioral) 패턴**

---

### 🧱 구조 구성요소

| 구성 요소 | 역할 |
|-----------|------|
| **Mediator** | 객체 간 통신을 조정하는 인터페이스 또는 추상 클래스 |
| **ConcreteMediator** | 실제 중재 로직을 구현한 클래스 |
| **Colleague** | 서로 통신해야 하는 객체 (모든 통신은 중재자를 통해 수행)

---

### 📚 예시로 이해하기 (Java 스타일)

```java
// Colleague 인터페이스
interface Colleague {
    void send(String message);
    void receive(String message);
}

// Mediator 인터페이스
interface Mediator {
    void notify(Colleague sender, String message);
}

// ConcreteMediator
class ChatRoom implements Mediator {
    private List<Colleague> users = new ArrayList<>();
    public void addUser(Colleague user) { users.add(user); }

    public void notify(Colleague sender, String message) {
        for (Colleague user : users) {
            if (user != sender) user.receive(message);
        }
    }
}
````

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|**장점**|객체 간 직접 참조 제거 → **결합도 감소**, 관계 단순화|
|**단점**|**중재자 클래스가 복잡해질 수 있음** (모든 로직이 집중되므로)|
|**적합 상황**|UI 컴포넌트 간 이벤트 조정, 채팅방 사용자 통신, 항공기 관제 시스템 등|

---

### 🎯 실무 팁

- MVC 구조에서 Controller 또는 EventBus가 Mediator 역할을 하는 경우 많음
    
- 중재자에 너무 많은 책임이 집중되지 않도록 **역할 분산 고려 필요**
    
- UI에서 다양한 위젯이 서로 상태를 바꿀 경우 Mediator 패턴으로 **상호작용 구조를 단순화**
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Observer Pattern]]|객체 간 알림/구독 관계 (비동기 전달 중심)|
|미디에이터 패턴|**모든 통신을 중앙 중재자가 통제** (동기 처리 중심)|
|[[Command Pattern]]|요청 자체를 객체로 분리하여 실행 시점 제어|