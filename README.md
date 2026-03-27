# 🏥 산재 데이터 분석 및 추천 정보제공 플랫폼
### 근로자 안전을 위한 산업재해 통합 정보 플랫폼

![Python](https://img.shields.io/badge/Python-3.10+-3776ab?style=flat-square&logo=python)
![Django](https://img.shields.io/badge/Django-5.2-092e20?style=flat-square&logo=django)
![SQLite](https://img.shields.io/badge/SQLite-Database-003B57?style=flat-square&logo=sqlite)
![Status](https://img.shields.io/badge/Status-Active-success?style=flat-square)

> 산업재해 정보를 실시간으로 수집·분석하여 근로자에게 **맞춤형 안전정보**와 **지역별 산재지정병원**을 추천하는 플랫폼

---

## 📑 목차

- [프로젝트 개요](#프로젝트-개요)
- [주요 기능](#주요-기능)
- [기술 스택](#기술-스택)
- [시스템 아키텍처](#시스템-아키텍처)
- [설치 및 실행](#설치-및-실행)
- [프로젝트 구조](#프로젝트-구조)
- [주요 기술 상세](#주요-기술-상세)
- [팀 정보](#팀-정보)

---

## 🎯 프로젝트 개요

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

## 🛠️ 기술 스택

### Backend
| 분류 | 기술 |
|------|------|
| **Framework** | Django 5.2 |
| **Language** | Python 3.10+ |
| **Database** | SQLite (개발용) |
| **Task Scheduler** | APScheduler |
| **Authentication** | Django Auth + OAuth2 |

### Frontend
| 분류 | 기술 |
|------|------|
| **Template** | Django Template |
| **Map API** | 네이버 지도 API |
| **Styling** | CSS3 |
| **Interactive** | JavaScript / AJAX |

### External APIs
| 서비스 | 목적 | 제공자 |
|--------|------|--------|
| **지오코딩** | 주소→좌표 변환 | 카카오 |
| **지도** | 병원/산재지점 표시 | 네이버 |
| **산재통계** | 공식 산재 통계 | 통계청 (KOSIS) |
| **병원 데이터** | 산재지정병원 정보 | 보건복지부 (SAFEMAP) |
| **안전자료** | 안전교육 자료 | 산업안전보건공단 |
| **소셜로그인** | 회원 인증 | 카카오, 네이버, 구글 |

---

## 🏗️ 시스템 아키텍처

```
┌─────────────────────────────────────────────────────┐
│                   Frontend (Template)                │
│          병원검색 | 통계 | 뉴스 | 마이페이지         │
└────────────────────┬────────────────────────────────┘
                     │
┌────────────────────▼────────────────────────────────┐
│              Django URL Router                        │
│  /hospital | /member | /stats | /news | /safe       │
└────────────────────┬────────────────────────────────┘
                     │
┌────────────────────▼────────────────────────────────┐
│            Django App Layer (Views/Services)         │
│                                                       │
│  ├─ hospital     (병원 검색, 지오코딩)               │
│  ├─ member       (회원, 소셜로그인)                 │
│  ├─ news         (뉴스 관리)                         │
│  ├─ safe         (안전자료)                          │
│  ├─ stats        (통계 분석)                         │
│  ├─ manager      (관리자 대시보드)                   │
│  └─ reviews      (리뷰 시스템)                       │
└────────────────────┬────────────────────────────────┘
                     │
┌────────────────────▼────────────────────────────────┐
│             Data & Business Logic                    │
│                                                       │
│  ├─ Models        (Member, Hospital, News, ...)     │
│  ├─ Services      (소셜로그인, 통계계산, ...)        │
│  ├─ Crawlers      (뉴스, 병원, 안전자료)            │
│  └─ Signals       (신호 처리)                        │
└────────────────────┬────────────────────────────────┘
                     │
┌────────────────────▼────────────────────────────────┐
│             SQLite Database                          │
│  t_member | t_hospital | t_news | t_safe | ...      │
└─────────────────────────────────────────────────────┘
                     │
         ┌───────────┼───────────┐
         │           │           │
    ┌────▼────┐  ┌──▼────┐  ┌──▼─────┐
    │ 카카오   │  │네이버 │  │통계청   │
    │지오코딩  │  │지도   │  │KOSIS   │
    └─────────┘  └───────┘  └────────┘
```

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

## 📁 프로젝트 구조

```
Sanjae_Project/
├── README.md                      # 프로젝트 설명서
├── manage.py                      # Django 관리 스크립트
├── db.sqlite3                     # 데이터베이스
├── data.json                      # 초기 데이터
│
├── sanjekok/                      # 메인 프로젝트 폴더
│   ├── __init__.py
│   ├── settings.py               # 프로젝트 설정
│   ├── urls.py                   # 메인 URL 라우터
│   ├── wsgi.py                   # WSGI 설정
│   ├── asgi.py                   # ASGI 설정
│   └── scheduler.py              # APScheduler 설정
│
├── main/                          # 메인 페이지 앱
│   ├── views.py                  # 통계API, 홈페이지
│   ├── models.py
│   ├── urls.py
│   └── templates/
│       ├── base.html             # 기본 템플릿
│       ├── main.html             # 메인 페이지
│       ├── intro_service.html    # 서비스 소개
│       └── intro_tech.html       # 기술 소개
│
├── hospital/                      # 병원 검색 앱
│   ├── views.py                  # 병원 검색, 상세정보
│   ├── models.py                 # Hospital 모델
│   ├── urls.py
│   ├── crawler/                  # 병원 정보 크롤러
│   │   ├── fetch.py             # SAFEMAP API 호출
│   │   ├── parse.py             # 데이터 파싱
│   │   ├── save.py              # DB 저장
│   │   └── run.py               # 크롤러 메인
│   └── templates/
│       └── hospital/
│
├── member/                        # 회원 관리 앱
│   ├── views.py                  # 회원가입, 로그인, 마이페이지
│   ├── models.py                 # Member, Individual 모델
│   ├── services.py               # 소셜로그인 처리
│   ├── signals.py                # 회원가입 신호
│   ├── decorators.py             # 로그인 체크
│   ├── forms.py                  # 회원가입 폼
│   ├── urls.py
│   ├── migrations/
│   └── templates/
│       └── member/
│
├── news/                          # 뉴스 앱
│   ├── views.py                  # 뉴스 조회/검색
│   ├── models.py                 # News 모델
│   ├── urls.py
│   ├── crawler/                  # 뉴스 자동 크롤러
│   │   ├── fetch.py             # sanjaenews.co.kr 크롤링
│   │   ├── parse.py
│   │   └── save.py
│   └── migrations/
│
├── safe/                          # 안전자료 앱 (자료실)
│   ├── views.py                  # 자료 조회/검색
│   ├── models.py                 # Safe, Tag, SafeTag, History
│   ├── urls.py
│   ├── crawler/                  # KOSHA 자료 크롤러
│   │   ├── fetch.py             # KOSHA API 크롤링
│   │   ├── parse.py
│   │   └── save.py
│   └── migrations/
│
├── stats/                         # 통계 분석 앱
│   ├── views.py                  # 개인 통계 대시보드
│   ├── models.py                 # Stats1~9 모델
│   ├── stats.py                  # 통계 계산 로직
│   ├── urls.py
│   └── migrations/
│
├── manager/                       # 관리자 대시보드 앱
│   ├── views.py                  # 관리자 대시보드, 관리
│   ├── models.py
│   ├── urls.py
│   └── templates/
│       ├── manager_base.html
│       ├── manager_dash.html    # 대시보드
│       ├── manager_member.html  # 회원 관리
│       ├── manager_detail.html
│       ├── manager_review.html  # 리뷰 관리
│       ├── manager_stats.html   # 통계
│       └── manager_login.html   # 관리자 로그인
│
├── reviews/                       # 리뷰 시스템 앱
│   ├── views.py                  # 리뷰 생성/조회
│   ├── models.py                 # Review 모델
│   └── urls.py
│
├── search/                        # 위치 기반 검색 앱
│   ├── views.py                  # 주소기반 검색 API
│   ├── models.py
│   └── urls.py
│
├── static/                        # 정적 파일
│   ├── CSS/
│   ├── img/
│   └── js/
│
└── templates/                     # 공유 템플릿
    └── common/
```

---

## 📌 주요 기술 상세

### 🗺️ 지도 기반 검색 (Haversine 공식)
```python
# 두 지점 간 거리 계산
from math import radians, sin, cos, sqrt, atan2

def haversine_distance(lat1, lon1, lat2, lon2):
    R = 6371  # 지구 반경 (km)
    
    lat1, lon1, lat2, lon2 = map(radians, [lat1, lon1, lat2, lon2])
    dlat = lat2 - lat1
    dlon = lon2 - lon1
    
    a = sin(dlat/2)**2 + cos(lat1)*cos(lat2)*sin(dlon/2)**2
    c = 2*atan2(sqrt(a), sqrt(1-a))
    
    return R * c  # km 단위
```

### 🔐 소셜 로그인 (OAuth2)
```
사용자 → 리다이렉션 → OAuth 제공자 → 토큰 발급 → 회원 생성/업데이트 → 로그인
```

### 🤖 자동 크롤링 (APScheduler)
```python
from apscheduler.schedulers.background import BackgroundScheduler

scheduler = BackgroundScheduler()
scheduler.add_job(fetch_news, 'cron', hour='9,21')  # 매일 09:00, 21:00
scheduler.start()
```

### 📊 통계 분석
- **통계청 KOSIS API** 연동으로 공식 데이터 기반 분석
- 개인 업종별 산재통계 비교
- 연령대별/성별 데이터 시각화

### 🔍 지오코딩
- **카카오 Geolocation API** 활용
- 주소 → 위도/경도 변환
- 역지오코딩으로 좌표 → 주소 변환

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

## 👥 팀 정보

**프로젝트명**: 산재 데이터 분석 및 추천 정보제공 플랫폼  
**개발팀**: 하랑 유니버스  
**개발 기간**: 2024 ~ 2025  
**버전**: 1.0.0

---

## 📄 라이센스

이 프로젝트는 MIT 라이센스 하에 배포됩니다.

---

<div align="center">
  
  **Made with ❤️ by 산재 데이터팀**
  
  [⬆ Back to top](#-산재-데이터-분석-및-추천-정보제공-플랫폼)
  
</div>
