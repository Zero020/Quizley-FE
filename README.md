# <img src="https://github.com/user-attachments/assets/1aabaf99-c19a-4983-affb-56d522320ae4" alt="" width="29" height="34" /> Quizley-FE 
하루 한 번 **상상력을 자극하는 질문**으로 생각하는 힘을 길러주는 서비스, Quizley의 React + TypeScript + Vite 기반 프론트엔드 레포지토리입니다.
<img width="1920" height="1080" alt="" src="https://github.com/user-attachments/assets/26797c13-f8f4-4881-88a3-f80fd3a05902" />

<br>

## Index

1. [About Quizley](#about-quizley)
2. [Main Function](#main-function)
3. [Project Structure 📁](#project-structure-)
4. [Tech Stack 🛠️](#tech-stack-)
5. [GitHub Flow Guidelines 🔀](#github-flow-guidelines-)
6. [API Integration Rules ⚡](#api-integration-rules-)
7. [Deployment 🚀](#deployment-)
8. [Team 👊](#team-)


<br>

## About Quizley
현대 사회에서 AI 도구 사용이 늘어나면서 정답을 빠르게 얻는 데 익숙해지고 스스로 사고하는 습관이 약화되고 있어 이를 극복하고자, **하루에 한 번씩 상상력을 자극할 수 있는 질문들에 대답해 보며 스스로 생각하는 힘을 기를 수 있도록 도와주는 서비스**를 만들었습니다.

<br>

## Main Function
<img width="500" height="300" alt="홈" src="https://github.com/user-attachments/assets/f7e41714-1fe1-4dfa-9695-d187a34b8a29" />
<img width="500" height="300" alt="홈 (1)" src="https://github.com/user-attachments/assets/042b4b22-bb06-45e9-83a5-88404b3f9eea" />
<img width="500" height="300" alt="홈 - 주말" src="https://github.com/user-attachments/assets/0de7f9fd-8f62-49be-aa37-033e4180f360" />
<img width="500" height="300" alt="홈 - 알림" src="https://github.com/user-attachments/assets/4994cade-e384-4ab7-a3e0-5ea305a2f246" />
<img width="500" height="300" alt="커뮤니티" src="https://github.com/user-attachments/assets/fb127079-a291-4d1f-b0f4-d6c32599cab4" />
<img width="500" height="300" alt="기록" src="https://github.com/user-attachments/assets/45f53021-654d-47cb-bd65-63a2033d9ce1" />
<img width="500" height="300" alt="기록 (1)" src="https://github.com/user-attachments/assets/84b61a5a-6396-4947-b693-1bffc113fe3e" />


<br>
<br>

##  Project Structure 📁
```
Quizley
├── .github
│   └── ISSUE_TEMPLATE
│   │   └── todo---프론트--.md          # 이슈 템플릿
│   └── pull_request_template.md        # PR 템플릿
└── quizley
    ├── public                          # 정적 파일
    │   └── favicon.svg
    ├── src
    │   ├── api                         # API 요청 관련 모듈
    │   │   ├── auth.ts                 # 로그인/회원가입/토큰발급 API
    │   │   ├── balance.ts              # 밸런스 게임 관련 API
    │   │   ├── communityApi.ts         # 커뮤니티 관련 API
    │   │   ├── notifications.ts        # 알림 관련 API
    │   │   ├── ...
    │   │   └── request.ts              # axios/fetch 공통 설정 + 토큰 자동 재발급
    │   ├── assets                      # 이미지 및 아이콘
    │   │   ├── icon / img
    │   ├── component                   # 재사용 가능한 UI 컴포넌트
    │   │   ├── answerQInput.tsx
    │   │   ├── btnLong.tsx
    │   │   ├── calender.tsx
    │   │   ├── ...
    │   ├── context                     # 레벨업을 위한 글로벌 상태 관리
    │   │   └── LevelCotext.tsx
    │   ├── pages                       # 라우팅되는 실제 페이지 화면
    │   │   ├── quizleyBotPage.tsx
    │   │   ├── community / ...
    │   │   ├── ReportTodayInsightPage.tsx
    │   │   └── ...
    │   ├── types                       # TypeScript 타입 선언
    │   │   └── assets.d.ts
    │   ├── App.tsx
    │   ├── App.css
    │   ├── index.css                   # Tailwind 기반 스타일 초기화 + 디자인 토큰
    │   ├── main.tsx
    │   └── vite-env.d.ts 
    ├── .env                            # 환경 변수 (API URL 등)
    ├── index.html
    ├── package.json                    # 의존성 및 스크립트 관리
    ├── tailwind.config.js              # Tailwind CSS 설정
    ├── tsconfig.json                   # TypeScript 설정
    └── vite.config.js                  # Vite 개발/빌드 환경 설정
```

<br>

##  Tech Stack 🛠️
- React · TypeScript · Vite
- Tailwind CSS
  
<br>

##  UI Guidelines 🎨

- index.css, tailwind.config.js 내부의 **디자인 토큰**을 기반으로 화면 스타일을 구성
- 컴포넌트 제작 시 반드시 토큰 기반 클래스 또는 **Tailwind 유틸 클래스**를 사용해 일관성을 유지

<br>

## GitHub Flow Guidelines 🔀

>  **Issue → Branch → Commit → Push → PR → Review → dev 병합**

### 1. ISSUE
- 내용:
  - Description(요약)
  - 할 일 목록
- 태그:
  - Reviewers: 타인 코드 수정 시 해당 팀원, 없으면 전원
  - Labels: 생성된 라벨만 사용
  - Assignees: 본인
  - Development: dev 브랜치 선택 후 branch 생성

### 2. BRANCH
- 메인 개발 브랜치: dev

`{issue-number}-{작업요약}`
예) 23-mypage

### 3. Commit Convention
| 타입       | 설명        |
| -------- | --------- |
| feat     | 새로운 기능 추가 |
| fix      | 버그 수정     |
| refactor | 코드 구조 변경  |
| perf     | 성능 개선     |
| merge    | 브랜치 병합    |
| conflict | 충돌 해결     |
`feat: 마이페이지 기본 UI 구현`

### 4. Push
- 작업 완료 후 push
- push 전 반드시 dev pull → merge → push

### 5. Pull Request
- 내용 : 작업 내용 요약, 작업 화면 스크린샷 첨부, 리뷰 받고 싶은 부분 작성
- 태그 : reviewers, assignees, labels 지정
- dev 브랜치로 PR 생성 -> merge 후 브랜치 close

<br>

## API Integration Rules ⚡
- 모든 공통 설정은 src/api/request.ts에서 Axios 인스턴스로 관리
- API별로 폴더 분리 (auth, quiz, community 등)
- 화면 내부(.tsx)에서만 API 호출 작성

<br>

## Deployment 🚀

### 1) 인프라 구조

- **Vercel**
  - Quizley-FE의 정적 파일을 호스팅
  - GitHub 연동을 통한 자동 빌드 & 배포

- **Backend API**
  - 인증, 커뮤니티, 퀴즈 등 모든 데이터 제공

### 2) 배포 방식

- GitHub ↔ Vercel 연동을 통해 **자동 배포** 수행
- 설정된 브랜치(`main` 또는 `dev`)에 코드가 머지되면 자동으로:
  1. 의존성 설치
  2. Vite 기반 프로덕션 빌드 (`npm run build`)
  3. 글로벌 CDN에 배포 완료

- 로컬 환경 변수는 `.env`, 배포 환경 변수는 Vercel Dashboard에서 관리

### 3) 배포 플로우

1. 작업 브랜치 생성 → 기능 구현  
2. PR 생성 → `dev` 브랜치로 merge  
3. dev 업데이트 감지 → Vercel 자동 빌드 & 배포  
4. 배포 URL에서 즉시 새로운 버전 확인 가능

<br>

## Team 👊
- planning & Design | 최서연, 류사랑
- Backend | 김민서, 장혜리, 송유리
- Frontend
  - 김시원: 홈화면
  - 손예원: 로그인/회원가입, 마이페이지, 기록
  - 최영: 커뮤니티

<br>

## Other Information
### 🔗 Backend Repository: https://github.com/Linaeformin/Quizley
** 본 레포지토리는 'Quizley'의 프론트엔드 레포지토리입니다.



