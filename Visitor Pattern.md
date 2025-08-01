---
type: learn
created: 2025-08-02(토) / 01:20
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

## ✅ 비지터 패턴(Visitor Pattern)

### 🔤 용어 해석

- **Visitor**: 방문자
- 👉 비지터 패턴은 **객체의 구조는 변경하지 않고, 객체에 수행할 연산(동작)을 외부 객체로 분리**하여 정의하는 패턴

---

### 🧩 비지터 패턴이란?

| 항목 | 설명 |
|------|------|
| **정의** | 객체 구조를 변경하지 않고, **객체에 새로운 연산을 추가**할 수 있도록 하는 설계 방식 |
| **목적** | 연산(행위)을 객체에서 분리함으로써 **기능 추가를 유연하게 하고, 구조와 책임을 분리** |
| **분류** | [[GOF(Gang of Four Design Patterns)]] 중 **행위(Behavioral) 패턴**

---

### 🧱 구조 구성요소

| 구성 요소 | 역할 |
|-----------|------|
| **Visitor** | 각 요소에 대한 동작을 정의한 인터페이스 |
| **ConcreteVisitor** | 실제 연산을 수행하는 구현 클래스 |
| **Element** | `accept(visitor)` 메서드를 가진 요소 인터페이스 |
| **ConcreteElement** | 실제 데이터를 가진 객체이며, visitor를 받아 연산을 위임 |
| **ObjectStructure** | 여러 요소를 포함하고 순회 기능 제공

---

### 📚 예시로 이해하기 (Java 스타일)

```java
// Element
interface Shape {
    void accept(Visitor visitor);
}

class Circle implements Shape {
    public void accept(Visitor visitor) {
        visitor.visit(this);
    }
}

// Visitor
interface Visitor {
    void visit(Circle circle);
}

class DrawVisitor implements Visitor {
    public void visit(Circle circle) {
        System.out.println("원을 그림");
    }
}
````

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|**장점**|객체 변경 없이 기능(연산) 추가 가능, 연산 분리로 코드 응집도 상승|
|**단점**|새로운 객체 타입이 추가되면 **Visitor 인터페이스도 수정 필요** → 개방-폐쇄 원칙 위반 가능|
|**적합 상황**|복잡한 객체 구조에 대해 **여러 종류의 연산이 자주 추가되는 경우**|

---

### 🎯 실무 팁

- 컴파일러의 AST(Abstract Syntax Tree) 탐색/처리에 자주 사용
    
- UI 요소(버튼, 텍스트, 입력창 등)를 순회하며 다양한 기능(렌더링, 유효성 검사 등)을 적용할 때 유용
    
- **Element의 내부 상태를 Visitor가 외부에서 활용**하므로 캡슐화 원칙과 충돌 우려 → 주의 필요
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Iterator Pattern]]|요소를 순회하면서 동일한 연산 반복|
|비지터 패턴|순회 대상마다 다른 연산을 적용 (이중 디스패치 기반)|
|[[Strategy Pattern]]|행위를 객체로 분리하되, 타입 분기 없이 교체 가능|