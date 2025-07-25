---
type: learn
created: 2025-07-23(수) / 00:57
topic: ""
category: backend
summary: ""
tags: []

# ✅ 오답 복습 관리
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-07-23
review_success: false
related_concepts: []
---
---

## ✅ 오버라이딩 (Overriding)

### 🔤 용어 해석

- **Override**: 덮어쓰기, 재정의
    
- 부모로부터 물려받은 기능을 **같은 이름으로 바꾸어 실행 내용만 새로 정의**
    

---

### 📌 개념 정리

- **상속받은 메서드의 동작을 자식 클래스에서 변경**하는 것
    
- **이름, 매개변수, 반환값 모두 동일**해야 오버라이드로 인정됨
    
- 다형성(Polymorphism)의 핵심 요소
    
- 실행 시점은 런타임(동적 바인딩)
    

---

### ⚙️ 구성 조건

1. 부모 클래스에 메서드 존재
    
2. 자식 클래스에서 **동일한 시그니처(이름, 매개변수)**로 재정의
    
3. 접근 제한자(예: public)는 부모보다 더 좁을 수 없음
    
4. 언어나 환경에 따라 `@Override` 같은 명시 필요 (Java 등)
    

---

### 💬 예시 (Java 기준)

```java
class Animal {
    void sound() {
        System.out.println("동물이 소리를 낸다");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("멍멍!");
    }
}
```

- `Dog`는 `Animal`의 `sound()`를 오버라이드하여 다른 동작을 정의함
    

---

### 🔁 관련 개념 비교

| 구분     | [[Overloading\|오버로딩 (Overloading)]] | 오버라이딩 (Overriding)  |
| ------ | ----------------------------------- | ------------------- |
| 정의     | 같은 이름, **다른 매개변수**                  | 같은 이름, **같은 매개변수**  |
| 위치     | 같은 클래스 내                            | 상속 관계 (자식 클래스에서 정의) |
| 목적     | 다양한 입력 처리                           | 기존 기능 재정의           |
| 바인딩 시점 | 컴파일 타임                              | 런타임                 |

---

### 🎯 핵심 요약

- 오버라이드는 **상속관계에서 부모 메서드를 자식이 재정의**
    
- 다형성의 핵심이며, 런타임에 어떤 메서드를 쓸지 결정됨
    
- 꼭 메서드 이름과 매개변수 모두 **일치**해야 함
    

---

### 🧠 학습 메모

- 시험에 자주 출제되는 오버로딩 vs 오버라이드 구분 숙지
    
- 오버라이드는 다형성 문제에 자주 출제됨 (예: 동적 바인딩)
    
- 인터페이스 구현할 때도 오버라이드 사용
    

---