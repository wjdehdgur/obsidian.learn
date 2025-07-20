# 🧭 개발 대시보드

## 📆 최근 작성된 개발 일지 (카드 스타일)

```dataviewjs
const pages = dv.pages('"logs/daily"')
  .where(p => p.type === "daily")
  .sort(p => p.date, 'desc')
  .limit(10);

for (let p of pages) {
  dv.paragraph(`
---
🗓 **${p.date?.toFormat("yyyy-MM-dd") ?? "날짜 없음"}**  
📁 **프로젝트**: ${p.project ?? "_미입력_"}  
📝 **주제**: ${p.topic ?? "_기재 안됨_"}  
🧾 **요약**: ${p.summary ?? "_요약 없음_"}  
🔗 [[${p.file.name}]]
---
  `);
}
```

## ➕ 빠른 기록 시작

```button
name 생성: 오늘의 개발일지
type note
template .templates/daily
folder logs/daily
open true
```


## ➕ 회고 / 학습 노트 생성nnn


```button
name 생성: 이번 주 회고
type note
template .templates/review
folder logs/weekly
open true
```

```button
name 생성: 새로운 학습 노트
type note
template .templates/learn
folder knowledge/backend
open true
```


