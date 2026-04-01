<p align="center">
  <img width="800" height="300" alt="image" src="https://github.com/user-attachments/assets/648d61ed-feaa-430a-8738-55e91fca237b" />
</p>

<h1 align="center">⛑ 산재콕 (SanJaeCok)</h1>
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
- 🗺️ **위치기반 정보 검색**: 사용자 집,근무지,사고지역 기준 산재지정병원 검색
- 📊 **맞춤형 분석**: 사용자의 업종, 연령대별 산재 위험도 분석
- 🛡️ **안전교육 제공**: 안전자료 자동 수집 및 큐레이션

### 해결하는 문제
- ❌ 산재 발생 시 대처할 수 있는 병원 정보 부족
- ❌ 개인 업종에 맞는 산재통계 정보 미흡
- ❌ 안전교육 자료에 대한 접근성 낮음
- ❌ 실시간 산재 관련 뉴스 수집의 어려움
---
## 👥 팀 구성 및 역할 
- **김용찬(팀장)** : 회원맞춤 산업재해 통계 시각화
- **최도윤** : 멤버기능, 소셜로그인, 서버배포
- **박소윤** : 산업재해 뉴스, 안전자료실  
- **이하랑** : 메인페이지, 관리자페이지
- **문승신** : 산업재해 위치, 산재지정병원 검색 


## 🛠 Tech Stack

<div align="center">

### 💻 Frontend
<img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white"/>
<img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white"/>
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"/>
<img src="https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white"/>
<img src="https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white"/>
<img src="https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chartdotjs&logoColor=white"/>


### 🧠 Backend
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white"/>
<img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white"/>


### 🗄 Database
<img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white"/>


### ☁️ Infra & Tools
<img src="https://img.shields.io/badge/AWS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white"/>
<img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/>
<img src="https://img.shields.io/badge/VSCode-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white"/>
<img src="https://img.shields.io/badge/Cron-Scheduler-blue?style=for-the-badge"/>

</div>

## 🔍 Data Sources

<div align="center">

### 📡 Open API
<img src="https://img.shields.io/badge/KOSIS-산업재해현황-005BAC?style=for-the-badge"/>
<img src="https://img.shields.io/badge/생활안전지도-API-2ECC71?style=for-the-badge"/>


### 🕷 Crawling Data
<img src="https://img.shields.io/badge/근로복지공단-산재지정의료기관-FF7F50?style=for-the-badge"/>
<img src="https://img.shields.io/badge/산재뉴스-크롤링-E74C3C?style=for-the-badge"/>
<img src="https://img.shields.io/badge/산업안전포털-안전자료-8E44AD?style=for-the-badge"/>

</div>

## ⚡ 주요 기능

---

### 1️⃣ 🏥 산재& 병원 검색 시스템

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/12802a5f-6bf9-4cd8-96e8-225b0d94918e" width="400"/>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/4f9047ab-d6b4-4b2f-b9f6-76b6b956a5ce" width="400"/>
    </td>
  </tr>
</table>


- 산재지정병원 검색 (주소, 병원명 기반)  
- 지도 기반 근처 병원 검색 (Haversine 거리 계산)  
- 병원 상세정보 조회 (전문분야, 연락처)  
- 카카오 API 기반 실시간 지오코딩  
- 병원 리뷰 및 평점 시스템 제공  

---

### 2️⃣ 👤 회원 관리 시스템

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/4a383e31-0403-44e9-b817-590f16c6ddb3" width="400"/>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/7b7c6005-89ce-475c-85c0-c47caefabd08" width="400"/>
    </td>
  </tr>
</table>

- 로컬 회원가입 및 2단계 인증  
- 카카오 / 네이버 / 구글 OAuth2 소셜 로그인  
- 개인 산재 기록 관리 기능  
- 마이페이지 (프로필 수정, 비밀번호 변경)  
- 사용자 산재 위치 GPS 저장  

---

### 3️⃣ 📊 통계 분석 대시보드

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/d06d95da-12b1-4ed8-828f-702694ec5b6b" width="400"/>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/65a8f407-26bf-45e5-a87a-612bca161ed2" width="400"/>
    </td>
  </tr>
</table>

- 개인 업종별 산업재해 통계 제공  
- 연령대 및 성별 기반 분석  
- Chart.js 기반 시각화  
- 위험도 평가 및 안전정보 제공  

---

### 5️⃣ 📚 뉴스 & 안전자료실

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/a1265a75-b678-48bb-bea8-0c892b834d56" width="400"/>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/ed8daf2e-1613-4392-bd47-d67e5280d696" width="400"/>
    </td>
  </tr>
</table>


- 산업안전 교육자료 제공  
- 자료 유형별 분류 (영상, PPT, 문서 등)  
- 다국어 콘텐츠 지원  
- 조회수 및 최근 기록 관리  

---

### 6️⃣ ⚙️ 관리자 대시보드

<table>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/aad4a48b-3a5a-49bd-b5e0-64e1bd7cc8be" width="400"/>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/2868de8b-9a92-4690-95bd-851254c814b8"  width="400"/>
    </td>
  </tr>
</table>

- 전체 회원 및 데이터 통계   
- 신규 가입자 추이 모니터링  
- 사용자 및 산재정보 데이터 관리 기능
- 병원 리뷰 데이터 관리 

---

# 💥Troubleshooting -- 산업재해 통계 시각화
## 1️⃣ Pandas Pivot Table 집계 시 분류불능 데이터 포함

### 📌 문제
연령대별 통계 계산 시  '분류불능' 항목-> 불필요한 범주, 연령대 범주 너무 세부화 되어있음.
```
연령대 통계: [18~24세미만: 120, 25~29세: 450,... 분류불능: 35]  # ❌ 
```

### 🔍 원인
- **DB 데이터 품질**: 통계청 공식 데이터에 '분류불능' 항목 존재
- **연령대별 그룹화 필요** 

### 💡 해결 방법

#### Before (오류 코드)
```python
# stats.py - get_stats4() 함수
pivot = (
    df.pivot_table(
        index="prd_de",
        columns="c2_nm",
        values="dt",
        aggfunc="sum",
    )
    .sort_index()
)  # ❌ 분류불능 항목 포함

```

#### After (해결 코드)
```python
# stats.py - get_stats4() 함수
pivot = (
    df.pivot_table(
        index="prd_de",
        columns="c2_nm",
        values="dt",
        aggfunc="sum",
    )
    .sort_index()
)

# ✅ 데이터 정규화: 분류불능 항목 제거
pivot = pivot.drop(columns=["분류불능"], errors="ignore")

age_pivot = pd.DataFrame(index=pivot.index)

# ✅ 명시적 연령대 그룹화
age_pivot["18세 미만"] = pivot.get("18세 미만", 0)
age_pivot["20대"] = pivot.get("18~24세", 0) + pivot.get("25~29세", 0)
                    .
                    .
age_pivot["60대 이상"] = pivot.get("60세 이상", 0)
```

### 📊 효과
<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/e19b3c3c-8b95-4a72-8fb6-931eca94fdc2" />

- ✅ 차트 가독성 향상

## 2️⃣ 차트 재렌더링 시 이전 데이터 누적 현상

### 📌 문제
사용자가 "최근 1년" → "2년" → "3년" 버튼을 차례대로 클릭할 때, Chart.js 인스턴스가 재사용되지 않아 성능 저하 및 메모리 누수

### 🔍 원인
- **메모리 누수**: 이전 Chart 인스턴스 destroy() 미실행
- **DOM 리소스**: canvas 요소가 중복 바인딩됨

### 💡 해결 방법

#### Before (오류 코드)
```javascript
// chart.js
function createHorizontalBarChart(chartRefName, canvasId, labels, data, options = {}) {
    const canvas = document.getElementById(canvasId);
    const ctx = canvas.getContext("2d");

    // ❌ 기존 차트 확인 없이 매번 새로 생성
    charts[chartRefName] = new Chart(ctx, {
        type: "bar",
        data: { labels, datasets: [{data, ...}] },
        ...
    });
}
```

#### After (해결 코드)
```javascript

    const ctx = canvas.getContext("2d");
    const existing = charts[chartRefName];

    // ✅ 기존 차트 재활용 (데이터만 업데이트)
    if (existing) {
        existing.data.labels = labels;
        existing.data.datasets[0].data = data;
        existing.data.datasets[0].backgroundColor = colors;
        existing.update();  // 차트 재렌더링
        return;  
    }

    // ✅ 첫 번째 호출 시에만 신규 생성
    charts[chartRefName] = new Chart(ctx, {
        type: "bar",
        data: { labels, datasets: [{data, backgroundColor: colors, ...}] },
        ...
    });
}
```

#### 📊 효과
- ✅ 차트 변환 응답속도: 1.5s → 150ms (약 10배 개선)
- ✅ 메모리 사용량: 안정적 유지 (누적 증가 제거)
- ✅ 사용자 경험 개선 (버튼 클릭 반응 즉시성)


## 3️⃣다중 통계함수의 쿼리 성능 (N+1 Problem)

### 📌 문제
사용자가 통계 페이지를 로드할 때마다 9개의 통계 함수(`get_stats1` ~ `get_stats9`)가 순차적으로 데이터베이스를 조회하여 응답 속도가 3~5초 지연:


### 🔍 원인
- **순차 쿼리**: 각 `get_stats*()` 함수에서 독립적으로 `filter()` → `values()` 실행
- **데이터 중복 조회**: 동일 업종의 Stats 테이블을 여러 번 쿼리
- **Pandas 변환 오버헤드**: 매번 `DataFrame.from_records()` 및 `pivot_table()` 실행

### 💡 해결 방법

#### Before (오류 코드)
```python
# views.py - 순차 쿼리
summary1 = get_stats1(industry_name1)
summary2 = get_stats2(industry_name2)
...
summary9 = get_stats9(industry_name9)
# ❌ 총 9회 DB 접근, ~4-5초 소요
```

#### After (해결 코드 - 캐싱 적용)
```python
# views.py - 캐싱 추가
from django.views.decorators.cache import cache_page
from django.core.cache import cache

def stats_home(request):
    
    # ✅ 캐시 키 생성
    cache_key = f"stats_{industry.id}_{age_group}"
    cached_data = cache.get(cache_key)
    
    if cached_data:
        # 캐시된 데이터 사용
        summary1, summary2, ..., summary9, risk_analysis = cached_data
    else:
        # 쿼리 실행 (처음 1회만)
        summary1 = get_stats1(industry_name1)
        summary2 = get_stats2(industry_name2)
        # ... 나머지 쿼리 ...
        
        # ✅ 24시간 동안 캐시 저장
        cache.set(cache_key, 
            (summary1, summary2, ..., summary9, risk_analysis), 
            86400  # 24시간
        )
```

### 📊 효과
- ✅ 페이지 로드 속도: 4-5배 개선
- ✅ DB 쿼리 횟수: 9회 → 1회 (캐싱 적용 시)


## 🎥 데모 영상

- 프로젝트 발표 영상 : [발표 영상](https://www.youtube.com/watch?v=e4Z1Nv8bzfg&list=PLedGoSru7948o9_CdQBQZmIc-K3tR8eO9&index=2)
- 프로젝트 화면 영상 : [화면 영상](https://www.youtube.com/watch?v=pW8r0M16QmE&list=PLedGoSru7948o9_CdQBQZmIc-K3tR8eO9&index=5)
---



