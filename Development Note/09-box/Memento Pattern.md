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

## ✅ 메멘토 패턴(Memento Pattern)

### 🔤 용어 해석

- **Memento**: 기억, 기록, 기념물
- 👉 메멘토 패턴은 **객체의 이전 상태를 저장하고, 필요할 때 복원할 수 있도록 하는 설계 패턴**

---

### 🧩 메멘토 패턴이란?

| 항목 | 설명 |
|------|------|
| **정의** | 객체 내부 상태를 캡슐화하여 **외부에 노출하지 않고, 이전 상태로 복원할 수 있도록** 하는 설계 방식 |
| **목적** | **Undo/Redo 기능 구현**, 임시 상태 저장, 히스토리 기능 제공 |
| **분류** | [[GOF(Gang of Four Design Patterns)]] 중 **행위(Behavioral) 패턴**

---

### 🧱 구조 구성요소

| 구성 요소 | 역할 |
|-----------|------|
| **Originator** | 현재 상태를 가진 객체. 상태 저장/복원 책임 |
| **Memento** | Originator의 상태를 저장하는 객체 (불변 객체로 캡슐화) |
| **Caretaker** | Memento를 보관하며 복원 요청 시 전달하는 객체

---

### 📚 예시로 이해하기 (Java 스타일)

```java
// Memento
class TextMemento {
    private final String text;
    public TextMemento(String text) { this.text = text; }
    public String getSavedText() { return text; }
}

// Originator
class Editor {
    private String text = "";
    public void setText(String t) { text = t; }
    public String getText() { return text; }

    public TextMemento save() {
        return new TextMemento(text);
    }

    public void restore(TextMemento memento) {
        text = memento.getSavedText();
    }
}
````

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|**장점**|객체 내부 상태 보호하면서도 복원 가능, Undo/Redo 용이|
|**단점**|저장 횟수가 많아지면 **메모리 사용량 증가**|
|**활용 상황**|에디터의 실행 취소, 게임 저장/로드, 상태 이력 관리|

---

### 🎯 실무 팁

- 상태 크기가 크거나 자주 저장된다면 **차등 저장(Diff 방식)** 고려
    
- 메멘토는 외부에 **상태를 노출하지 않으므로 캡슐화 원칙을 지키면서도 복원 기능 제공**
    
- Java에서는 `Serializable` 활용 시 메멘토 패턴 응용 가능
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Command Pattern]]|실행 요청 자체를 캡슐화|
|메멘토 패턴|객체 상태를 캡슐화하여 저장/복원|
|[[Prototype Pattern]]|객체 자체를 복제 (전체 복사)|