[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=DB7093&width=500&lines=Hi+There,+I'm+Soyeon+Park+🤩;)](https://git.io/typing-svg)


<p>
  📚 <b>Yonsei University Mirae Campus</b>, Dept. of Software (Mar 2022 - Feb 2026)<br>
  🧪 <b>Undergraduate Research Assistant</b> (Sep 2024 – Aug 2025)<br>
  💻 <b>Suprema Internship program (Mar 2026 - May 2026)</b>
</p>

<br>

## 🛠️ Tech Stack & Skills

**Languages**
<p style="display: flex; flex-wrap: wrap; gap: 8px;">
  <img alt="Python" src ="https://img.shields.io/badge/Python-3776AB.svg?style=for-the-badge&logo=Python&logoColor=white"/>
  <img alt="cplusplus" src="https://img.shields.io/badge/c++-%2300599C.svg?style=for-the-badge&logo=c%2B%2B&logoColor=white"/>
  <img alt="MySQL" src="https://img.shields.io/badge/MySQL-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white"/>
  <img alt="Pandas" src="https://img.shields.io/badge/pandas-150458.svg?style=for-the-badge&logo=pandas&logoColor=white"/>
  <img alt="Matplotlib" src="https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=pandas&logoColor=black"/>
  
</p>

**Mobile & Web Development**
<p style="display: flex; flex-wrap: wrap; gap: 8px;">
  <img alt="Flutter" src="https://img.shields.io/badge/Flutter-02569B.svg?style=for-the-badge&logo=Flutter&logoColor=white"/>
  <img alt="Spring Boot" src="https://img.shields.io/badge/Spring%20Boot-6DB33F.svg?style=for-the-badge&logo=Spring-Boot&logoColor=white"/>
  <img alt="React Native" src="https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB"/>
</p>

<br>

## 🚀 Key Projects for Data Analysis

### 1. Naver Shopping Market Insight Pipeline 🛍️
> **시장/브랜드 분석을 위한 데이터 파이프라인 구축 및 퍼널(Funnel) 스코어링 프로젝트**
> *Role: Data Engineering, SQL Analysis, Insight Reporting*

네이버 쇼핑 API를 활용하여 브랜드/트렌드 키워드 데이터를 수집하고, **SQL 기반 분석을 통해 리서치/제휴/타겟팅 인사이트**를 도출했습니다. 단순 수집을 넘어, 키워드를 퍼널(TOFU/MOFU/BOFU)로 구분하여 마케팅 집중 포인트를 제안하는 로직을 구현했습니다.

**Key Achievements:**
* **Automated Research**: 브랜드/카테고리/트렌드/IP 키워드 데이터 수집 자동화
* **Funnel Analysis**: 검색량과 상품 경쟁도를 기반으로 `Funnel Score`를 산출하여 잠재 시장 발굴
* **Market Intelligence**: 판매처(Mall) 데이터를 정규화하여 시장 내 주요 플레이어(Top Rank Winners) 식별

**Analysis Flow:**

```mermaid
flowchart LR
    A["Data Collection<br/>(Naver API)"] --> B["ETL & Normalize<br/>(Python/MySQL)"]

    B --> C["Funnel Scoring<br/>(SQL Analysis)"]

    C --> D["Targeting Insight<br/>(Visualization)"]
```



**Insights Example:**
* 특정 IP(캐릭터) 굿즈 시장의 점유율 상위 몰(Store) 분석을 통해 제휴 타겟 리스트 추출
* 키워드별 가격대(Min/Max/Avg) 분포 분석을 통한 포지셔닝 전략 제안

[👉 View Repository](https://github.com/soyeon911/dataanalysis_pro)

<br>

### 2. Time To Pill (Medication Management App) 💊
> **모바일 서비스 유저 데이터 구조 설계 및 서비스 구축**
> *Role: Full-Stack Dev (React Native, Spring Boot, MySQL)*

직접 모바일 서비스를 기획하고 구축하며, **서비스 내에서 유저 행동 데이터(User Action)와 로그가 어떻게 DB에 적재되는지** 경험했습니다.

**Data Perspective:**
* **Schema Design**: 유저(User) - 약(Pill) - 스케줄(Schedule) 간의 ERD를 설계하여, 유저의 복약 행동 데이터를 구조화
* **Tracking Points**: 회원가입, 검색, 복약 완료 등 주요 이벤트가 발생하는 시점과 데이터 흐름 파악

**Database Schema:**
```mermaid
erDiagram
    users ||--o{ user_pills : logs
    users ||--o{ schedules : actions
    pills ||--o{ user_pills : reference
    schedules {
        enum schedule_time
        boolean taken
        timestamp taken_at
    }
```

[👉 View Repository](https://github.com/wtaegyu/Time-to-Pill/tree/soyeon)

<br>

## 📊 GitHub Stats

<p>
  <img src="https://github-readme-stats.vercel.app/api?username=soyeon911&show_icons=true&theme=dracula" height="200px"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=soyeon911&langs_count=8&layout=compact" height="200px" style="margin-left: 10px;"/>
</p>

## 🧠 Problem Solving

<p>
  <a href="https://solved.ac/sypark911">
    <img src="http://mazassumnida.wtf/api/generate_badge?boj=sypark911" alt="solved.ac profile" />
  </a>
</p>
