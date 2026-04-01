# 📖 나의 일기장 (My Private Diary)

한국어 개인 일기 웹앱입니다. 로그인, 기분/날씨 기록, Google Sheets 연동까지 지원하는 싱글 파일 앱입니다.

---

## ✨ 주요 기능

- 🔐 **로그인 보호** — 아이디/비밀번호로 일기장 잠금
- 📝 **일기 작성** — 제목, 본문, 기분(이모지), 날씨 선택
- 💾 **로컬 저장** — `localStorage`에 자동 저장 (오프라인 동작)
- 📊 **Google Sheets 연동** — OAuth 2.0으로 구글 스프레드시트에 동기화
- 📈 **통계** — 총 일기 수 / 작성 일수 / 총 글자수 / 이번 달 작성 수
- 📅 **최근 일기 목록** — 클릭 시 불러오기
- 📱 **반응형 디자인** — 모바일/데스크톱 모두 지원

---

## 🚀 사용 방법

### 1. 바로 실행 (로컬)

```bash
# 저장소 클론
git clone https://github.com/<your-username>/diary-app.git
cd diary-app

# index.html을 브라우저에서 열기
open index.html   # macOS
start index.html  # Windows
```

### 2. GitHub Pages로 배포

1. 이 저장소를 Fork 하거나 직접 생성
2. **Settings → Pages → Branch: main / root** 설정
3. `https://<your-username>.github.io/diary-app/` 에서 접속

---

## 🔑 기본 로그인 계정

| 항목 | 값 |
|------|-----|
| 아이디 | `admin` |
| 비밀번호 | `admin` |

> ⚠️ 보안을 위해 `index.html` 파일 내 `CRED` 객체의 아이디/비밀번호를 반드시 변경하세요.
> 
> ```js
> const CRED = { id: 'your-id', pw: 'your-password' };
> ```

---

## 📊 Google Sheets 연동 설정

Google Sheets에 일기를 자동 저장하려면 OAuth Client ID가 필요합니다.

1. [Google Cloud Console](https://console.cloud.google.com) 접속
2. **Google Sheets API** 활성화
3. **사용자 인증 정보 → OAuth 2.0 클라이언트 ID** 생성 (웹 애플리케이션 유형)
4. 승인된 JavaScript 원본에 앱 URL 추가 (예: `https://your-username.github.io`)
5. 앱 내 **⚙️ 설정** 버튼에서 Client ID 입력 후 저장
6. Google Sheets URL을 사이드바에 붙여넣기

---

## 🗂️ 파일 구조

```
diary-app/
└── index.html   # 전체 앱 (HTML + CSS + JS 단일 파일)
```

---

## 🛠️ 기술 스택

- **Vanilla HTML / CSS / JavaScript** — 프레임워크 없음
- **Google Sheets API v4** — 일기 데이터 클라우드 저장
- **Google OAuth 2.0** — 인증
- **Nanum Myeongjo / Noto Sans KR** (Google Fonts) — 한국어 폰트

---

## 📄 라이선스

MIT License
