---
type: learn
created: 2025-08-02(토) / 01:15
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

## ✅ 상태 패턴(State Pattern)

### 🔤 용어 해석

- **State**: 상태, 상황
- 👉 상태 패턴은 **객체의 내부 상태에 따라 동작이 달라지도록 하고, 상태 전환을 객체화**하여 관리하는 설계 패턴

---

### 🧩 상태 패턴이란?

| 항목 | 설명 |
|------|------|
| **정의** | 객체가 가지는 **내부 상태에 따라 동일한 요청이 서로 다른 방식으로 처리되도록** 구현하는 패턴 |
| **목적** | 조건문 없이 상태 전환을 캡슐화하고 **상태별 행위를 독립적으로 분리** |
| **분류** | [[GOF(Gang of Four Design Patterns)]] 중 **행위(Behavioral) 패턴**

---

### 🧱 구조 구성요소

| 구성 요소 | 역할 |
|-----------|------|
| **Context** | 상태를 가지는 객체. 상태 전환 요청을 처리 |
| **State** | 상태에 따른 행위 인터페이스 정의 |
| **ConcreteState** | 각 상태별로 행동을 구체적으로 구현한 클래스

---

### 📚 예시로 이해하기 (Java 스타일)

```java
// State 인터페이스
interface State {
    void handle();
}

// ConcreteState
class ReadyState implements State {
    public void handle() {
        System.out.println("대기 중...");
    }
}
class PlayingState implements State {
    public void handle() {
        System.out.println("재생 중...");
    }
}

// Context
class MediaPlayer {
    private State state;
    public void setState(State state) { this.state = state; }
    public void play() { state.handle(); }
}
````

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|**장점**|상태별 행동 분리, 조건문 제거, 클래스 책임 분리|
|**단점**|상태 수가 많을 경우 클래스 수 증가|
|**활용 상황**|플레이어, 게임 상태, 연결 상태, 인증 상태 등 상태 변화가 많은 시스템|

---

### 🎯 실무 팁

- 상태 전환이 자주 일어나거나 복잡한 경우, 조건문보다 **상태 객체 전환이 더 가독성 높고 유지보수 용이**
    
- 상태 전환이 명확한 경우, 상태 객체 간 **전환 책임도 각자에게 위임** 가능
    
- 상태 패턴은 종종 [[Strategy Pattern]]과 혼동되지만, 전략은 **행위 선택**, 상태는 **상태 전이 중심**
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Strategy Pattern]]|행위를 동적으로 교체|
|상태 패턴|객체의 상태 변화에 따라 행위가 달라짐|
|[[Observer Pattern]]|상태 변화 발생 시 외부에 알림 전달|