# 🏠 자취생 누수 도우미 (LeakCheck)

자취생을 위한 **AI 기반 누수 진단 및 기록 안드로이드 앱**입니다.  
천장, 벽, 바닥 등의 누수 의심 상황을 사진으로 분석하고,  
진단 결과를 기록하며 집주인/관리실에 전달할 **신고 문구를 자동 생성**합니다.

---

## 📱 주요 기능

### 1️⃣ 사진 기반 AI 누수 분석
- 사용자가 촬영한 사진을 기반으로 **ML Kit Image Labeling**을 활용
- 누수 관련 키워드(water, stain, mold 등)를 분석하여
- **누수 가능성(%)**을 수치화하여 제공

### 2️⃣ 사진 + 메모 기록 저장
- 사진, 사용자 메모, AI 분석 결과를 함께 저장
- **Room Database**를 사용하여 로컬 DB에 기록 관리

### 3️⃣ 누수 기록 목록 관리
- 저장된 모든 누수 기록을 **RecyclerView**로 표시
- 기록 클릭 시 상세 결과 화면 이동
- 스와이프 삭제 기능 제공

### 4️⃣ 집주인/관리실 신고 문구 자동 생성
- 입력 정보(호수, 위치, 날짜, 상세 설명)를 기반으로
- 실제 연락에 바로 사용할 수 있는 **신고 문구 자동 생성**
- 클립보드 복사 기능 지원

---

## 🧠 AI 활용 방식

- Google **ML Kit Image Labeling (On-device)** 사용
- 클라우드 비용 없이 오프라인에서 이미지 분석 가능
- 분석 결과를 기반으로 자체 점수 로직을 적용하여
  누수 가능성을 % 형태로 사용자에게 제공

---

## 🛠 사용 기술 스택

| 구분 | 기술 |
|---|---|
| Language | Kotlin |
| Platform | Android |
| UI | XML, ConstraintLayout |
| AI | Google ML Kit (Image Labeling) |
| Database | Room (SQLite) |
| Architecture | Activity 기반 구조 |
| 기타 | RecyclerView, Intent, Clipboard API |

---

## 📂 프로젝트 구조

com.example.leakcheck
├── MainActivity
├── RecordActivity
├── LeakResultActivity
├── RecordListActivity
├── ReportTemplateActivity
├── DiagnosisActivity
├── database
│ ├── AppDatabase
│ ├── LeakRecord
│ └── LeakRecordDao
└── adapter
└── RecordAdapter

yaml
코드 복사

---

## 🔄 앱 실행 흐름

1. 메인 화면
2. 사진 + 메모로 누수 기록
3. AI 분석 결과 확인
4. 결과 저장
5. 기록 목록 확인
6. 집주인 신고 문구 생성 및 복사

---

## 🎯 기획 의도

자취생은 누수 발생 시  
- 원인을 명확히 설명하기 어렵고
- 집주인과의 소통에 부담을 느끼는 경우가 많습니다.

본 앱은  
**AI 분석 + 기록 관리 + 신고 문구 자동화**를 통해  
자취생의 생활 불편을 줄이는 것을 목표로 합니다.

---

## 👨‍🎓 개발자 정보

- 이름: 김민성  
- 학년: 대학교 3학년  
- 과목: AI 활용 앱 개발 과제

---

## ✅ 향후 개선 사항

- AI 분석 정확도 향상을 위한 Custom Model 적용
- Firebase 연동을 통한 클라우드 백업
- 누수 위험도 시각화(UI 개선)
- 알림 기능 추가

---

## 📸 실행 화면
(동영상 참조)
