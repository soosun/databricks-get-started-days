# Databricks Get Started Days

Databricks를 처음 접하는 분들을 위한 4시간 입문 워크숍 자료입니다.

이 저장소는 Databricks Workspace 기본 사용법부터 Delta Lake, Data Engineering, Databricks SQL, AI/BI Dashboard, Genie까지 빠르게 경험할 수 있도록 구성된 핸즈온 노트북과 샘플 데이터를 포함합니다.

## 대상

- Databricks를 처음 사용해보는 데이터 엔지니어, 데이터 분석가, BI 사용자
- Lakehouse, Delta Lake, Unity Catalog, Databricks SQL의 기본 개념을 실습으로 익히고 싶은 분
- Databricks Free Edition 또는 Databricks Workspace에서 간단한 데이터 파이프라인과 대시보드를 만들어보고 싶은 분

## 학습 목표

워크숍을 마치면 다음을 수행할 수 있습니다.

- Databricks Workspace, Notebook, Catalog Explorer, Compute의 기본 구조를 이해합니다.
- CSV 데이터를 Delta Table로 적재하고 조회합니다.
- Delta Lake의 INSERT, UPDATE, DELETE, Time Travel 등 핵심 기능을 실습합니다.
- Bronze, Silver, Gold로 이어지는 Medallion Architecture를 간단한 예제로 구현합니다.
- Databricks Job을 구성해 여러 노트북 태스크를 실행합니다.
- Databricks SQL로 데이터를 탐색하고 Assistant를 활용해 쿼리를 작성합니다.
- AI/BI Dashboard와 Genie Space를 만들어 비즈니스 사용자를 위한 분석 경험을 구성합니다.

## 저장소 구성

```text
.
├── Get Started with Databricks for Data Engineering/
│   ├── M1 - Databricks Overview/
│   │   └── 01 - Databricks Workspace Walkthrough.ipynb
│   └── M2 - Using Databricks for Data Engineering/
│       ├── 01-Creating and Working with a Delta Table.ipynb
│       ├── 02-Ingesting Data into Delta Lake.ipynb
│       ├── 03-Transforming Data Using the Medallion Architecture.ipynb
│       ├── 04-Creating a Simple Databricks Job.ipynb
│       ├── 04A-Task 1 - Setup - Bronze.ipynb
│       ├── 04B-Task 2 - Silver - Gold.ipynb
│       └── 05L - Ingest and Manipulate a Delta Table Lab.ipynb
├── Get Started with SQL Analytics and BI on Databricks/
│   ├── M01 - Databricks Overview/
│   │   └── 01 - Databricks Workspace Walkthrough.ipynb
│   ├── M02 - Using Databricks for Data Analytics/
│   │   ├── 01 - Writing Queries in Databricks.ipynb
│   │   ├── 02 - Using Databricks Assistant with Databricks SQL.ipynb
│   │   └── 03 - Using Delta Lake Features with Databricks SQL.ipynb
│   └── M03 - Databricks AI-BI/
│       ├── 01 - Creating a Dashboard in Databricks.ipynb
│       ├── 02 - Creating Genie Spaces.ipynb
│       └── 03 - Data Analytics Comprehensive Lab.ipynb
└── dataset/
    ├── customers.csv
    ├── employees.csv
    ├── employees2.csv
    ├── sales.csv
    └── sales_orders.csv
```

## 실습 준비

### 1. Databricks 환경

다음 중 하나의 환경이 필요합니다.

- Databricks Free Edition
- Databricks Workspace
- Serverless Compute 또는 실습용 Cluster
- Databricks SQL Warehouse

### 2. 자료 가져오기

이 저장소를 로컬에 클론하거나 ZIP으로 다운로드합니다.

```bash
git clone <repository-url>
```

Databricks Workspace에서 다음 방식 중 하나로 노트북을 가져옵니다.

- Workspace UI에서 `.ipynb` 파일 Import
- Databricks Repos 또는 Git Folder로 GitHub 저장소 연결
- 필요한 노트북만 선택해 개별 업로드

### 3. 샘플 데이터

`dataset/` 폴더의 CSV 파일은 실습용 샘플 데이터입니다. 각 노트북의 안내에 따라 Unity Catalog Volume 또는 Workspace 파일 영역에 업로드한 뒤 사용합니다.

## 트랙 안내

### Data Engineering

Data Engineering 트랙은 데이터 엔지니어링 입문자를 대상으로 Delta Lake와 Lakehouse 패턴을 실습합니다.

주요 주제:

- Delta Table 생성 및 관리
- CSV 데이터 적재
- CTAS, Upload UI, COPY INTO, Auto Loader
- Delta Lake DML과 Time Travel
- Bronze, Silver, Gold Medallion Architecture
- Databricks Job과 멀티 태스크 워크플로우

### SQL Analytics and BI

SQL Analytics/BI 트랙은 SQL 사용자와 비즈니스 분석가가 Databricks에서 데이터를 탐색하고 시각화하는 흐름을 다룹니다.

주요 주제:

- Databricks SQL 쿼리 작성
- Databricks Assistant를 활용한 SQL 작성 및 디버깅
- Delta Lake 기능을 SQL로 실습
- AI/BI Dashboard 생성
- Genie Space 생성
- 종합 대시보드 Lab

## 참고

이 자료는 Databricks 입문 워크숍을 위한 교육용 자료입니다. 실제 운영 환경에 적용할 때는 조직의 Unity Catalog 권한 모델, 네트워크 정책, 데이터 거버넌스 기준에 맞게 조정하세요.