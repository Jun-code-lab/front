# Project Overview

치톤피드 (Chiton Feed) - 식물 키우기 웹뷰 앱

반응형 웹 프로젝트로 HTML과 CSS만을 사용하여 구축됩니다.
최종 목적은 웹뷰 앱이므로 모바일 뷰가 최우선입니다.

## Project Requirements

- **Technology Stack**: HTML and CSS only (no JavaScript frameworks)
- **Final Deliverables**: Pure HTML and CSS files
- **Primary Target**: 웹뷰 앱 (Mobile-First)
- **Target Devices**:
  - iPhone: 375px ~ 430px (iPhone SE ~ iPhone Pro Max)
  - Galaxy: 360px ~ 412px (Galaxy S 시리즈)
  - Base Width: 375px
- **Orientation**: Portrait (세로) only
- **Total Pages**: 19 pages

## Development Guidelines

### Responsive Design Approach
- **Mobile-First 필수**: 모바일 뷰가 가장 중요 (웹뷰 앱 목적)
- Base: 375px (iPhone 기준)
- CSS media queries 사용
- Breakpoints:
  - Mobile (Primary): 360px - 430px
  - Tablet (Optional): 768px - 1023px
  - Desktop (Optional): 1024px and above

### CSS Best Practices
- Use flexbox or CSS Grid for layouts
- Use relative units (%, em, rem, vw, vh) instead of fixed pixels where appropriate
- Viewport meta tag: `<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">`
- 웹뷰 앱 최적화:
  - 터치 친화적 UI (최소 44px 터치 영역)
  - 이미지 최적화 (빠른 로딩)
  - CSS 애니메이션 최적화
  - 부드러운 스크롤
- Test on iPhone and Galaxy devices

## Page Structure (총 19 페이지)

### 1. 시작/로그인 (3페이지)
1. **시작 페이지** - `index.html`
   - 1초 스플래시 화면
   - 앱 로고 표시

2. **로그인** - `pages/auth/login.html`
   - Google 로그인만 지원
   - 간단한 로그인 인터페이스

3. **프로필 등록** - `pages/auth/profile-setup.html`
   - 사용자 프로필 정보 입력
   - 닉네임, 프로필 사진 등

### 2. 온보딩 (7페이지)
처음 가입한 사용자만 보는 화면

4. **온보딩 메인** - `pages/onboarding/intro.html`
   - 앱 소개 및 안내

5. **기기 등록** - `pages/onboarding/device-register.html`
   - IoT 기기 연동 시작

6. **연동 완료** - `pages/onboarding/device-connected.html`
   - 기기 연동 성공 화면

7. **식물 등록** - `pages/onboarding/plant-register.html`
   - 키울 식물 정보 입력

8. **치피 탄생** - `pages/onboarding/chipi-birth.html`
   - 캐릭터(치피) 생성 화면

9. **하이 치피** - `pages/onboarding/chipi-greeting.html`
   - 치피와 첫 만남

### 3. 키트 심는 방법 (3페이지)
10. **키트 심는 방법** - `pages/guide/planting.html`
    - 식물 키트 심기 가이드

11. **물 주는 방법** - `pages/guide/watering.html`
    - 물주기 가이드

12. **영양제 주는 방법** - `pages/guide/fertilizer.html`
    - 영양제 사용 가이드

### 4. 홈 페이지 (3페이지)
13. **홈 페이지 (기본)** - `pages/home/main.html`
    - 메인 대시보드
    - 식물 상태 확인

14. **낮 버전** - `pages/home/day.html`
    - 낮 시간대 테마

15. **밤 버전** - `pages/home/night.html`
    - 밤 시간대 테마

### 5. 성장일지 (3페이지)
16. **성장일지 메인** - `pages/diary/list.html`
    - 성장 기록 목록

17. **등록** - `pages/diary/create.html`
    - 새로운 일지 작성

18. **결과** - `pages/diary/detail.html`
    - 일지 상세 보기

### 6. 마이페이지 (1페이지)
19. **마이페이지** - `pages/mypage/index.html`
    - 사용자 설정 및 정보

---

## File Structure

### 프로젝트 폴더 구조:
```
front/
├── index.html                          # 1. 시작 페이지 (스플래시)
│
├── pages/
│   ├── auth/                           # 인증 관련
│   │   ├── login.html                  # 2. 로그인
│   │   └── profile-setup.html          # 3. 프로필 등록
│   │
│   ├── onboarding/                     # 온보딩 (첫 사용자)
│   │   ├── intro.html                  # 4. 온보딩 메인
│   │   ├── device-register.html        # 5. 기기 등록
│   │   ├── device-connected.html       # 6. 연동 완료
│   │   ├── plant-register.html         # 7. 식물 등록
│   │   ├── chipi-birth.html            # 8. 치피 탄생
│   │   └── chipi-greeting.html         # 9. 하이 치피
│   │
│   ├── guide/                          # 가이드
│   │   ├── planting.html               # 10. 키트 심는 방법
│   │   ├── watering.html               # 11. 물 주는 방법
│   │   └── fertilizer.html             # 12. 영양제 주는 방법
│   │
│   ├── home/                           # 홈 (메인)
│   │   ├── main.html                   # 13. 홈 페이지
│   │   ├── day.html                    # 14. 낮 버전
│   │   └── night.html                  # 15. 밤 버전
│   │
│   ├── diary/                          # 성장일지
│   │   ├── list.html                   # 16. 성장일지 메인
│   │   ├── create.html                 # 17. 등록
│   │   └── detail.html                 # 18. 결과
│   │
│   └── mypage/                         # 마이페이지
│       └── index.html                  # 19. 마이페이지
│
├── css/
│   ├── base/
│   │   ├── reset.css                   # CSS 리셋
│   │   ├── variables.css               # CSS 변수 (색상, 폰트, 간격)
│   │   └── typography.css              # 타이포그래피
│   │
│   ├── layout/
│   │   ├── header.css                  # 헤더 (있을 경우)
│   │   ├── footer.css                  # 푸터
│   │   ├── navigation.css              # 네비게이션 바
│   │   └── container.css               # 컨테이너 레이아웃
│   │
│   ├── components/
│   │   ├── buttons.css                 # 버튼 스타일
│   │   ├── cards.css                   # 카드 컴포넌트
│   │   ├── forms.css                   # 폼 요소
│   │   └── character.css               # 치피 캐릭터 스타일
│   │
│   ├── pages/
│   │   ├── splash.css                  # 스플래시 화면
│   │   ├── auth.css                    # 로그인/프로필
│   │   ├── onboarding.css              # 온보딩
│   │   ├── guide.css                   # 가이드
│   │   ├── home.css                    # 홈 페이지
│   │   ├── diary.css                   # 성장일지
│   │   └── mypage.css                  # 마이페이지
│   │
│   └── mobile.css                      # 모바일 전용 스타일 (우선)
│
├── images/
│   ├── common/                         # 공통 이미지
│   │   ├── logo.png                    # 로고
│   │   ├── icons/                      # 아이콘들
│   │   └── backgrounds/                # 배경 이미지
│   │
│   ├── auth/                           # 로그인 관련 이미지
│   ├── onboarding/                     # 온보딩 이미지
│   ├── chipi/                          # 치피 캐릭터 이미지
│   ├── plants/                         # 식물 이미지
│   ├── guide/                          # 가이드 이미지
│   └── diary/                          # 일지 관련 이미지
│
├── fonts/                              # 웹폰트
└── CLAUDE.MD                           # 프로젝트 문서
```

---

## CSS 연결 방법

### HTML 기본 구조

**루트 페이지 (index.html):**
```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>치톤피드 - 스플래시</title>

    <!-- CSS -->
    <link rel="stylesheet" href="css/base/reset.css">
    <link rel="stylesheet" href="css/base/variables.css">
    <link rel="stylesheet" href="css/base/typography.css">
    <link rel="stylesheet" href="css/components/buttons.css">
    <link rel="stylesheet" href="css/pages/splash.css">
    <link rel="stylesheet" href="css/mobile.css">
</head>
<body>
    <!-- 콘텐츠 -->
</body>
</html>
```

**서브 페이지 예시 (pages/home/main.html):**
```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>치톤피드 - 홈</title>

    <!-- CSS -->
    <link rel="stylesheet" href="../../css/base/reset.css">
    <link rel="stylesheet" href="../../css/base/variables.css">
    <link rel="stylesheet" href="../../css/base/typography.css">
    <link rel="stylesheet" href="../../css/layout/navigation.css">
    <link rel="stylesheet" href="../../css/components/buttons.css">
    <link rel="stylesheet" href="../../css/components/cards.css">
    <link rel="stylesheet" href="../../css/components/character.css">
    <link rel="stylesheet" href="../../css/pages/home.css">
    <link rel="stylesheet" href="../../css/mobile.css">
</head>
<body>
    <!-- 콘텐츠 -->
</body>
</html>
```

---

## 개발 가이드

### 페이지 관리 팁:
- **네이밍 규칙**: 파일명은 소문자와 하이픈 사용 (예: `device-register.html`)
- **상대 경로 주의**: pages 폴더 안의 파일들은 `../../`로 CSS/이미지 접근
- **공통 구조**: 반복되는 HTML은 복사-붙여넣기 (네비게이션, 푸터 등)
- **스타일 재사용**: 비슷한 레이아웃의 페이지는 같은 CSS 공유
- **이미지 최적화**:
  - WebP 포맷 사용 권장
  - 모바일용 해상도로 최적화 (2x 리티나 고려)
  - Lazy loading 고려

### CSS 작성 가이드:
- **Mobile-First**: 기본 스타일은 모바일용, 미디어 쿼리로 확장
- **CSS 변수 활용**: `variables.css`에 색상, 폰트, 간격 정의
- **BEM 방법론**: 클래스명 규칙 (예: `.button--primary`, `.card__title`)
- **성능**: 불필요한 애니메이션 지양, transform/opacity 위주 사용

### 우선순위:
1. **1단계**: 스플래시 → 로그인 → 홈 페이지 (핵심 플로우)
2. **2단계**: 온보딩 플로우 완성
3. **3단계**: 성장일지, 가이드 페이지
4. **4단계**: 마이페이지 및 세부 기능

---

## 참고사항

### 코드 품질:
- 깔끔하고 유지보수 가능한 코드 작성
- Semantic HTML5 요소 사용 (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`)
- 접근성 고려 (ARIA labels, alt text 필수)
- HTML/CSS 유효성 검증 후 배포

### 웹뷰 앱 특화:
- 터치 이벤트 최적화
- 네이티브 앱처럼 보이도록 디자인
- 로딩 속도 중요 (이미지 압축, CSS 최적화)
- Pull-to-refresh, 스와이프 제스처 고려

### 브라우저 호환성:
- 주요 타겟: iOS Safari, Android Chrome
- CSS Flexbox/Grid 안전하게 사용 가능
- 최신 CSS 기능 사용 시 fallback 고려

---

## 다음 단계

1. **폴더 구조 생성**: pages, css, images 폴더 생성
2. **베이스 파일 작성**: reset.css, variables.css 등 기본 CSS
3. **피그마 디자인 확인**: 각 페이지별 디자인 세부사항 확인
4. **1단계 페이지 개발**: 스플래시 → 로그인 → 홈 순서로 진행
