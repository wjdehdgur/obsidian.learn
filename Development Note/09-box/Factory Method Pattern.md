---
type: learn
created: 2025-08-01(금) / 00:14
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

## ✅ 팩토리 메서드 패턴(Factory Method Pattern)

### 🔤 용어 해석

- **Factory**: 공장 → 객체를 만들어내는 곳
- **Method**: 메서드, 함수
- 👉 팩토리 메서드 패턴은 **객체 생성을 서브클래스에 위임**하여, 상위 클래스에서는 인스턴스 생성 방식을 알 필요 없게 하는 패턴

---

### 🧩 팩토리 메서드 패턴이란?

| 항목 | 설명 |
|------|------|
| **정의** | 객체 생성을 위한 인터페이스는 정의하되, 실제 어떤 클래스의 인스턴스를 만들지는 **서브클래스에서 결정**하도록 하는 패턴 |
| **목적** | 코드의 결합도를 낮추고, **유연하게 객체 생성을 제어**하기 위함 |
| **분류** | [[GOF(Gang of Four Design Patterns)]] 중 **생성(Creational) 패턴**

---

### 🧱 구조 구성요소

| 구성 요소 | 역할 |
|-----------|------|
| **Product (인터페이스)** | 생성될 객체의 공통 인터페이스 |
| **ConcreteProduct** | 실제 생성될 객체 클래스 |
| **Creator (추상 클래스)** | 팩토리 메서드를 정의하는 상위 클래스 |
| **ConcreteCreator** | 실제 객체 생성을 구현하는 서브클래스 |

---

### 📚 예시로 이해하기 (Java 스타일)

```java
// Product 인터페이스
interface Button {
    void render();
}

// ConcreteProduct
class WindowsButton implements Button {
    public void render() {
        System.out.println("윈도우 버튼 출력");
    }
}

// Creator
abstract class Dialog {
    abstract Button createButton();
    public void renderWindow() {
        Button button = createButton();
        button.render();
    }
}

// ConcreteCreator
class WindowsDialog extends Dialog {
    Button createButton() {
        return new WindowsButton();
    }
}
````

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|**확장성**|새로운 객체를 만들 때 기존 코드를 건드리지 않고 **서브클래스만 추가**하면 됨|
|**유연성**|객체 생성 코드를 캡슐화함으로써 **클래스 의존도 감소**|
|**단점**|클래스 수 증가, 구조 복잡도 상승 가능성 있음|

---

### 🎯 실무 팁

- 상위 클래스는 **객체 생성 책임을 갖지 않도록 분리**하는 것이 원칙
    
- 다양한 종류의 객체 생성이 예상되거나 자주 바뀔 경우에 적합
    
- Spring Framework에서는 Bean 생성이나 Strategy 등록 등에서 자주 활용됨
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Abstract Factory Pattern]]|관련 객체를 일괄적으로 생성하는 상위 수준의 팩토리|
|팩토리 메서드|하나의 제품 객체를 서브클래스가 선택 생성|
|[[Builder Pattern]]|복잡한 객체를 단계적으로 조립|
