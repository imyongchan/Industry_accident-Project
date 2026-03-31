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

## 💥Troubleshooting




## 🎥 데모 영상

- 프로젝트 발표 영상 : [발표 영상](https://www.youtube.com/watch?v=e4Z1Nv8bzfg&list=PLedGoSru7948o9_CdQBQZmIc-K3tR8eO9&index=2)
- 프로젝트 화면 영상 : [화면 영상](https://www.youtube.com/watch?v=pW8r0M16QmE&list=PLedGoSru7948o9_CdQBQZmIc-K3tR8eO9&index=5)
---



