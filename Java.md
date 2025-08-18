---
type: learn
created: 2025-08-18(월) / 23:47
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-08-18
review_success: false
related_concepts: []
---
## ✅ 자바(Java)

### 🔤 용어 해석

- Java: 자바, 객체지향 기반의 범용 프로그래밍 언어
    
- 👉 [[OOP(Object-Oriented Programming)]] 중심 설계로 플랫폼 독립성과 풍부한 API를 제공
    

---

### 🧩 자바란?

| 항목     | 설명                                                                            |
| ------ | ----------------------------------------------------------------------------- |
| **정의** | JVM 위에서 실행되는 객체지향형 범용 프로그래밍 언어                                                |
| **목적** | 코드 이식성, 보안성, 네트워크 중심의 애플리케이션 개발                                               |
| **분류** | [[Compiled Language]], [[Object-Oriented Language]], [[Platform Independent]] |


---

### 🧱 구성 요소

|구성 요소|설명|
|---|---|
|클래스 & 객체|`class`, `new`, `this`, 생성자 등|
|접근 제어자|`public`, `private`, `protected`, default|
|상속/다형성|`extends`, `implements`, `@Override` 등|
|예외 처리|`try-catch`, `throw`, `throws`, `finally`|
|주요 키워드|`static`, `final`, `abstract`, `interface`|
|자료형/컬렉션|`String`, `ArrayList`, `HashMap` 등|

---

### 📚 예시로 이해하기1(이해하기 쉬운 직관적인 예시)

- TV라는 클래스를 만들고 켜기/끄기 기능을 구현 →  
    `클래스`는 설계도, `객체`는 실제 TV
    

---

### 📚 예시로 이해하기2 (언어 명시)

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, Java!");
    }
}

// 예외 처리 예시
try {
    int x = 5 / 0;
} catch (ArithmeticException e) {
    System.out.println("0으로 나눌 수 없습니다.");
} finally {
    System.out.println("예외 처리 종료");
}
```

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|플랫폼 독립성|JVM을 통해 OS에 상관없이 실행 가능|
|객체지향 중심|캡슐화, 상속, 다형성 등 핵심 원칙 적용|
|예외 처리 체계|컴파일 시점부터 오류 예방 가능|
|표준 API 풍부|`java.util`, `java.io`, `java.lang` 등 방대한 라이브러리|
|정적 타입|컴파일 시점에 자료형 고정|

---

### 🎯 실무 팁

- 인터페이스 기반 설계를 통해 **유지보수성과 확장성** 확보
    
- [[Spring]] 등 프레임워크를 학습할 땐 **접근 제어자, DI, 예외 처리**에 익숙해져야 함
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Python]]|동적 타이핑, 간결한 문법, 인터프리터 기반|
|자바(Java)|정적 타이핑, 클래스 기반 설계, 컴파일 기반|