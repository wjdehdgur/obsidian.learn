---
type: learn
created: 2025-08-02(토) / 01:18
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

## ✅ 템플릿 메서드 패턴(Template Method Pattern)

### 🔤 용어 해석

- **Template**: 틀, 구조
- **Method**: 메서드, 함수
- 👉 템플릿 메서드 패턴은 **알고리즘의 구조를 상위 클래스에서 정의하고, 그 일부 단계는 하위 클래스에서 오버라이드하여 구현하는 방식의 패턴**

---

### 🧩 템플릿 메서드 패턴이란?

| 항목 | 설명 |
|------|------|
| **정의** | 알고리즘 전체 구조를 상위 클래스에서 정의하고, **일부 구체적인 작업은 하위 클래스가 구현**하도록 하는 설계 패턴 |
| **목적** | 공통 로직은 재사용하면서, 세부 구현은 유연하게 변경 가능하도록 분리 |
| **분류** | [[GOF(Gang of Four Design Patterns)]] 중 **행위(Behavioral) 패턴**

---

### 🧱 구조 구성요소

| 구성 요소 | 역할 |
|-----------|------|
| **AbstractClass** | 템플릿 메서드를 정의하고, 공통 알고리즘 흐름 구성 |
| **Template Method** | 전체 알고리즘의 구조를 정의하는 메서드 |
| **Primitive Method** | 하위 클래스에서 구현해야 할 단계 메서드 |
| **ConcreteClass** | Primitive Method를 구체적으로 구현하는 하위 클래스

---

### 📚 예시로 이해하기 (Java 스타일)

```java
abstract class DataProcessor {
    public final void process() { // Template Method
        readData();
        processData();
        saveData();
    }

    abstract void readData();    // Primitive Method
    abstract void processData(); // Primitive Method

    void saveData() {
        System.out.println("데이터 저장");
    }
}

class CSVDataProcessor extends DataProcessor {
    void readData() { System.out.println("CSV 파일 읽기"); }
    void processData() { System.out.println("CSV 처리 로직"); }
}
````

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|**장점**|코드 재사용 가능, 알고리즘 구조 통제, 구현 분리|
|**단점**|상속 기반이라 유연성 한계, 클래스 수 증가 가능|
|**활용 예시**|후크 메서드 제공, 프레임워크 내부 동작 제어(Spring, Servlet 등)|

---

### 🎯 실무 팁

- 알고리즘의 전체 흐름은 **고정하되**, 단계별 동작만 변경하고 싶을 때 매우 유용
    
- 프레임워크나 라이브러리 개발 시 **확장 포인트 제공을 위한 구조**로 자주 사용됨
    
- Hook 메서드(선택적으로 오버라이딩 가능한 메서드)와 함께 사용 시 확장성 극대화
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Strategy Pattern]]|알고리즘 자체를 캡슐화하여 교체 가능|
|템플릿 메서드 패턴|알고리즘 구조는 고정, 단계만 교체|
|[[Factory Method Pattern]]|객체 생성을 서브클래스에 위임|