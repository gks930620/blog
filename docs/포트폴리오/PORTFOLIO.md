# Programmers Helper (IntelliJ Plugin)

프로그래머스 코딩테스트 문제를 IntelliJ 안에서 바로 시작할 수 있게 만든 생산성 플러그인입니다.  
Marketplace 배포까지 완료했고, 서버/운영 인프라 없이 사용하는 구조입니다.

## 1) 어떤 문제를 해결했는가

코딩테스트 문제를 풀기 전, 아래 준비 작업이 반복적으로 발생했습니다.

- 문제별 클래스 파일 생성
- `solution` 시그니처 확인 후 수동 작성
- 예제/테스트 케이스를 직접 복사해 `main`에 붙여넣기

즉, 풀이 이전의 보일러플레이트 작업이 누적되어 시작 속도가 느려지는 문제가 있었습니다.

## 2) 어떻게 해결했는가

`Programmers Helper` Tool Window를 통해 문제 템플릿을 즉시 가져오도록 구현했습니다.

- 문제 목록 인덱스(`templates/index.txt`)를 읽어 동적 목록 구성
- 검색어 + 언어 필터로 원하는 문제 빠르게 탐색
- 선택한 문제의 템플릿 코드를 우측 패널에서 즉시 미리보기
- 원클릭 파일 생성(덮어쓰기 확인 포함) 후 IDE 에디터 자동 오픈
- 클립보드 복사 기능으로 원하는 위치에 바로 붙여넣기 가능

## 3) 내가 작업한 핵심 구현

- IntelliJ ToolWindow UI 구성 (좌: 문제 목록 / 우: 코드 미리보기)
- 템플릿 리소스 로더 및 문제 리포지토리 구현
- 파일 생성 시 `WriteCommandAction` 기반 안전한 쓰기 처리
- 초기 폴더를 프로젝트 경로로 맞춰 사용 동선 단축
- 현재 Java 템플릿 548개를 인덱싱해 즉시 사용 가능하게 구성

## 4) 기술 스택

- Kotlin, Java 21
- IntelliJ Platform Gradle Plugin
- IntelliJ SDK (ToolWindow, FileChooser, VFS, Editor API)
- JetBrains Marketplace 배포

## 5) 실행 결과 화면

아래는 실제 플러그인 동작 화면입니다.

![Programmers Helper Overview](./overview-1.png)

## 6) 결과/의미

- 문제 풀이 시작까지의 준비 시간을 크게 줄임
- 반복 수작업을 플러그인 UX로 흡수
- 배포 후에도 별도 서버 운영 없이 유지 가능한 구조 확보
