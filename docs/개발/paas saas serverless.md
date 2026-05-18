---
layout: default
title: Spring과 Serverless
description: Spring, PaaS, SaaS, Serverless를 짧게 비교하고 실무 선택 기준을 정리
---
## PaaS / SaaS / Serverless 한 번에 정리

### 1) PaaS (Platform as a Service)

- 의미: 앱 코드를 올리면 인프라 운영을 플랫폼이 대신 처리
- 예시: Railway, Render, Heroku, Google App Engine
- 잘 맞는 경우: Spring Boot 웹 API, 백오피스, 일반 서비스 서버

### 2) SaaS (Software as a Service)

- 의미: 이미 완성된 소프트웨어를 구독해서 사용
- 예시: Notion, Slack, Gmail, Figma
- 잘 맞는 경우: 직접 개발 대신 기능을 바로 써야 할 때

### 3) Serverless

- 의미: 요청/이벤트가 있을 때만 함수가 실행되고 사용량만큼 과금
- 예시: AWS Lambda, Google Cloud Functions, Azure Functions, Cloudflare Workers
- 잘 맞는 경우: 배치, 파일 변환, 알림 발송, 이벤트 후처리

## spring 개발자는 어떻게 하면 되나
기본적으로 spring boot 프로젝트를 PaaS에 올리면 됨. 
이미 spring boot 프로젝트를 만든 순간부터 Serverless 제품들은 사용 안해도 되는 경우가 많음.

단  한 달에 딱 한 번, 월말 새벽 3시에만 실행되는 대규모 정산 기능이나 전체 회원 대상 알림 발송 기능이 필요한 경우 
PAAS 제품의 사양을 그에 맞춰서 높이면 평상시에는 낭비가 너무 심함
가끔 필요한 대규모 작업은 serverless 제품으로 구현해서 필요할 때만 실행
... 했었는데 요즘엔 PAAS 제품들도 자동으로 스케일링이 잘 되니까 굳이 serverless 제품을 쓸 필요가 없는 경우가 많음.

# 결론 
spring boot 프로젝트를  했다면 그냥 railway 등 PAAS 하나 선택해서 잘 하면 됨
spring이 필요없이 단순히 특정 작업들만 할거다 ==> 애초에 serverless 제품 선택해서 구현 !
SAAS는  개발이랑 상관없고 notion 같은거 잘 쓰면 됨 끝.









