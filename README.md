# Blog Template

GitHub Pages + Jekyll 기반 `md` 블로그 템플릿입니다.

## 핵심 포인트

- `docs`를 Pages 소스로 사용합니다.
- 현재 설정은 **레포 이름이 `blog`일 때 바로 동작**하도록 맞춰져 있습니다.
- 디자인은 `ch_lecture`에서 사용 중인 레이아웃/스타일과 동일한 계열입니다.

## 구조

- `docs/` : 사이트 소스
- `docs/_config.yml` : 사이트 설정
- `docs/_layouts/default.html` : 공통 레이아웃
- `docs/assets/css/style.scss` : 공통 스타일
- `docs/index.md` : 홈

## 배포 방법

1. `blog` 폴더 내용을 새 레포 루트로 복사합니다.
2. GitHub `Settings > Pages`로 이동합니다.
3. `Deploy from a branch` 선택 후 `main`(또는 `master`) + `/docs` 선택
4. 저장 후 1~5분 대기

## 반드시 확인할 설정

`docs/_config.yml`

- 레포 이름이 `blog`면 그대로 사용:
  - `baseurl: "/blog"`
  - `repository_url: "https://github.com/YOUR_ID/blog"`
- 레포 이름이 다르면 `baseurl`/`repository_url`을 그 이름으로 변경
- 사용자 페이지(`YOUR_ID.github.io`)로 배포하면 `baseurl: ""`

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
