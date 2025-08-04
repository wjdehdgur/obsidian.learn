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

## ✅ 인터프리터 패턴(Interpreter Pattern)

### 🔤 용어 해석

- **Interpreter**: 해석기, 번역기
- 👉 인터프리터 패턴은 **언어나 표현식을 해석하는 방법을 클래스 구조로 정의**하여, 문장을 해석하고 실행할 수 있도록 하는 패턴

---

### 🧩 인터프리터 패턴이란?

| 항목 | 설명 |
|------|------|
| **정의** | 특정 언어나 표현식을 **문법으로 정의하고**, 해당 문법에 따라 해석하는 클래스를 구현하는 설계 패턴 |
| **목적** | 표현식을 트리 형태로 구성한 뒤, 각 노드에 의미를 부여하고 **재귀적으로 해석** |
| **분류** | [[GOF(Gang of Four Design Patterns)]] 중 **행위(Behavioral) 패턴**

---

### 🧱 구조 구성요소

| 구성 요소 | 역할 |
|-----------|------|
| **AbstractExpression** | 모든 표현식 클래스가 구현해야 할 인터페이스 |
| **TerminalExpression** | 더 이상 분해할 수 없는 표현식 (숫자, 변수 등) |
| **NonTerminalExpression** | 다른 표현식을 포함하여 계산 또는 조합 |
| **Context** | 해석에 필요한 전역 정보(예: 변수 테이블 등)

---

### 📚 예시로 이해하기 (Java 스타일 – 간단한 수식 해석기)

```java
interface Expression {
    int interpret();
}

class Number implements Expression {
    private int value;
    public Number(int value) { this.value = value; }
    public int interpret() { return value; }
}

class Add implements Expression {
    private Expression left, right;
    public Add(Expression left, Expression right) {
        this.left = left;
        this.right = right;
    }
    public int interpret() {
        return left.interpret() + right.interpret();
    }
}

// 사용
Expression expr = new Add(new Number(2), new Number(3));
System.out.println(expr.interpret()); // 출력: 5
````

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|**장점**|문법을 객체로 표현하여 **구조적 해석 및 확장성 확보**|
|**단점**|복잡한 문법일수록 **클래스 수 증가**, 성능 저하|
|**적합 상황**|수식 해석기, 도메인 언어 DSL, SQL 파서 등|

---

### 🎯 실무 팁

- 간단한 문법이나 도메인 한정 언어(DSL)에는 적합
    
- 복잡한 문법은 [[Visitor Pattern]] 또는 파서 생성기(ANTLR, yacc 등)와 함께 사용
    
- 재귀 구조를 사용하므로 **트리 기반 구조 이해 필수**
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Visitor Pattern]]|구조는 유지하고, 다양한 연산을 분리|
|인터프리터 패턴|표현식 자체를 구조화하고 직접 해석|
|[[Composite Pattern]]|트리 구조 표현은 유사하나, 해석보다는 조합이 목적|