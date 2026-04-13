---
layout: default
title: My MD Blog
description: Markdown notes and docs
---

## 문서 목록

- [포트폴리오](포트폴리오/)


---

## 시작하기

- `docs/` 아래에 원하는 `*.md` 문서를 추가합니다.
- 폴더별 `index.md`를 만들면 `/폴더명/` 경로로 접근할 수 있습니다.




## 문서 추가 규칙

1. 파일은 `docs/` 아래에 둡니다.
2. 각 문서 상단에 front matter를 넣습니다.
3. 폴더에 `index.md`를 만들면 탐색이 편해집니다.

```md
---
layout: default
title: 문서 제목
description: 문서 설명
---
```



## GitHub Pages 설정

1. `Settings > Pages` 이동
2. `Deploy from a branch` 선택
3. Branch: `main`(또는 `master`)
4. Folder: `/docs`
5. 저장 후 1~5분 대기

## URL 예시

- 메인: `https://YOUR_ID.github.io/my-md-blog/`
- 포트폴리오: `https://YOUR_ID.github.io/my-md-blog/포트폴리오/`

