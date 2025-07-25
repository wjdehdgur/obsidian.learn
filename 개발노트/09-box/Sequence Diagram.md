---
type: learn
created: 2025-07-21(월) / 23:28
topic: ""
category: backend
summary: ""
tags: []
concept: ""
review_count: 0
mistake_count: 0
last_review: 2025-07-21
review_success: false
related_concepts:
---

---
## ✅ 순차 다이어그램 (Sequence Diagram)

### 🔤 용어 해석

- **Sequence**: 순서, 순차적
    
- **Diagram**: 도식, 그림, 다이어그램
    
- 👉 따라서 "Sequence Diagram"은 **순서를 시각적으로 표현한 다이어그램**
    

---

### 🧩 순차 다이어그램이란?

|항목|설명|
|---|---|
|**정의**|**객체 간의 메시지 교환**을 시간의 흐름에 따라 **순차적으로 표현**한 UML 다이어그램입니다.|
|**포함 범주**|UML의 **행위 다이어그램(Behavior Diagram)** 중 하나|
|**표현 방식**|세로 방향은 시간 흐름, 가로 방향은 상호작용하는 객체들|
|**목적**|어떤 객체가 어떤 시점에 어떤 메시지를 주고받는지를 표현하여 시스템의 **구체적 실행 흐름**을 이해하는 데 도움|

---

### 🔄 순차 다이어그램 구성 요소

|구성 요소|설명|
|---|---|
|**객체 (Object)**|다이어그램 상단에 표시되며, 서로 메시지를 주고받는 주체|
|**생명선 (Lifeline)**|객체 아래로 그려진 점선, 시간의 흐름을 의미|
|**메시지 (Message)**|객체 간에 주고받는 요청/응답 (→ 화살표로 표시)|
|**자기 호출 (Self-message)**|객체가 **자기 자신에게 메시지를 보내는** 경우|
|**활성화 바 (Activation Bar)**|어떤 객체가 메시지를 수신하고 실행 중일 때 표시|
|**제어 블록 (Statement Block)**|조건문/반복문 등 제어 흐름 구조를 표현할 수 있음|

---

### 🧭 순차 다이어그램의 방향

|방향|의미|
|---|---|
|**수직 방향**|**시간의 흐름**을 나타냄 (위 → 아래로 흐름 진행)|
|**수평 방향**|객체 간의 **메시지 흐름**, 즉 상호작용 대상 표시|

---

### 💬 예시로 이해하기

**상황**: 사용자가 로그인하는 과정

```
사용자 → 로그인 페이지: 로그인 요청
로그인 페이지 → 서버: 아이디/비밀번호 확인 요청
서버 → DB: 사용자 정보 조회
DB → 서버: 결과 반환
서버 → 로그인 페이지: 로그인 성공/실패 결과 전송
로그인 페이지 → 사용자: 결과 표시
```

👉 위 과정을 순차 다이어그램으로 그리면, 객체들의 메시지가 시간 순으로 정렬되어 보여요.

---

### 🎯 특징 요약

|항목|설명|
|---|---|
|모델링 대상|**시간 흐름을 가진 상호작용**|
|핵심 키워드|메시지, 객체, 생명선, 시간 순서|
|다이어그램 위치|UML의 **동적 다이어그램** (행위 다이어그램)|
|실무 용도|API 흐름 설명, 기능별 요청 흐름 파악, 테스트 시나리오 작성 등|

---

### 🧠 정리

- 순차 다이어그램은 **행위 다이어그램**의 일종이다.
    
- 시스템의 **동적인 상호작용**을 시간 순서대로 표현한다.
    
- **객체 간 메시지 흐름**을 파악하기 위해 사용한다.
    

---
