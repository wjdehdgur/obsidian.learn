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

## ✅ 책임 연쇄 패턴(Chain of Responsibility Pattern)

### 🔤 용어 해석

- **Chain**: 연결된 구조, 사슬
- **Responsibility**: 책임, 처리 역할
- 👉 책임 연쇄 패턴은 **여러 처리 객체를 체인처럼 연결해, 요청을 처리할 수 있는 객체가 처리하거나 다음 객체로 넘기도록 하는 구조**

---

### 🧩 책임 연쇄 패턴이란?

| 항목 | 설명 |
|------|------|
| **정의** | 요청을 처리할 수 있는 **여러 객체를 연결해**, 하나가 처리하지 못하면 다음 객체로 넘기면서 **책임을 분산**하는 패턴 |
| **목적** | 클라이언트와 처리 객체 간 결합도를 낮추고, **유연한 요청 처리 흐름 구현** |
| **분류** | [[GOF(Gang of Four Design Patterns)]] 중 **행위(Behavioral) 패턴**

---

### 🧱 구조 구성요소

| 구성 요소 | 역할 |
|-----------|------|
| **Handler** | 요청을 처리하거나 다음 핸들러로 전달하는 인터페이스 |
| **ConcreteHandler** | 실제 처리 책임을 가지며, 필요 시 다음 핸들러로 위임 |
| **Client** | 요청을 처음 전달하는 객체

---

### 📚 예시로 이해하기 (Java 스타일)

```java
abstract class Handler {
    protected Handler next;
    public void setNext(Handler next) { this.next = next; }
    public abstract void handleRequest(String request);
}

class AuthHandler extends Handler {
    public void handleRequest(String request) {
        if (request.equals("인증")) {
            System.out.println("인증 처리 완료");
        } else if (next != null) {
            next.handleRequest(request);
        }
    }
}

class LoggingHandler extends Handler {
    public void handleRequest(String request) {
        if (request.equals("로그")) {
            System.out.println("로그 처리 완료");
        } else if (next != null) {
            next.handleRequest(request);
        }
    }
}
````

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|**장점**|핸들러 추가/삭제가 유연함, 코드 중복 방지, 조건문 최소화|
|**단점**|디버깅 어려움, 요청이 끝까지 전달될 경우 누락 위험|
|**활용 상황**|인증 체계, 이벤트 처리, 필터 체인, 로깅 시스템 등|

---

### 🎯 실무 팁

- Spring Security의 **필터 체인(FilterChainProxy)** 구조가 대표적인 예
    
- 각 처리 단계는 반드시 `다음 핸들러 호출 여부`를 명시해야 함
    
- 너무 많은 체인 구성은 오히려 **처리 흐름 추적을 어렵게 하므로 주의**
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Decorator Pattern]]|기능을 덧붙이는 방식으로 체인 구성|
|책임 연쇄 패턴|책임을 넘기는 방식으로 체인 구성|
|[[Command Pattern]]|요청 자체를 객체화하여 실행|