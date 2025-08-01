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

## ✅ 반복자 패턴(Iterator Pattern)

### 🔤 용어 해석

- **Iterator**: 반복자, 순회 도구
- 👉 반복자 패턴은 **컬렉션 내부 구조를 노출하지 않고 요소들을 순차적으로 접근할 수 있도록** 해주는 설계 패턴

---

### 🧩 반복자 패턴이란?

| 항목 | 설명 |
|------|------|
| **정의** | 집합 객체 내부 구조를 노출하지 않고, **순차적으로 요소를 탐색할 수 있는 방법을 제공**하는 패턴 |
| **목적** | 컬렉션 순회를 위한 표준화된 인터페이스 제공 및 **컬렉션과 순회 알고리즘 분리** |
| **분류** | [[GOF(Gang of Four Design Patterns)]] 중 **행위(Behavioral) 패턴**

---

### 🧱 구조 구성요소

| 구성 요소 | 역할 |
|-----------|------|
| **Iterator** | 요소 순회를 위한 인터페이스 (`hasNext()`, `next()` 등) |
| **ConcreteIterator** | 실제 순회 구현 클래스 |
| **Aggregate** | 컬렉션 인터페이스. 반복자 생성 책임 |
| **ConcreteAggregate** | 실제 컬렉션 구현체. 반복자 반환

---

### 📚 예시로 이해하기 (Java 스타일)

```java
// Iterator 인터페이스
interface Iterator<T> {
    boolean hasNext();
    T next();
}

// Aggregate 인터페이스
interface Iterable<T> {
    Iterator<T> createIterator();
}

// ConcreteAggregate
class BookShelf implements Iterable<String> {
    private List<String> books = new ArrayList<>();
    public void addBook(String book) { books.add(book); }

    public Iterator<String> createIterator() {
        return new BookShelfIterator();
    }

    private class BookShelfIterator implements Iterator<String> {
        private int index = 0;
        public boolean hasNext() { return index < books.size(); }
        public String next() { return books.get(index++); }
    }
}
````

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|**장점**|컬렉션 구조와 순회 알고리즘을 분리하여 재사용성 향상|
|**단점**|간단한 순회에도 별도 클래스 필요 → 코드 양 증가|
|**활용 예시**|Java의 `Iterator`, `for-each`, JavaScript의 `for...of`, Python의 `__iter__()` 등|

---

### 🎯 실무 팁

- **컬렉션 내부 구조가 자주 변경될 수 있는 경우** 반복자 패턴을 적용하면 클라이언트 코드 변경 없이 유지 가능
    
- Java, Python 등 대부분의 언어는 반복자 패턴을 **언어 차원에서 내장**하고 있어 따로 구현할 필요 없는 경우가 많음
    
- 커스텀 컬렉션이나 **비표준 탐색 흐름이 필요한 경우 직접 반복자 구현** 고려
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Composite Pattern]]|트리 구조처럼 계층적 객체를 다룰 때 반복자 패턴과 함께 사용됨|
|반복자 패턴|컬렉션을 순차적으로 순회|
|[[Visitor Pattern]]|객체 구조는 유지한 채 요소별 작업을 캡슐화|