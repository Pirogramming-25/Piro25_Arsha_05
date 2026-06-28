# Piro25_Arsha_05

피로그래밍 25기 1주차 토요일 팀 과제(배포용)를 위한 Arsha 페이지 전체 클론코딩 레포지토리입니다.


## ⏰ 과제 마감 및 규칙
- **마감 기한:** 06월 30일(화) 오전 10시까지 (커밋 시간 기준)
- **🚨 절대 금지 사항:** JavaScript 사용 금지, 외부 라이브러리/프레임워크/플러그인(Bootstrap, Tailwind, jQuery, React, Swiper.js, AOS 등) 사용 절대 불가.


## 🧑‍🤝‍🧑 조원 및 파트 분담

- **홍연우:** `PORTFOLIO` (포트폴리오 그리드 레이아웃 및 호버 효과)
- **정다희:** `TEAM` ~ `TESTIMONIALS` (팀원 프로필 카드, 슬라이드 자동 넘김)
- **이주헌:** `FREQUENTLY ASKED QUESTIONS` ~ `RECENT BLOG POSTS` (FAQ 토글, 블로그 카드)
- **유채영:** `Header`, `HOME` ~ `Call To Action`, `CONTACT`, `Footer` 및 초기 구조 세팅


## 🌿 브랜치(Branch) 규칙
우리 조의 베이스캠프(Default Branch)는 **`develop`**입니다. `main` 브랜치는 운영진 제출용이므로 직접 푸시하지 않습니다.

1. **`develop`** 브랜치에서 시작합니다.

2. 각자 규칙에 맞도록 본인의 작업 브랜치를 생성하여 작업합니다.
- `feature/#이슈번호-기능명`
    - *예: `feature/#1-Portfolio`*


3. 작업 완료 후 `develop` 브랜치를 향해 **Pull Request(PR)**를 생성합니다.
4. **Merge**는 추후 팀원들의 리뷰를 받은 후 진행하게 됩니다.


## 📋 이슈(Issue) 관리
새로운 섹션이나 기능 구현을 시작하기 전, 반드시 GitHub Issues 탭에 접속하여 본인 파트의 이슈를 먼저 생성합니다.

- **제목 양식:** `[feat] 작업 내용`
    - *예: `[feat] Portfolio 화면 구현`*

해당 이슈 기반으로 작업 브랜치를 생성합니다.


## 💬 커밋 메시지 컨벤션 (Commit Convention)
작업 단위별로 쪼개서 자주 커밋해 주세요. 메시지 맨 앞에는 아래 태그를 붙여줍니다.

- `feat: ...` (새로운 기능이나 레이아웃 구역 추가)
- `fix: ...` (깨진 레이아웃이나 버그 수정)
- `style: ...` (디자인 및 CSS 수정)
- `docs: ...` (주석 추가 및 README 수정)

*예: `feat: Portfolio Grid 이미지 배치 및 CSS 스타일링`*


## 📂 파일 구조 및 협업 가이드
Git 충돌(Conflict)을 방지하기 위해 HTML은 주석으로 구역을 나누고, CSS는 파트당 1개씩 파일을 분리하여 작업합니다.

```text
Piro25_Arsha_05/
├── .gitignore
├── index.html          (최종 본문 - 공통 뼈대 안에서 내 파트 주석 내부만 수정)
└── css/
    ├── reset.css       (공통 패딩/마진 초기화)
    ├── common.css      (아르샤 공통 컬러 변수 및 공통 스타일)
    ├── header.css
    ├── hero.css
    ├── about.css 
    ├── why-us.css
    ├── services.css
    ├── work-process.css
    ├── portfolio.css
    ├── team.css
    ├── pricing.css
    ├── testimonials.css
    ├── faq.css
    ├── subscribe.css
    ├── blog.css
    ├── contact.css 
    └── footer.css 
```

## 🚨 작업 시 주의사항
* **HTML:** `index.html`에서 오직 내 파트 주석 안쪽 공간만 건드려야 합니다. 다른 사람의 영역은 절대 수정하거나 지우지 않습니다.
* **CSS:** 오직 내가 구현할 부분에 맞는 CSS 파일만 수정합니다. `common.css`는 수정이 필요할 경우 팀원들과 상의 후 반영합니다.
* **공통 색상 변수 사용:** `common.css`에 명시되어 있는 색상을 홈페이지 내부 요소의 기본 색상으로 사용합니다. 개인 파일에서 `#37517e` 같은 색상 코드를 직접 적지 말고, 변수를 활용해 주세요.
  - *예시:* `background: var(--primary-color);`
* **공통 레이아웃 스타일 유지:** `common.css`에 명시되어 있는 공통 요소(`.container`, `section` 등)의 스타일을 타 CSS 파일에서 임의로 변경하거나 덮어쓰지 않습니다.

## 🚀 [참고] 필수 Git 명령어 루틴 (복붙용)

### 1-1. 작업 시작 전 - 브랜치 최초 생성
반드시 `develop`에서 최신 코드를 pull 받은 상태에서 새 브랜치를 팝니다.

```bash
# 1. develop 브랜치로 이동
git switch develop

# 2. 서버의 최신 코드 다운로드
git pull origin develop

# 3. 내 전용 브랜치 생성과 동시에 이동 
git switch -c "feature/#이슈번호-기능명"
```

### 1-2. 작업 시작 전 - 기존 브랜치 존재
그 사이에 `develop`에 업데이트한 최신 코드를 내 브랜치로 가져온 뒤 시작합니다.
```bash
# 1. develop 브랜치로 이동해서 최신 코드 pull 받기
git switch develop
git pull origin develop

# 2. 다시 내 작업 브랜치로 이동
git switch "feature/#이슈번호-기능명"

# 3. 최신 develop 내용을 내 브랜치로 병합(가져오기)
git merge develop
```

### 2. 작업 도중 저장 (하나의 작은 단위가 끝날 때마다 자주 실행!)
```bash
git status
# 상태는 add 전후 수시로 확인하는 것 추천합니다.

git add "파일명"
git commit -m "커밋메시지"
```


### 3. 작업 종료 및 깃허브 업로드 (마무리할 때)
```bash 
git push origin "feature/#이슈번호-브랜치명"
```
업로드 후 GitHub 웹사이트에서 Pull Request(PR)를 날리고 팀원들에게 공유합니다.
