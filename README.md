<p align="center">
  <img width="720" src="https://github.com/user-attachments/assets/afeec5d8-44cf-43a1-8afa-59db78741844" />
</p>

<h1 align="center">🩸 산재콕 (SanJaeCok)</h1>
<p align="center">산업재해 데이터 기반 맞춤형 위험도 분석 및 예방 서비스</p>


## 📌 Introduction

산업재해 관련 정보는 여러 기관에 분산되어 있어 접근성이 낮고,  
산재 지정 의료기관 또한 제한적이어서 정보 탐색에 어려움이 있습니다.  

이에 따라 본 프로젝트는 **산재 정보, 통계, 예방 자료를 통합 제공하고**,  
사용자 맞춤형 위험도 분석을 통해 산업재해 예방을 지원하는 서비스를 목표로 개발되었습니다.

---

## 📊 Project Overview

- **프로젝트명**: 산재콕 (SanJaeCok)  
- **개발기간**: 2024.11.18 ~ 2024.12.24  
- **팀명**: 하랑 유니버스
- **개발 형태**: 4인 팀 프로젝트

### 목표
- 🔍 **산업재해 정보 통합화**: 공공데이터 기반 산재통계 및 뉴스 자동 수집
- 🗺️ **지역기반 서비스**: GPS를 활용한 근처 산재지정병원 검색
- 📊 **맞춤형 분석**: 사용자의 업종, 연령대별 산재 위험도 분석
- 🛡️ **안전교육 제공**: KOSHA 안전자료 자동 수집 및 큐레이션

### 해결하는 문제
- ❌ 산재 발생 시 대처할 수 있는 병원 정보 부족
- ❌ 개인 업종에 맞는 산재통계 정보 미흡
- ❌ 안전교육 자료에 대한 접근성 낮음
- ❌ 실시간 산재 관련 뉴스 수집의 어려움


## 🛠 Tech Stack

### Frontend
- ![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
- ![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
- ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
- ![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=flat-square&logo=bootstrap&logoColor=white)
- ![jQuery](https://img.shields.io/badge/jQuery-0769AD?style=flat-square&logo=jquery&logoColor=white)
- ![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat-square&logo=chartdotjs&logoColor=white)

---

### Backend
- ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
- ![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)
- ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)

---

### Database
- ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

---

### Infra & Tools
- ![AWS](https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
- ![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)
- ![VSCode](https://img.shields.io/badge/VSCode-007ACC?style=flat-square&logo=visualstudiocode&logoColor=white)
- ![Scheduler](https://img.shields.io/badge/Scheduler-Cron-blue?style=flat-square)

---

## 📊 Data Sources

### Public API
- ![KOSIS](https://img.shields.io/badge/KOSIS-산업재해현황-blue?style=flat-square)
- ![SafetyMap](https://img.shields.io/badge/생활안전지도-API-green?style=flat-square)

---

### Crawling Data
- ![근로복지공단](https://img.shields.io/badge/근로복지공단-산재지정의료기관-orange?style=flat-square)
- ![산재뉴스](https://img.shields.io/badge/산재뉴스-크롤링-red?style=flat-square)
- ![산업안전포털](https://img.shields.io/badge/산업안전포털-데이터-purple?style=flat-square)
> 산업재해 정보를 실시간으로 수집·분석하여 근로자에게 **맞춤형 안전정보**와 **지역별 산재지정병원**을 추천하는 플랫폼

---


## ⚡ 주요 기능

### 1️⃣ **병원 검색 시스템** 🏥
```
• 산재지정병원 검색 (주소, 병원명 기반)
• 지도 기반 근처 병원 검색 (Haversine 거리 계산)
• 병원 상세정보 조회 (전문분야, 연락처)
• 실시간 지오코딩 (카카오 API)
• 병원별 리뷰/평점 조회
```

### 2️⃣ **회원 관리 시스템** 👤
```
• 로컬 회원가입 (2단계 인증)
• 소셜 로그인 (카카오, 네이버, 구글 OAuth2)
• 개인 산재 기록 관리
• 마이페이지 (프로필 수정, 비밀번호 변경)
• 개인별 산재 위치 저장 (GPS 좌표)
```

### 3️⃣ **통계 분석 대시보드** 📊
```
• 개인 업종별 산재통계 (통계청 공식 데이터)
• 연령대별, 성별 산재 분석
• 7일 신규가입 추이 차트
• 위험도 평가 및 안전정보 제공
```

### 4️⃣ **자동 크롤링 시스템** 🤖
```
• 산재지정병원 정보 수집 (SAFEMAP API)
• 뉴스 자동 수집 (sanjaenews.co.kr) - 매일 09:00, 21:00
• 안전교육 자료 수집 (KOSHA) - 매일 03:30
• 관리자 수동 트리거 기능
```

### 5️⃣ **안전자료실** 📚
```
• KOSHA 안전교육 자료 제공
• 자료 유형별 분류 (PPT, 동영상, 책자, OPS)
• 다국어 지원 (한, 영, 중 등)
• 조회수 추적 및 최근 방문 기록
```

### 6️⃣ **관리자 대시보드** ⚙️
```
• 전체 회원, 산재, 리뷰 통계
• 신규 가입자 추이 모니터링
• 크롤러 수동 실행 관리
• 회원/산재/리뷰/통계 페이지 관리
```

---


---

## 🚀 설치 및 실행

### 사전 요구사항
```bash
• Python 3.10 이상
• pip 또는 conda
• Git
```

### 1단계: 저장소 클론
```bash
git clone https://github.com/imyongchan/Industry_accident-Project.git
cd Sanjae_Project
```

### 2단계: 가상환경 생성 및 활성화
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

### 3단계: 의존성 설치
```bash
pip install -r requirements.txt
```

### 4단계: 데이터베이스 마이그레이션
```bash
cd sanjekok
python manage.py migrate
```

### 5단계: 관리자 계정 생성
```bash
python manage.py createsuperuser
```

### 6단계: 서버 실행
```bash
python manage.py runserver
```

### 7단계: 브라우저에서 접속
```
http://localhost:8000
관리자: http://localhost:8000/admin
```

---

## 📌 주요 기술 상세


### 📊 통계 분석
- **통계청 KOSIS API** 연동으로 공식 데이터 기반 분석
- 개인 업종별 산재통계 비교
- 연령대별/성별 데이터 시각화



---

## 💡 프로젝트 하이라이트

### ✨ 혁신적 기능
- 🤖 **완전 자동화된 데이터 수집**: 매일 정해진 시간에 최신 정보 자동 업데이트
- 🗺️ **GPS 기반 스마트 검색**: 사용자 위치에서 가장 가까운 병원 즉시 제시
- 👥 **다중 인증 시스템**: 로컬 + 3가지 소셜 로그인 지원
- 📈 **맞춤형 위험도 분석**: AI 기반 사용자 업종별 산재통계 분석

### 🏆 개발 역량 시연
- **풀스택 개발**: Backend(Django) + Frontend(Template) 통합 구현
- **외부 API 연동**: 6개 이상의 외부 API 안정적 통합
- **자동화 시스템**: 스케줄러를 통한 크롤링 자동화
- **데이터베이스 설계**: 정규화된 관계형 DB 모델링 (19개 이상의 테이블)
- **보안 구현**: 비밀번호 해싱, 세션 관리, OAuth2 인증

---

## 🔗 유용한 링크

- 📖 [Django 공식 문서](https://docs.djangoproject.com/)
- 🗺️ [네이버 지도 API 문서](https://developers.naver.com/docs/map/)
- 📊 [통계청 KOSIS API](https://kosis.kr/)
- 🏥 [보건복지부 SAFEMAP](https://safemap.go.kr/)
- 🛡️ [산업안전보건공단](https://www.kosha.or.kr/)

---


---

## 📄 라이센스

이 프로젝트는 MIT 라이센스 하에 배포됩니다.

---

