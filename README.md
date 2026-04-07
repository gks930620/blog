# MD Blog Template

GitHub Pages + Jekyll 기반의 `md` 문서 블로그 템플릿입니다.

## 구조

- `docs/` : 실제 사이트 소스
- `docs/_config.yml` : 사이트 설정
- `docs/_layouts/default.html` : 공통 레이아웃
- `docs/assets/css/style.scss` : 공통 스타일
- `docs/index.md` : 홈

## 사용 방법

1. 이 `md_blog_template` 폴더 내용을 새 레포지토리 루트로 복사합니다.
2. GitHub에서 `Settings > Pages`로 이동합니다.
3. `Deploy from a branch` 선택 후 `master`(또는 `main`) + `/docs`를 선택합니다.
4. `docs/_config.yml`에서 아래 항목을 새 레포 기준으로 수정합니다.
   - `url`
   - `baseurl`
   - `repository_url`
5. `docs/` 아래에 원하는 `*.md` 문서를 추가합니다.

## 새 문서 작성 예시

```md
---
layout: default
title: 문서 제목
description: 문서 한 줄 설명
---

## 문서 본문

- 항목 1
- 항목 2
```

