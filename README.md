# 박소연 | Software QA / Test Automation Portfolio

소프트웨어 품질 검증과 테스트 자동화에 관심을 가진 신입 개발자입니다.  
OpenAPI 명세 기반 REST API 테스트 자동화, 오류 응답 검증, 실패 케이스 재현 문서화, CI 기반 반복 검증 환경 구축 경험을 보유하고 있습니다.

현대오토에버 Embedded SW QA Engineer 직무에서 요구하는 SW 품질 점검, 품질 지표 모니터링, 이슈 원인 분석 및 재발 방지 업무에 필요한 기본기를 중심으로 포트폴리오를 구성했습니다.

> 공개 포트폴리오 특성상 과거 재직 회사의 내부 제품명, 상세 테스트 항목, 수치, 영업비밀성 정보는 제외했습니다.

---

## Target Role

### Embedded SW QA Engineer

관심 업무는 다음과 같습니다.

- 요구사항 및 명세 기반 SW 품질 검증
- Python 기반 테스트 자동화 및 데이터 처리
- 오류 응답, 상태 변화, 예외 케이스 검증
- CI 환경을 활용한 반복 가능한 품질 점검
- 실패 케이스 재현 절차 문서화 및 원인 분석 지원

직접적인 차량제어 SW 또는 AUTOSAR 실무 경험은 없지만, 명세와 실제 동작을 대조하고 오류를 재현 가능한 형태로 정리한 경험을 바탕으로 SW 품질 점검 업무에 빠르게 적응하고자 합니다.

---

## Skills

| Category | Skills |
|---|---|
| Language | Python, Java, C 기초 |
| Backend | Spring Boot, REST API |
| Test Automation | pytest, requests, OpenAPI/Swagger 기반 테스트 |
| Database | MySQL, SQL 기본 |
| CI/CD | GitHub Actions, Jenkins |
| DevOps / Tooling | Docker, Git, GitHub |
| QA Practice | API 명세 검증, 예외 케이스 설계, 오류 응답 검증, 실패 재현 문서화 |

---

## Experience

### Software Quality Engineer Intern

**기간:** 2026.03 ~ 2026.05  
**역할:** REST API 테스트 자동화 및 소프트웨어 품질 검증

#### 주요 업무

- OpenAPI/Swagger 명세를 분석하여 REST API 테스트 케이스 구성
- Python, pytest, requests 기반 API 자동화 테스트 구현
- 필수값 누락, 타입 오류, null/empty, 경계값 등 예외 케이스 검증
- HTTP status뿐 아니라 response body, success flag, error code까지 확인
- 실패 케이스의 입력값, 기대 결과, 실제 결과, 재현 절차 문서화
- CI 기반 정기 실행 결과 확인 및 리포트 관리
- 데모 웹 서비스의 화면 전환, 결과 표시, 오류 피드백 등 사용자 흐름 검증 보조

#### 직무 연결 포인트

이 경험을 통해 단순히 기능 실행 여부만 확인하는 것이 아니라, 명세와 실제 응답의 차이를 확인하고 오류 상황을 재현 가능한 형태로 정리하는 방식의 품질 검증을 수행했습니다.  
이는 차량제어 SW 플랫폼 품질 점검 업무에서 요구되는 요구사항 준수 확인, 이슈 원인 분석, 재발 방지 관리의 기초 역량과 연결됩니다.

---

## Projects

## 1. Spec-Based API Test Automation

### Overview

OpenAPI 명세를 기반으로 REST API 테스트 케이스를 구성하고, Python 자동화 테스트를 통해 정상/예외 응답을 반복 검증한 프로젝트입니다.

### Tech Stack

- Python
- pytest
- requests
- OpenAPI/Swagger
- GitHub Actions

### What I Did

- API 명세를 기준으로 요청 파라미터, 필수값, 타입, 응답 구조를 분석했습니다.
- 필수값 누락, 잘못된 타입, 빈 문자열, null, 경계값 등 예외 케이스를 구성했습니다.
- HTTP status code만 확인하지 않고 응답 body, success flag, error code를 함께 검증했습니다.
- 실패 케이스는 입력값, 기대 결과, 실제 결과, 재현 절차 기준으로 정리했습니다.
- CI 환경에서 테스트가 반복 실행될 수 있도록 구성하고 결과 리포트를 관리했습니다.

### Result

- 수동으로 반복 확인하던 API 검증 흐름을 자동화했습니다.
- 명세와 실제 응답이 다른 케이스를 재현 가능한 형태로 정리했습니다.
- 오류 발생 시 원인 파악에 필요한 입력 조건과 응답 정보를 구조화했습니다.

### Relevance to Hyundai AutoEver

Embedded SW QA Engineer 직무는 SW 품질 점검, 품질 지표 모니터링, 필드 이슈 원인 분석 및 재발 방지 점검을 수행합니다.  
이 프로젝트는 명세 기반으로 동작을 검증하고, 실패 조건을 재현 가능하게 문서화했다는 점에서 해당 직무와 연결됩니다.

---

## 2. URL Shortener Jenkins CI Pipeline

### Overview

URL Shortener 백엔드 프로젝트에 Jenkins 기반 CI 환경을 구축하고, 정적 분석·타입 검사·테스트·커버리지 확인을 품질 gate로 구성한 프로젝트입니다.

### Tech Stack

- Python
- FastAPI
- Jenkins
- Docker
- pytest
- ruff
- mypy
- coverage

### What I Did

- Jenkins self-hosted CI 환경을 구축했습니다.
- Docker 기반 agent 실행 환경을 구성했습니다.
- ruff, mypy, pytest, coverage를 품질 gate로 설정했습니다.
- 테스트 결과와 coverage report를 artifact로 관리했습니다.
- 실행 경로, 권한, Docker mount 문제를 분리해 원인을 파악하고 수정했습니다.

### Result

- 코드 변경 시 반복적으로 품질 검증이 수행되는 구조를 만들었습니다.
- 테스트 실패, 타입 오류, 정적 분석 오류를 CI 단계에서 확인할 수 있도록 했습니다.
- 품질 검증 결과를 리포트 형태로 남겨 문제 재현과 추적이 가능하도록 했습니다.

### Relevance to Hyundai AutoEver

현대오토에버 Embedded SW QA Engineer 직무의 우대사항에는 Jenkins 사용 경험이 포함되어 있습니다.  
이 프로젝트는 Jenkins를 단순 실행 도구가 아니라, 품질 기준을 자동으로 확인하는 검증 환경으로 구성했다는 점에서 SW 품질 모니터링 업무와 연결됩니다.

---

## 3. Time To Pill Backend & Collaboration Project

### Overview

복약 관리 서비스를 주제로 한 팀 프로젝트에서 PM과 백엔드 역할을 수행했습니다.  
프론트엔드와 백엔드가 동일한 기준으로 개발할 수 있도록 API 응답 구조와 Mock 기준을 먼저 정리했습니다.

### Tech Stack

- Java
- Spring Boot
- MySQL
- Swagger
- Git

### What I Did

- API 응답 구조와 Mock 데이터를 정리했습니다.
- Swagger 기반으로 API 명세를 공유했습니다.
- 프론트엔드와 백엔드 간 요청/응답 기준 차이를 줄였습니다.
- 응답 구조 변경 시 영향 범위를 팀원에게 공유했습니다.
- DB 구조를 설계하고 백엔드 기능 구현을 담당했습니다.

### Result

- 프론트엔드와 백엔드가 병렬로 개발할 수 있는 기준을 마련했습니다.
- 변경 사항을 문서화하고 공유하여 협업 과정의 혼선을 줄였습니다.
- 요구사항, API 명세, 구현 결과 간 정합성을 유지하는 경험을 쌓았습니다.

### Relevance to Hyundai AutoEver

SW 품질 점검 업무에서는 개발 산출물과 요구사항 사이의 정합성을 확인하는 역량이 중요합니다.  
이 프로젝트는 협업 과정에서 기준을 정리하고, 변경 영향을 관리한 경험이라는 점에서 품질 프로세스 점검 업무와 연결됩니다.

---

## Why Software QA

저는 결과가 한 번 정상적으로 나온 것보다, 어떤 조건에서 실패하고 그 실패가 다시 재현되는지를 확인하는 과정에 더 관심이 있습니다.  
API 테스트 자동화와 CI 구축 경험을 통해 명세, 입력 조건, 응답, 오류 코드, 실행 환경을 기준으로 문제를 좁혀가는 방식을 익혔습니다.

앞으로는 차량제어 SW 플랫폼과 같이 안정성과 품질 기준이 중요한 분야에서, 요구사항을 정확히 이해하고 반복 가능한 검증 체계를 만드는 QA 엔지니어로 성장하고자 합니다.

---

## Contact

- Email: sypark911@naver.com
