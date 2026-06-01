<div align="center">

# 👋 안녕하세요, 박소연입니다

### 만드는 것에서 멈추지 않고, **검증하고 운영**까지 하는 개발자

데이터 파이프라인 · 백엔드 API · 장비 제어 · 테스트 자동화 —
"동작하는 시스템 전체"를 직접 설계하고 끝까지 책임지는 것을 좋아합니다.

[![GitHub](https://img.shields.io/badge/GitHub-soyeon911-211F1A?style=flat-square&logo=github)](https://github.com/soyeon911)

</div>

---

## 🙋‍♀️ About Me

- 🎯 팀에서는 주로 **PM과 백엔드**를 맡아 일정·구조·협업을 조율합니다.
- 🧪 **Suprema SWE 인턴십**(2026.03–05)에서 API 테스트 자동화 시스템을 처음부터 직접 설계·구현·운영하고 사내 세미나에서 발표했습니다.
- 🌱 도메인을 가리지 않고 데이터 분석, 웹·앱 서비스, 데스크톱, 장비 제어까지 다양하게 경험했습니다.
- 💡 좋은 코드는 결국 **다음 사람이 신뢰할 수 있는 코드**라고 믿어, 테스트·문서화·로깅·상태 관리에 진심입니다.

> _"문제를 끝까지 따라가서, 재현 가능하고 신뢰할 수 있는 결과로 만드는 사람"_

---

## 🛠️ Tech Stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=csharp&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

**Frameworks**

![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)
![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=black)
![.NET](https://img.shields.io/badge/.NET-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![MFC](https://img.shields.io/badge/MFC-00599C?style=flat-square&logo=cplusplus&logoColor=white)

**Data & Infra**

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)

**Test & Quality**

![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
![xUnit](https://img.shields.io/badge/xUnit-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=flat-square&logo=swagger&logoColor=black)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)

| 분야 | 사용 기술 |
|------|-----------|
| 사용 언어 | Python · Java · C# · C++ · JavaScript/TypeScript · SQL |
| 프레임워크 | Spring Boot 3.x · Django · React Native(Expo) · .NET 10 · MFC |
| 데이터/인프라 | MySQL · SQLite · Docker · GitHub Actions · JWT/OAuth |
| 테스트/품질 | pytest · xUnit · GoogleTest · Swagger/OpenAPI · Valgrind · ASan |
| 기타 | Git · Serilog · Bruno/Postman · matplotlib · AI Agent 활용 |

---

## 💼 Experience

### Suprema Inc. — Software Quality Engineer Intern
`2026.03 – 2026.05` · SWE팀

생체 인식 도메인(FAR/FRR/EER)과 제품 라인업(SDK→Module→Server→Plugin)을 학습한 뒤,
**Q-Face Engine API Server를 위한 테스트 자동화 시스템**을 처음부터 직접 설계·구현·운영했습니다.

- Swagger 명세 분석 → **Rule-Based 테스트 케이스 자동 생성** (Parser → Enricher → Generator → Runner → Reporter)
- GitHub Actions로 **CI 파이프라인** 구성, Swagger 변경 감지 시에만 테스트 실행하도록 최적화
- 요청 후 `/health` 확인으로 **크래시 탐지 레이어** 추가, 결과를 원인별로 분류
- 테스트를 통해 **Swagger 명세 오류 5건** 역으로 발견 → 명세 수정 제안
- 전 과정을 사내 세미나에서 발표


---

## 🚀 Projects

### 🧮 [DataAnalysis_pro](https://github.com/soyeon911/DataAnalysis_pro) · `개인`
**네이버 쇼핑 키워드 스냅샷 분석 파이프라인**
네이버 쇼핑 API로 상품 데이터를 수집해 MySQL에 적재하고, SQL 분석 + 퍼널 스코어링으로 타겟팅 인사이트를 도출.
- 수집 출처(API)와 실제 판매처(몰)를 분리, **스냅샷(batch) 단위**로 추세 비교
- 몰명 표기 불일치 **정규화 ETL**, 키워드 **TOFU/MOFU/BOFU/SATURATED** 퍼널 스코어링
- `Python` `MySQL` `SQL` `matplotlib` `Naver API`
- **역할:** 기획 · 수집 · ETL · 분석 전 과정 직접 구현

### 💊 [Time-to-Pill](https://github.com/soyeon911/Time-to-Pill) · `팀` · `PM` · `Backend`
**복약 관리 모바일 애플리케이션**
약 검색·등록, 복약 스케줄/알림/통계를 관리하는 앱. React Native + Spring Boot 구성.
- **Spring Boot 3.x · Java 21** 기반 REST API (Auth · Pill · Schedule · Search)
- JWT 인증 + Google OAuth, 약품·병용금기(DUR) 정보 연동, MySQL 스키마/마이그레이션 설계
- `Spring Boot` `Java 21` `React Native` `TypeScript` `MySQL` `JWT/OAuth`
- **역할:** PM & Backend 전담 (API·DB·인증 설계 및 일정 관리)

### ⚙️ [MiniEqController](https://github.com/soyeon911/MiniEqController) · `개인`
**상태머신 기반 경량 장비 컨트롤러**
장비 제어를 모사한 .NET 컨트롤러. 상태머신·인터락·타임아웃/재시도 등 신뢰성 로직을 HTTP API로 제어.
- 상태머신 `Idle→Init→Ready→Run→Error→Recover`, 인터락(Door/Vacuum) 위반 처리
- **STOP 즉시 취소 + 큐 드레인**, 우선순위 큐, 최신 명령만 실행하는 Coalescing
- Serilog 로깅 · 메트릭 · 헬스체크 · **Docker & xUnit 테스트**
- `C#` `.NET 10` `Minimal API` `xUnit` `Serilog` `Docker`
- **역할:** 설계 · 구현 · 테스트 · 컨테이너화 전 과정

### ⏱️ [WindowClock](https://github.com/soyeon911/WindowClock) · `팀` · `PM` · `기능 구현`
**윈도우 데스크톱 시계·뽀모도로 앱**
MFC 기반 데스크톱 앱. 시계·알람·뽀모도로·통계를 DLL로 모듈화.
- 기능별 **DLL 모듈화**(Clock · Pomodoro · Alarm)로 협업 구조 설계
- **뽀모도로 타이머** 구현 — 집중/휴식 사이클, 원형 시계 렌더링, 타이머 텍스트 갱신
- `C++` `MFC` `Win32 API` `DLL`
- **역할:** PM & 뽀모도로 기능 구현

### 🔗 [Web_project (Tulink)](https://github.com/soyeon911/Web_project) · `팀` · `PM` · `Frontend` · `Backend`
**대학생 전공 튜터링 매칭 웹 서비스**
Django 기반 웹 서비스. 단과대·전공·시간대로 튜터와 학생을 매칭하고 예약·크레딧·QR까지 연결.
- 다단계 회원가입, 전공/단과대 기반 **튜터 매칭** 및 예약 플로우
- **Link 크레딧** 시스템(잔액·결제·이용 횟수), 마이페이지 설계
- `Django` `Python` `SQLite` `HTML/CSS/JS`
- **역할:** PM · Frontend · Backend 보조 (1인 다역)

---

<div align="center">

### 📫 Contact

설계부터 운영까지, 끝까지 책임지는 개발자를 찾으신다면 편하게 연락 주세요.

[![GitHub](https://img.shields.io/badge/GitHub-@soyeon911-211F1A?style=for-the-badge&logo=github)](https://github.com/soyeon911)

</div>
