<div align="center">

# 박소연 | Soyeon Park

### Reliability-Oriented Software Engineer

**실패를 재현하고, 시스템의 상태 변화와 복구 과정을 검증합니다.**

API 테스트 자동화와 CI 품질 게이트를 구축해 왔으며,  
현재는 장애 감지·복구·관측 가능성을 다루는 SRE로 역량을 확장하고 있습니다.

<br>

[![Email](https://img.shields.io/badge/Email-sypark911%40naver.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:sypark911@naver.com)
[![GitHub](https://img.shields.io/badge/GitHub-soyeon911-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/soyeon911)
[![Velog](https://img.shields.io/badge/Velog-soyeon911-20C997?style=flat-square&logo=velog&logoColor=white)](https://velog.io/@soyeon911/posts)

</div>

---

## About Me

소프트웨어를 만드는 과정과 검증하는 과정은 서로 분리되지 않는다고 생각합니다.

정상 응답만 확인하기보다 **실제 데이터가 의도한 상태로 변경**되었는지,  
일부 처리만 성공했을 때 **정합성이 유지**되는지, 장애 이후 **안전하게 복구**되는지 확인합니다.

REST API 테스트 자동화 시스템과 Jenkins 기반 CI 품질 게이트를 직접 설계했습니다.  
이 경험을 바탕으로 반복되는 검증을 자동화하고, 실패를 빠르게 감지하고,  
운영 가능한 시스템을 만드는 엔지니어로 성장하고 있습니다.

---

## Core Competencies

| Area | Experience |
|---|---|
| **Test Automation** | OpenAPI 기반 테스트 생성, API·통합·단위 테스트, 회귀 테스트 자동화 |
| **CI/CD** | Jenkins·GitHub Actions 기반 품질 게이트 및 자동 실행 환경 구축 |
| **Reliability** | Timeout·Retry·Backoff·Interlock·Health Check·안전 상태 복구 설계 |
| **Backend** | REST API, 상태 전이, 데이터베이스 스키마, 인증·인가 구현 |
| **Failure Analysis** | 실패 원인 분류, 재현 조건 정리, 응답과 실제 상태의 정합성 검증 |

---

## Experience

### 한국정보통신기술협회(TTA)

**SW 시험·검증 업무 지원**  
`2026.07 – Present`

의료·디지털헬스케어 분야 연구개발 결과물의 요구사항과 시험 기준을 분석하고,  
시험 결과와 판단 근거를 추적 가능한 형태로 문서화하고 있습니다.

- 요구사항 및 시험 기준 분석
- 시험 조건·기대 결과·실제 결과 문서화
- 결함 재현 절차와 검증 근거 정리
- 시험 결과와 실제 시스템 상태의 일치 여부 확인

---

### Suprema

**Software Quality Engineer Intern**  
`2026.03 – 2026.05`

생체인식 REST API 서버의 테스트 케이스 생성부터 실행, 판정, 리포팅까지 연결되는  
테스트 자동화 시스템을 설계하고 구현했습니다.

- Swagger/OpenAPI 명세 분석 및 테스트 입력 구조화
- 필수값 누락, 타입 오류, `null`, 경계값 등 규칙 기반 테스트 생성
- `pytest` 기반 API 테스트 실행 환경 구축
- HTTP status와 response body를 함께 확인하는 판정 기준 설계
- 실패 원인을 `Schema · Domain · State · Runtime` 관점으로 분류
- GitHub Actions 기반 자동 회귀 테스트 구성
- Web Dashboard 및 Excel 테스트 리포트 구현
- 자동화 시스템의 설계와 결과를 사내 세미나에서 발표

---

## Featured Projects

### 01. URL Shortener CI

> 테스트 코드부터 실행 환경, 품질 기준, 결과 리포트까지 연결한 CI 자동화 프로젝트

[Repository](https://github.com/soyeon911/TestAutomation)

#### Problem

테스트가 개발자의 로컬 환경에 의존하면 실행 결과를 동일하게 재현하기 어렵고,  
코드 품질 기준도 일관되게 적용하기 어렵습니다.

#### Implementation

- FastAPI 기반 URL 단축 서비스 구현
- Unit·Integration·API 3계층 테스트 구성
- Hypothesis 기반 Property-based Testing 적용
- `ruff`, `mypy`, `pytest`, `coverage` 품질 게이트 구성
- Jenkins 병렬 파이프라인 구축
- Docker 동적 에이전트를 이용한 실행 환경 격리
- JUnit·Coverage·Allure 테스트 리포트 연동
- Jenkins Shared Library를 통한 파이프라인 공통화

#### Result

- 총 89개 자동화 테스트 구성
- 라인 커버리지 96% 달성
- 커버리지 기준 미달 시 빌드가 실패하도록 품질 기준 자동화
- Jenkinsfile을 약 90줄에서 2줄 수준으로 단순화
- 실행 환경과 결과 리포트를 CI 파이프라인에서 재현 가능하게 구성

#### Reliability Perspective

테스트를 많이 작성하는 것보다, 같은 기준으로 반복 실행하고  
실패 원인을 빠르게 확인할 수 있는 환경을 만드는 데 집중했습니다.

#### Tech

`Python` `FastAPI` `SQLAlchemy` `pytest` `Hypothesis`  
`Jenkins` `Docker` `Allure` `ruff` `mypy`

---

### 02. Mini Equipment Controller

> 상태 전이와 장애 복구 흐름을 중심으로 구현한 경량 장비 제어 시스템

[Repository](https://github.com/soyeon911/MiniEqController)

#### Problem

장비 제어 시스템은 정상 명령 처리뿐 아니라 Timeout, 중복 명령,  
인터락 위반, 실행 중단과 같은 비정상 상황에서도 안전한 상태를 유지해야 합니다.

#### Implementation

- 장비 상태 머신 설계

```text
Idle → Init → Ready → Run
                  ↘ Error → Recover
```

- Door·Vacuum 인터락 조건 검증
- 명령별 Timeout과 Retry 처리
- 재시도 간 Backoff 적용
- STOP 요청 시 실행 취소 및 대기 명령 제거
- 오류 발생 후 안전 상태 복귀
- 우선순위 기반 명령 큐 구현
- 동일 키의 최신 명령만 유지하는 Coalescing 적용
- 구조화 로그와 상태 진단 메트릭 구성
- `/healthz`, `/ready` 상태 확인 API 구현
- xUnit 기반 상태 전이 테스트 작성

#### Reliability Perspective

장애를 단순한 예외로 처리하지 않고, 감지·재시도·중단·복구가 포함된  
하나의 상태 전이 과정으로 모델링했습니다.

#### Tech

`C#` `.NET` `Minimal API` `xUnit` `Serilog` `Docker`

---

### 03. API Test Automation

> OpenAPI 명세를 반복 가능한 테스트와 판정 기준으로 변환한 실무 프로젝트

#### Problem

API 명세만으로는 실제 도메인 제약과 상태 변화까지 검증하기 어려웠고,  
명세가 변경될 때마다 테스트 케이스를 수동으로 관리해야 했습니다.

#### Implementation

- OpenAPI 명세 파싱 및 요청 필드 구조화
- 규칙 기반 테스트 케이스 자동 생성
- API 특성에 따른 검증 정책 보강
- `pytest` 기반 자동 실행 구조 구현
- HTTP status·response body·error code를 조합한 결과 판정
- 실패 유형별 결과 분류 및 리포팅
- GitHub Actions 기반 회귀 테스트 구성

#### Reliability Perspective

응답 성공 여부에만 의존하지 않고, 오류 코드와 실제 상태 변화까지 확인하도록  
검증 기준을 확장했습니다. 실패 결과에는 입력 조건과 판정 근거를 함께 남겨  
동일한 문제를 다시 재현할 수 있도록 구성했습니다.

#### Tech

`Python` `pytest` `requests` `OpenAPI` `GitHub Actions`

> 회사 프로젝트로, 공개 가능한 범위의 설계와 수행 내용만 기술했습니다.

---

## Other Projects

| Project | Description | Tech |
|---|---|---|
| [Time To Pill](https://github.com/soyeon911/Time-to-Pill) | 복약 일정·의약품 관리 서비스의 API, 인증, DB 설계 | `Spring Boot` `MySQL` `JWT` `OAuth` |
| [DataAnalysis Pro](https://github.com/soyeon911/DataAnalysis_pro) | 외부 API 데이터 수집·정규화·스냅샷 비교 ETL | `Python` `MySQL` `SQL` |
| [DateMap](https://github.com/soyeon911/datemap) | 장소와 추억을 지도에 기록하는 모바일 앱 | `React Native` `Expo` `TypeScript` |
| [Tulink](https://github.com/soyeon911/Web_project) | 튜터링 매칭 및 중복 예약 방지 웹 서비스 | `Django` `MySQL` |
| [Window Clock](https://github.com/soyeon911/WindowClock) | 시계·알람·뽀모도로 기능을 제공하는 데스크톱 앱 | `C++` `MFC` |

---

## Tech Stack

### Main

`Python` `Java` `C#` `SQL`  
`FastAPI` `Spring Boot` `.NET`  
`pytest` `Hypothesis` `xUnit`  
`Jenkins` `GitHub Actions` `Docker`  
`MySQL` `SQLAlchemy`  
`OpenAPI` `Allure` `ruff` `mypy`

### Additional Experience

`C++` `JavaScript` `TypeScript`  
`Django` `React Native`  
`GTest` `Catch2`

---

## Learning & In Progress

### FaultLab

예약·결제 시스템에 장애 조건을 주입하고, 감지와 복구 과정을 관찰하는  
신뢰성 실험 프로젝트를 설계하고 있습니다.

#### Planned Scenarios

- 동일 예약에 대한 동시 요청
- 결제 중복 처리와 멱등성 검증
- 외부 결제 API Timeout
- 처리 도중 애플리케이션 종료
- 부분 성공으로 인한 데이터 불일치
- Retry 증가에 따른 요청 증폭
- DB·Cache 장애와 복구
- 장애 발생 전후의 로그·메트릭·트레이스 비교

#### Planned Stack

`Spring Boot` `PostgreSQL` `Redis` `Docker Compose`  
`k6` `Toxiproxy` `OpenTelemetry` `Prometheus` `Grafana`

### SRE Learning Path

- Linux 시스템과 네트워크
- 컨테이너 운영과 오케스트레이션
- Logs·Metrics·Traces 기반 관측 가능성
- SLI·SLO와 Error Budget
- 부하 테스트와 용량 계획
- 장애 주입과 복구 자동화
- Infrastructure as Code
- Incident Response와 Postmortem

---

<div align="center">

### Contact

[Email](mailto:sypark911@naver.com) ·
[GitHub](https://github.com/soyeon911) ·
[Velog](https://velog.io/@soyeon911/posts)

</div>
