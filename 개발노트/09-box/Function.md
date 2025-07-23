---
type: learn
created: 2025-07-23(수) / 23:13
topic: ""
category: backend
summary: ""
tags: 
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-07-23
review_success: false
related_concepts:
---
---

## ✅ 함수 (Function)

### 🔤 용어 해석

- **Function**: 기능, 작용  
    → **입력값을 받아서 일정한 처리를 한 뒤 결과를 반환하는 코드 블록**
    

---

### 📌 개념 정리

- 중복 없이 **특정 작업을 반복 실행**하기 위해 사용
    
- 같은 동작을 여러 번 호출해 사용할 수 있는 **재사용 가능한 명령 집합**
    
- 하나의 **입력 → 처리 → 출력** 흐름을 가진다
    

---

### ⚙️ 함수의 기본 구조 (예: Python)

```python
def add(a, b):
    return a + b
```

|구성 요소|설명|
|---|---|
|`def`|함수 정의 키워드|
|`add`|함수 이름|
|`a, b`|매개변수 (입력값)|
|`return`|결과 반환|

---

### 💬 실무 예시

- 총합 계산 함수
    

```javascript
function sum(arr) {
    let total = 0;
    for (let num of arr) total += num;
    return total;
}
```

---

### 🔁 관련 개념 비교

| 구분    | 함수(Function)            | [[Method\|메서드(Method)]] |
| ----- | ----------------------- | ----------------------- |
| 위치    | 클래스 밖에서도 정의 가능          | 클래스 내부에만 존재             |
| 소속    | 독립적                     | 객체에 소속됨 (`객체.메서드()`)    |
| 예시 언어 | C, JavaScript, Python 등 | Java, Python, C++ 등     |

---

### 🎯 핵심 요약

- 함수는 **입력값 → 처리 → 출력값** 구조
    
- 코드 재사용성 향상, 가독성 증가
    
- 함수는 **객체 없이도 존재 가능**
    

---

### 🧠 학습 메모

- 함수 = “값을 넣으면 결과를 돌려주는 상자”
    
- 함수 vs 메서드 차이는 **소속 여부**
    
- 리턴값이 없는 함수도 존재 (`void`, `None` 등)
    

---