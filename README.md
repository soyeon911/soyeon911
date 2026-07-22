<div align="center">

# 박소연 | Soyeon Park

### Backend & Quality Engineer

**정상 동작만 확인하지 않고,
시스템의 상태 변화와 실패 흐름을 코드로 검증합니다.**

백엔드 API, 테스트 자동화, CI/CD 파이프라인을 설계하고 구현합니다.
최근에는 동시성, 장애 복구, 관측 가능성, API 보안처럼
**시스템이 실패하는 조건을 발견하고 개선하는 엔지니어링**에 관심을 두고 있습니다.

<br>

[![Email](https://img.shields.io/badge/Email-sypark911%40naver.com-EA4335?style=flat-square\&logo=gmail\&logoColor=white)](mailto:sypark911@naver.com)
[![GitHub](https://img.shields.io/badge/GitHub-soyeon911-181717?style=flat-square\&logo=github\&logoColor=white)](https://github.com/soyeon911)
[![Velog](https://img.shields.io/badge/Velog-soyeon911-20C997?style=flat-square\&logo=velog\&logoColor=white)](https://velog.io/@soyeon911/posts)

</div>

---

## About Me

소프트웨어를 만드는 과정과 검증하는 과정을 분리하지 않는 개발자입니다.

단순히 요청이 성공했는지만 확인하기보다 다음과 같은 질문을 먼저 생각합니다.

* 동일한 요청이 여러 번 들어오면 어떤 상태가 되는가?
* 일부 처리만 성공한 경우 데이터 정합성은 유지되는가?
* 잘못된 순서로 API를 호출하면 상태가 깨지지 않는가?
* 외부 서비스가 지연되거나 종료되면 시스템은 어떻게 복구되는가?
* 테스트 결과와 실제 데이터 상태가 일치하는가?

REST API 테스트 자동화 시스템과 CI 품질 게이트를 직접 설계한 경험이 있으며,
현재는 백엔드 개발 역량을 기반으로 테스트 자동화, 신뢰성, 보안 검증 영역을 확장하고 있습니다.

---

## Engineering Focus

### Backend Engineering

* REST API 및 도메인 로직 설계
* 상태 전이와 예외 흐름 모델링
* 데이터베이스 스키마 및 트랜잭션 설계
* 인증·인가와 외부 API 연동
* 중복 요청과 데이터 정합성 처리

### Test Automation

* API 명세 기반 테스트 자동화
* Unit·Integration·API 테스트
* Property-based Testing
* 상태 기반 테스트와 경계 조건 검증
* 반복 가능한 회귀 테스트 환경 구축

### Quality & Reliability

* CI/CD 품질 게이트
* 실패 원인 분류와 결과 리포팅
* Timeout·Retry·Interlock 설계
* 로그·메트릭 기반 상태 분석
* 장애 주입과 복구 흐름 검증

---

## Experience

### 한국정보통신기술협회 · TTA

**SW 시험·검증 업무 지원**
`2026.07 – Present`

연구개발 결과물을 대상으로 요구사항과 기대 결과를 검증 가능한 시험 조건으로 구조화하고, 시험 결과와 근거를 문서화하고 있습니다.

* R&D 결과물 V&V 및 요구사항 충족 여부 검증
* 시험 조건, 기대 결과, 실제 결과 정리
* 결함 재현 조건과 검증 근거 문서화
* 반복 검증 업무의 자동화 가능성 분석
* 시험 결과와 실제 시스템 상태 간 정합성 확인

---

### Suprema

**Software Quality Engineer Intern**
`2026.03 – 2026.05`

생체인식 REST API 서버의 테스트 자동화 시스템을 설계하고 구현했습니다.

* Swagger/OpenAPI 명세 분석 및 테스트 입력 구조화
* 필수값 누락, 타입 오류, `null`, 경계값 등 규칙 기반 테스트 생성
* `pytest` 기반 API 테스트 실행 환경 구축
* HTTP status와 response body를 함께 검증하는 판정 기준 설계
* 실패 원인을 `Schema · Domain · State · Runtime` 관점으로 분류
* GitHub Actions 기반 자동 회귀 테스트 구성
* Web Dashboard 및 Excel 테스트 리포트 구현
* 자동화 시스템의 설계와 결과를 사내 세미나에서 발표

> 회사 코드, 내부 데이터 및 비공개 API 정보는 공개 저장소에 포함하지 않았습니다.

---

## Featured Projects

### 01. URL Shortener CI

> 테스트 코드 작성부터 실행 환경, 품질 기준, 결과 리포트까지 연결한 CI 자동화 프로젝트

🔗 [Repository](https://github.com/soyeon911/TestAutomation)

#### 주요 구현

* FastAPI 기반 URL 단축 서비스 구현
* Unit·Integration·API 3계층 테스트 구성
* 총 89개 테스트와 96% 라인 커버리지 달성
* Hypothesis 기반 Property-based Testing 적용
* `ruff`, `mypy`, `pytest`, `coverage` 품질 게이트 구성
* Jenkins 병렬 파이프라인 구축
* Docker 동적 에이전트를 이용한 실행 환경 격리
* JUnit, Coverage, Allure 리포트 연동
* Jenkins Shared Library 적용
* Jenkinsfile을 약 90줄에서 2줄 수준으로 단순화

#### Tech

`Python` `FastAPI` `SQLAlchemy` `pytest` `Hypothesis`
`Jenkins` `Docker` `Allure` `ruff` `mypy`

---

### 02. Mini Equipment Controller

> 상태 머신과 장애 복구 흐름을 중심으로 구현한 경량 장비 제어 시스템

🔗 [Repository](https://github.com/soyeon911/MiniEqController)

#### 주요 구현

* 장비 상태 머신 설계

```text
Idle → Init → Ready → Run
                 ↓
               Error → Recover
```

* Door·Vacuum 인터락 조건 검증
* 명령별 Timeout과 Retry 처리
* 재시도 간 Backoff 적용
* STOP 요청 시 실행 취소 및 대기 명령 제거
* 오류 발생 후 안전 상태 복귀
* 우선순위 기반 명령 큐
* 동일 키의 최신 명령만 유지하는 Coalescing
* 구조화 로그와 상태 진단 메트릭
* `/healthz`, `/ready` 상태 확인 API
* xUnit 기반 상태 전이 테스트

#### Tech

`C#` `.NET` `Minimal API` `xUnit` `Serilog` `Docker`

---

### 03. Time To Pill

> 복약 일정과 의약품 정보를 관리하는 모바일 애플리케이션

🔗 [Repository](https://github.com/soyeon911/Time-to-Pill)

#### 담당 역할

* Project Manager
* Backend Developer
* API 및 데이터베이스 설계
* 팀 일정과 기능 우선순위 관리

#### 주요 구현

* Spring Boot 기반 REST API
* 사용자 인증과 회원 관리
* 의약품 검색 및 등록
* 복약 일정 생성과 관리
* JWT 기반 인증
* Google OAuth 로그인
* MySQL 데이터베이스 스키마 설계
* 프론트엔드 협업을 위한 API 명세 및 Mock 응답 공유

#### Tech

`Java 21` `Spring Boot` `MySQL` `JWT` `OAuth`
`React Native` `TypeScript`

---

### 04. DataAnalysis Pro

> 외부 API 데이터를 수집하고 정규화해 분석하는 스냅샷 기반 ETL 프로젝트

🔗 [Repository](https://github.com/soyeon911/DataAnalysis_pro)

#### 주요 구현

* 네이버 쇼핑 API 데이터 수집
* 수집 결과 MySQL 적재
* 상품 데이터와 판매처 데이터 분리
* 도메인과 판매처 이름 기반 데이터 정규화
* 배치 스냅샷별 가격과 판매처 변화 비교
* 키워드별 시장 상태 분석
* TOFU·MOFU·BOFU·SATURATED 단계 분류
* 분석 결과 CSV 및 시각화 데이터 출력

#### Tech

`Python` `MySQL` `SQL` `ETL` `Naver API` `matplotlib`

---

## Other Projects

### DearMap

장소, 사진, 날짜, 메모를 지도 위에 저장하는 모바일 애플리케이션

* React Native 및 Expo 기반 앱 개발
* 네이버 지도 연동
* 장소 검색과 마커 관리
* 이미지 및 추억 데이터 저장

🔗 [Repository](https://github.com/soyeon911/datemap)

---

### Tulink

전공 수업 기반 튜터링 매칭 웹 서비스

* 튜터·튜티 매칭
* 수업 예약과 중복 예약 방지
* 크레딧 관리
* QR 기반 수업 확인
* Django 기반 웹 서비스 구현

🔗 [Repository](https://github.com/soyeon911/Web_project)

---

### Window Clock

시계, 알람, 뽀모도로, 통계 기능을 제공하는 Windows 데스크톱 애플리케이션

* MFC 기반 UI 구현
* DLL 모듈 분리
* 알람 및 타이머 기능
* 사용자 활동 통계 제공

🔗 [Repository](https://github.com/soyeon911/WindowClock)

---

## Tech Stack

### Languages

`Python` `Java` `C#` `C++` `JavaScript` `TypeScript` `SQL`

### Backend

`Spring Boot` `FastAPI` `Django` `.NET` `REST API`

### Database

`MySQL` `SQLAlchemy`

### Test

`pytest` `Hypothesis` `xUnit` `JUnit` `GTest` `Catch2`

### CI/CD & Infrastructure

`Jenkins` `GitHub Actions` `Docker` `Allure`

### Quality Tools

`OpenAPI` `Swagger` `ruff` `mypy` `coverage`

---

## How I Work

```text
01. 요구사항을 검증 가능한 조건으로 구체화합니다.

02. 정상 흐름뿐 아니라 실패 흐름과 경계 조건을 함께 설계합니다.

03. 응답 코드만 확인하지 않고 실제 데이터와 상태 변화를 검증합니다.

04. 반복되는 검증은 자동화하고 실행 결과를 추적 가능하게 만듭니다.

05. 문제를 발견하는 데서 끝내지 않고 원인과 재현 조건을 정리합니다.

06. 테스트 결과를 코드와 시스템 구조의 개선으로 연결합니다.
```

---

## Current Interests

현재 다음 주제를 중심으로 학습과 프로젝트를 확장하고 있습니다.

* Transaction과 데이터 정합성
* 동시성 제어와 중복 요청 방지
* Idempotency
* Property-based Testing
* Stateful Testing
* Logs·Metrics·Traces
* Fault Injection
* API Security
* Reliability Engineering
* Quality Platform Engineering

---

## Next Project

### FaultLab

예약·결제 시스템을 기반으로 다양한 실패 조건을 재현하고 검증하는 프로젝트를 준비하고 있습니다.

#### 검증 대상

* 동일 예약의 동시 요청
* 결제 중복 처리
* 외부 결제 API Timeout
* 처리 도중 서버 종료
* 부분 성공으로 인한 데이터 불일치
* 권한이 없는 사용자의 리소스 접근
* Retry 증가로 인한 요청 증폭
* DB와 Cache 장애
* 장애 이후 상태 복구

#### 적용 예정 기술

`Spring Boot` `PostgreSQL` `Redis` `Docker Compose`
`pytest` `Hypothesis` `Schemathesis` `k6` `Toxiproxy`
`OpenTelemetry` `Prometheus` `Grafana`

---

<div align="center">

## Contact

**Email**
[sypark911@naver.com](mailto:sypark911@naver.com)

**GitHub**
[github.com/soyeon911](https://github.com/soyeon911)

**Velog**
[velog.io/@soyeon911](https://velog.io/@soyeon911/posts)

</div>
