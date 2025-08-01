---
type: learn
created: 2025-08-01(금) / 00:16
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

## ✅ 추상 팩토리 패턴(Abstract Factory Pattern)

### 🔤 용어 해석

- **Abstract**: 추상적인, 공통적인
- **Factory**: 객체 생성 책임을 가지는 공장
- 👉 추상 팩토리 패턴은 **관련된 객체들을 일관성 있게 생성할 수 있도록 하는 팩토리 집합을 제공**하는 생성 패턴

---

### 🧩 추상 팩토리 패턴이란?

| 항목 | 설명 |
|------|------|
| **정의** | 서로 연관된 객체들을 **구체적인 클래스에 의존하지 않고, 일관성 있게 생성**할 수 있도록 인터페이스를 제공하는 패턴 |
| **목적** | 객체군(Product Family)을 함께 생성하여 **호환성과 일관성 보장** |
| **분류** | [[GOF(Gang of Four Design Patterns)]] 중 **생성(Creational) 패턴**

---

### 🧱 구조 구성요소

| 구성 요소 | 역할 |
|-----------|------|
| **AbstractFactory** | 제품 생성 메서드들의 인터페이스 정의 |
| **ConcreteFactory** | 제품을 실제로 생성하는 클래스 |
| **AbstractProduct** | 생성될 제품 객체의 인터페이스 |
| **ConcreteProduct** | 실제 구현된 제품 객체 |
| **Client** | 추상 팩토리를 사용하여 제품을 생성하는 소비자 코드

---

### 📚 예시로 이해하기 (Java 스타일)

```java
// AbstractProduct
interface Button { void render(); }
interface Checkbox { void check(); }

// ConcreteProduct
class WindowsButton implements Button { public void render() { ... } }
class WindowsCheckbox implements Checkbox { public void check() { ... } }

// AbstractFactory
interface GUIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

// ConcreteFactory
class WindowsFactory implements GUIFactory {
    public Button createButton() { return new WindowsButton(); }
    public Checkbox createCheckbox() { return new WindowsCheckbox(); }
}

// Client
class Application {
    private Button button;
    private Checkbox checkbox;
    public Application(GUIFactory factory) {
        this.button = factory.createButton();
        this.checkbox = factory.createCheckbox();
    }
}
````

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|**적용 시점**|관련된 객체들이 **함께 생성되어야 하는 경우**|
|**장점**|제품군 간 호환성 보장, 코드 일관성 유지, 클라이언트 코드 단순화|
|**단점**|제품군이 늘어날수록 인터페이스 및 클래스 수 증가, 복잡도 상승|

---

### 🎯 실무 팁

- UI 테마 변경, DB 드라이버 교체 등 **전체 제품군을 한꺼번에 교체해야 할 때 매우 유용**
    
- 팩토리 간 의존성이 강하므로, 구조 설계 시 **확장 대비 설계가 중요**
    
- Spring Bean 구성 및 DI에서도 내부적으로 추상 팩토리 형태 자주 사용됨
    

---

### 🧩 팩토리 계열 비교

| 항목   | [[Factory Method Pattern]] | [[Abstract Factory Pattern]] |
| ---- | -------------------------- | ---------------------------- |
| 생성 수 | 한 종류 객체                    | 관련된 여러 객체                    |
| 구성   | 서브클래스에서 생성 위임              | 팩토리 군 전체 인터페이스               |
| 유연성  | 낮음                         | 높음 (제품군 단위 변경 용이)            |
|      |                            |                              |