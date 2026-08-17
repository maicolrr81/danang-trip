# 🌴 다낭 가족여행 웹앱

우리 가족 14명, 2026년 10월 22~26일 다낭 여행을 위한 모바일 웹앱.

## 📱 사이트

**https://maicolrr81.github.io/danang-trip/**

## 🏗 구조

- **프론트엔드**: 단일 `index.html` (HTML/CSS/JS 인라인) · GitHub Pages 호스팅
- **데이터베이스**: 구글 시트 · [열기](https://docs.google.com/spreadsheets/d/1nXxRSQUMHYoL8dK4rODXT6MPfw967qLn8LALmd-dcvg/edit)
- **시트 → JSON 프록시**: [opensheet.elk.sh](https://opensheet.elk.sh)
- **지도**: Leaflet + OpenStreetMap (API 키 불필요)

## ✏️ 편집 방법

### 데이터 편집 (장소·일정 추가/수정)
1. [구글 시트 열기](https://docs.google.com/spreadsheets/d/1nXxRSQUMHYoL8dK4rODXT6MPfw967qLn8LALmd-dcvg/edit)
2. `장소` 또는 `일정` 탭에서 직접 편집
3. 저장하면 앱 새로고침 시 자동 반영 (몇 초 지연 있을 수 있음)

### 디자인/기능 편집
1. `index.html` 편집
2. `git commit` → `git push`
3. 1~2분 후 사이트 반영

## ⚠️ 시트 규칙

- **1행 = 헤더** (변경 금지)
- **2행부터 = 데이터**
- 카테고리는 드롭다운 값만 사용 (숙소·식당·마사지·네일·쇼핑·관광·카페·이동)
- 위도·경도는 구글맵에서 우클릭 → 좌표 복사

## 🎨 색상 팔레트

- 배경: `#0a1220` (다크)
- 메인: `#2dd4bf` (티얼)
- 서브: `#fb7185` (코럴)
- 강조: `#fbbf24` (모래)

## 📋 기능

- [x] 홈 화면 (D-day, 항공, 숙소, 오늘 일정, 미니 지도, 긴급 연락처)
- [x] 일정 (Day별 타임라인)
- [x] 지도 (Leaflet, 카테고리 필터, 검색)
- [x] 장소 리스트 (카테고리별 그룹)
- [x] 장소 상세 (주소 복사, 구글맵·그랩 링크)
- [x] 환율 계산기 (VND ↔ KRW)
- [x] 베트남어 회화 (검색, 음성 재생)
- [ ] 웹에서 직접 장소 등록 (예정: Google Apps Script)
- [ ] 준비물 체크리스트 UI
- [ ] 인원 관리 UI

## 🔧 로컬 테스트

```bash
# 단순 정적 파일 서빙
python3 -m http.server 8000
# 또는
npx serve
```

브라우저에서 http://localhost:8000
