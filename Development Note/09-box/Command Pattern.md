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

## ✅ 커맨드 패턴(Command Pattern)

### 🔤 용어 해석

- **Command**: 명령, 지시
- 👉 커맨드 패턴은 **요청(명령)을 객체로 캡슐화하여, 요청자와 실행자 간의 결합을 느슨하게 만들어주는 행위 패턴**

---

### 🧩 커맨드 패턴이란?

| 항목 | 설명 |
|------|------|
| **정의** | 요청을 캡슐화한 커맨드 객체를 통해 **요청자(Invoker)와 수신자(Receiver)를 분리**시키는 설계 방식 |
| **목적** | 실행 요청을 객체화하여 **명령 큐, Undo/Redo, 로그 기록 등 다양한 기능**을 쉽게 구현 |
| **분류** | [[GOF(Gang of Four Design Patterns)]] 중 **행위(Behavioral) 패턴**

---

### 🧱 구조 구성요소

| 구성 요소 | 역할 |
|-----------|------|
| **Command** | 실행할 명령에 대한 인터페이스 |
| **ConcreteCommand** | 실제 명령을 구현하는 클래스 |
| **Receiver** | 명령이 수행될 대상(실행 로직 포함) |
| **Invoker** | 명령을 실행시키는 주체 (예: 버튼 클릭) |
| **Client** | 명령 객체를 생성하고 설정하는 사용자

---

### 📚 예시로 이해하기 (Java 스타일)

```java
// Command 인터페이스
interface Command {
    void execute();
}

// Receiver
class Light {
    public void turnOn() {
        System.out.println("불 켜짐");
    }
}

// ConcreteCommand
class LightOnCommand implements Command {
    private Light light;
    public LightOnCommand(Light light) { this.light = light; }
    public void execute() {
        light.turnOn();
    }
}

// Invoker
class RemoteControl {
    private Command command;
    public void setCommand(Command command) {
        this.command = command;
    }
    public void pressButton() {
        command.execute();
    }
}
````

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|**장점**|명령의 캡슐화, 실행 취소/재실행 가능, 요청 내역 로그화 용이|
|**단점**|클래스 수 증가, 구조 복잡도 증가|
|**적합 상황**|버튼 클릭 처리, 매크로 기록, Undo/Redo, 작업 스케줄링 등|

---

### 🎯 실무 팁

- UI 이벤트 처리, 스케줄러, 트랜잭션 작업 취소 구현 등에서 활용 가능
    
- 명령에 대한 로깅 → **감사 로그 / 이력 추적 시스템 구현**에 유리
    
- Spring Framework의 `@Transactional` 로직과 결합해 커맨드 실행 단위로 관리 가능
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Strategy Pattern]]|여러 알고리즘 중 하나를 선택해 실행|
|커맨드 패턴|실행할 동작을 객체로 캡슐화해 요청과 실행 분리|
|[[Mediator Pattern]]|객체 간 복잡한 상호작용을 중재자가 관리|