# 🚚 Dealivery - P2P 퀵 서비스 매칭 플랫폼

> **Deal + Delivery = Dealivery**  
> 사용자와 사용자를 직접 연결하는 혁신적인 퀵 서비스 플랫폼

## 📋 프로젝트 소개

Dealivery는 Django를 기반으로 구축된 P2P(Peer-to-Peer) 퀵 서비스 매칭 웹 애플리케이션입니다. 기존의 배송업체와 고객을 연결하는 방식과 달리, **사용자 간 직접 매칭**을 통해 더 빠르고 저렴한 배송 서비스를 제공합니다.

### 핵심 가치
- **빠른 매칭**: 실시간 요청/응답 시스템
- **경제적 배송**: 중간 수수료 없는 직접 거래
- **상호 도움**: 커뮤니티 기반 배송 생태계
- **유연한 서비스**: 언제든 요청자↔배송자 역할 전환 가능

## ✨ 주요 기능

### 사용자 관리
- 회원가입/로그인 시스템
- 개인정보 및 연락처 관리
- 실시간 알림 시스템

### 배송 요청 시스템
- 픽업/배송 주소 설정
- 카테고리별 분류
- 최소 금액 설정 (5,000원 이상)
- 상세 설명 및 이미지 첨부

### 입찰 및 매칭
- 실시간 입찰 시스템
- 자동 최고가 업데이트
- 매칭 완료 시 자동 알림
- 거래 완료 후 상호 연락처 교환

### 개인 대시보드
- 내 요청 목록 관리
- 참여한 입찰 현황
- 완료된 거래 내역
- 관심 목록(워치리스트) 관리

## 🛠️ 기술 스택

### Backend
- **Framework**: Django 3.x
- **Database**: SQLite3
- **Language**: Python 3.8+

### Frontend
- **CSS Framework**: Bootstrap 4/5
- **Icons**: Font Awesome
- **Fonts**: Google Fonts (GmarketSans)
- **JavaScript**: jQuery, MDB

### Dependencies
- `django-annoying`: 편의 기능 제공
- `Pillow`: 이미지 처리 (선택사항)

## 🚀 설치 및 실행

### 1. 저장소 클론
```bash
git clone <repository-url>
cd Dealivery/Dealivery-master
```

### 2. 가상환경 설정
```bash
# 가상환경 생성
python -m venv dealivery_env

# 가상환경 활성화
# Windows
dealivery_env\Scripts\activate
# macOS/Linux
source dealivery_env/bin/activate
```

### 3. 의존성 설치
```bash
pip install django
pip install django-annoying
pip install pillow  # 이미지 처리용 (선택사항)
```

### 4. 데이터베이스 설정
```bash
# 마이그레이션 실행
python manage.py migrate

# 관리자 계정 생성 (선택사항)
python manage.py createsuperuser
```

### 5. 서버 실행
```bash
python manage.py runserver
```

웹 브라우저에서 `http://localhost:8000`으로 접속하여 서비스를 이용할 수 있습니다.

## 📱 사용법

### 첫 시작
1. **회원가입**: 이메일, 전화번호 등 기본 정보 입력
2. **로그인**: 생성한 계정으로 로그인

### 배송 요청하기
1. **요청 생성**: "퀵 서비스 요청" 버튼 클릭
2. **정보 입력**: 픽업/배송 주소, 가격, 카테고리, 설명 입력
3. **요청 등록**: 실시간 요청 목록에 자동 게시

### 배송 수행하기
1. **목록 확인**: "실시간 요청 목록"에서 적합한 요청 찾기
2. **입찰 참여**: 원하는 가격으로 입찰
3. **매칭 완료**: 요청자가 입찰 수락 시 자동 매칭

### 거래 관리
- **마이페이지**: 내 요청/입찰 현황 확인
- **알림 확인**: 매칭 완료 시 실시간 알림
- **거래 완료**: 상호 연락처로 직접 연락하여 배송 진행

## 🗄️ 데이터베이스 구조

### 주요 모델
- **User**: 사용자 정보 (전화번호, 알림 설정 포함)
- **Listing**: 배송 요청 정보
- **Bid**: 입찰 정보
- **Comment**: 댓글 시스템
- **Watchlist**: 관심 목록
- **Winner**: 매칭 완료된 거래 정보

## 🎨 주요 페이지

- **메인 페이지** (`/`): 서비스 소개 및 시작
- **이용안내** (`/intro`): 서비스 이용 방법
- **실시간 요청 목록** (`/activelisting`): 현재 활성화된 배송 요청
- **요청 생성** (`/createlisting`): 새 배송 요청 등록
- **마이페이지** (`/dashboard`): 개인 거래 현황
- **매칭 완료** (`/closedlisting`): 완료된 거래 목록

## 🔧 개발 환경 설정

### 디렉토리 구조
```
Dealivery-master/
├── auctions/                 # 메인 앱
│   ├── migrations/          # 데이터베이스 마이그레이션
│   ├── static/             # 정적 파일 (CSS, 이미지, JS)
│   ├── templates/          # HTML 템플릿
│   ├── models.py           # 데이터베이스 모델
│   ├── views.py            # 뷰 로직
│   └── urls.py             # URL 라우팅
├── commerce/               # Django 설정
│   ├── settings.py         # 프로젝트 설정
│   └── urls.py             # 메인 URL 설정
├── db.sqlite3              # SQLite 데이터베이스
└── manage.py               # Django 관리 스크립트
```

### 주요 설정
- **언어**: 한국어 (ko-kr)
- **시간대**: Asia/Seoul
- **디버그 모드**: 개발 시 True
- **허용 호스트**: 개발 시 모든 호스트 허용

## 🤝 기여하기

프로젝트에 기여하고 싶으시다면 언제든 Pull Request를 생성해 주세요!

### 기여 방법
1. 저장소를 포크합니다
2. 새로운 브랜치를 생성합니다 (`git checkout -b feature/AmazingFeature`)
3. 변경사항을 커밋합니다 (`git commit -m 'Add some AmazingFeature'`)
4. 브랜치에 푸시합니다 (`git push origin feature/AmazingFeature`)
5. Pull Request를 생성합니다

## 📝 라이선스

이 프로젝트는 [MIT](https://opensource.org/licenses/MIT) 라이선스 하에 배포됩니다.
