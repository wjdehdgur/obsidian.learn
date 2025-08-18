---
type: learn
created: 2025-08-18(월) / 23:16
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
---

## ✅ 예외 처리(Exception Handling)

### 🔤 용어 해석

- Exception: 예외
    
- Handling: 처리
    
- 👉 프로그램 실행 중 발생하는 **예기치 못한 오류를 잡아내고 정상 흐름으로 복구하는 과정**
    

---

### 🧩 예외 처리란?

|항목|설명|
|---|---|
|**정의**|프로그램 실행 중 오류가 발생해도 **프로그램이 중단되지 않고 안정적으로 계속 실행되도록** 처리하는 기법|
|**목적**|실행 시간 오류(Runtime Error) 발생 시 시스템 보호 및 복구|
|**기준 언어**|주로 Java 기준으로 출제됨|

---

### 🧱 예외 처리 구문 (Java 기준)

|키워드|설명|
|---|---|
|`try`|예외 발생 가능성이 있는 코드 블록|
|`catch`|발생한 예외를 처리|
|`finally`|예외 발생 여부와 관계없이 항상 실행|
|`throw`|예외를 명시적으로 발생시킴|
|`throws`|예외 발생 가능성을 메서드 시그니처에 명시|

---

### 📚 예시로 이해하기1

```java
try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("0으로 나눌 수 없습니다.");
} finally {
    System.out.println("항상 실행되는 블록");
}
```

---

### 🧠 특징 요약

|항목|설명|
|---|---|
|구조화된 처리|`try-catch-finally`로 흐름 제어|
|Checked vs Unchecked|컴파일 강제 여부에 따라 구분|
|예외 클래스 상속 구조|`Throwable` → `Exception`, `Error`|
|[[Garbage Collector]]와 연계|예외 발생 시 참조 끊긴 객체는 GC 대상|

---

### 🎯 실무 팁

- 핵심 로직은 반드시 `try-catch`로 보호
    
- `finally`는 **자원 해제(DB 연결, 파일 닫기 등)**에 주로 사용
    
- `catch` 블록에서는 반드시 **로그 또는 메시지 처리**
    
- `throws`를 남용하면 예외 흐름 추적 어려움 → 필요한 경우에만 사용
    

---

### 🧩 관련 개념 비교

|개념|설명|
|---|---|
|[[Checked Exception]]|컴파일 타임에 처리 강제됨 (예: IOException)|
|[[Unchecked Exception]]|런타임에 처리 (예: NullPointerException)|
|[[Error]]|시스템 오류, 복구 불가|
|[[Garbage Collector]]|예외 후 참조 끊긴 객체 정리|

---