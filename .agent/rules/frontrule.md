---
trigger: always_on
---

1. 프로젝트 개요 (Project Overview)
프로젝트명: 치톤피드 (Chiton Feed) - 식물 키우기 웹뷰 앱
성격: 반응형 웹 프로젝트 (웹뷰 앱 타겟)
핵심 목표: 모바일 뷰 최우선 (Mobile-First), 네이티브 앱과 유사한 사용자 경험 제공
2. 기술 스택 및 제약사항 (Tech Stack & Constraints)
Core: HTML5, CSS3 Only
금지: React, Vue, Angular 등 JavaScript 프레임워크 사용 금지.
JavaScript: 로직이 꼭 필요한 경우에만 바닐라 JS 최소 사용 (기본은 HTML/CSS로 해결).
최종 결과물: 순수 .html 및 .css 파일.
타겟 디바이스:
Primary: iPhone (375px ~ 430px), Galaxy (360px ~ 412px).
Base Width: 375px (iPhone SE 기준).
Orientation: Portrait (세로 모드) Only.
3. 파일 및 폴더 구조 (File Structure)
프로젝트 루트는 front/이며, 아래 구조를 엄격히 준수한다.

text
front/
├── index.html                          # [Page 1] 시작 페이지 (스플래시)
├── pages/
│   ├── auth/                           # 인증
│   │   ├── login.html                  # [Page 2] 로그인 (Google Only)
│   │   └── profile-setup.html          # [Page 3] 프로필 등록
│   ├── onboarding/                     # 온보딩
│   │   ├── intro.html                  # [Page 4] 앱 소개
│   │   ├── device-register.html        # [Page 5] 기기 등록
│   │   ├── device-connected.html       # [Page 6] 연동 완료
│   │   ├── plant-register.html         # [Page 7] 식물 등록
│   │   ├── chipi-birth.html            # [Page 8] 치피 탄생
│   │   └── chipi-greeting.html         # [Page 9] 하이 치피
│   ├── guide/                          # 가이드
│   │   ├── planting.html               # [Page 10] 키트 심기
│   │   ├── watering.html               # [Page 11] 물주기
│   │   └── fertilizer.html             # [Page 12] 영양제
│   ├── home/                           # 홈
│   │   ├── main.html                   # [Page 13] 홈 (기본)
│   │   ├── day.html                    # [Page 14] 낮 테마
│   │   └── night.html                  # [Page 15] 밤 테마
│   ├── diary/                          # 성장일지
│   │   ├── list.html                   # [Page 16] 목록
│   │   ├── create.html                 # [Page 17] 등록
│   │   └── detail.html                 # [Page 18] 상세
│   └── mypage/                         # 마이페이지
│       └── index.html                  # [Page 19] 설정
├── css/
│   ├── base/                           # reset.css, variables.css, typography.css
│   ├── layout/                         # header.css, footer.css, navigation.css, container.css
│   ├── components/                     # buttons.css, cards.css, forms.css, character.css
│   ├── pages/                          # 각 페이지별 전용 CSS (splash.css, home.css 등)
│   └── mobile.css                      # 모바일 전용 스타일
├── images/                             # common, auth, onboarding, chipi, plants, guide, diary
└── fonts/                              # 웹폰트
4. 코딩 컨벤션 (Coding Conventions)
4.1 HTML
Semantic Markup: <header>, <nav>, <main>, <section>, <article>, <footer>를 사용하여 구조화한다.
Viewport Meta: 모든 HTML 파일 <head>에 필수 포함.
html
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
접근성 (Accessibility): 모든 <img> 태그에 alt 속성 필수. 버튼 및 입력 폼에 aria-label 적절히 사용.
CSS 연결:
Root (index.html): css/base/... 경로 사용.
Sub-pages (pages/...): ../../css/base/... 상대 경로 사용.
4.2 CSS
Methodology: BEM (Block Element Modifier) 방식을 따른다. (예: .card__header, .btn--primary)
Variables: 색상, 폰트, 여백 등은 반드시 css/base/variables.css에 정의된 CSS 변수를 사용한다.
Layout: flexbox 또는 grid를 사용하여 배치한다. float 사용 지양.
Units: 고정 픽셀(px) 대신 상대 단위(%, rem, vw, vh)를 적극 활용한다.
Reset: 모든 페이지는 reset.css를 가장 먼저 로드한다.
5. 디자인 및 UI/UX 가이드 (Design & UI/UX)
5.1 반응형 전략 (Mobile-First)
기본 스타일: 375px (iPhone) 기준으로 작성한다.
Breakpoints:
Mobile (Primary): 360px ~ 430px
Tablet: 768px ~ 1023px (Optional)
Desktop: 1024px+ (Optional)
미디어 쿼리는 모바일 스타일을 덮어쓰는(override) 방식으로 작성한다.
5.2 웹뷰 최적화 (Webview Optimization)
Touch Targets: 모든 터치 요소(버튼, 링크)는 최소 44px × 44px 영역을 확보한다.
Scrolling: -webkit-overflow-scrolling: touch; 등을 활용하여 부드러운 스크롤을 구현한다.
Images: 고해상도 디스플레이(Retina)를 고려하여 2x 이미지를 사용하거나 벡터(SVG)를 활용한다. 포맷은 WebP 권장.
Performance: 무거운 애니메이션을 피하고, transform과 opacity 속성을 이용한 가벼운 전환 효과를 사용한다.
6. 개발 프로세스 및 우선순위 (Roadmap)
Phase 1: 기반 구축 및 핵심 플로우
폴더 구조 생성 및 공통 CSS (reset, variables) 작성.
스플래시(index.html) → 로그인(auth/) → 홈(home/) 개발.
Phase 2: 온보딩 프로세스
인트로 → 기기 등록 → 식물 등록 → 치피 탄생 플로우 구현.
Phase 3: 서브 기능 구현
성장일지(diary/), 가이드(guide/) 페이지 개발.
Phase 4: 마무리
마이페이지(mypage/) 및 전체 UI 디테일 폴리싱.
디바이스 테스트 (iPhone/Galaxy 해상도 검증).
7. 기타 규칙 (Misc)
네이밍:
HTML 파일명: kebab-case (예: device-register.html)
CSS 클래스명: BEM (예: profile-setup__input)
코드 품질:
중복 코드는 컴포넌트 CSS로 분리하여 재사용한다.
HTML/CSS 유효성 검사를 통과해야 한다.