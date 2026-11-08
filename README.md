# 🚗 도로관리팀 다중 차량 운행일지 (PWA 모바일 앱)

여러 대의 점검·순찰·보수 차량을 개별 등록하고, 차량마다 **운행 시작(시작 키로수·출발시간)**과 **운행 종료(종료 키로수·종료시간·주행거리 자동 계산)**를 기록 및 엑셀(CSV)로 내보낼 수 있는 모바일 웹앱(PWA)입니다.

---

## 📦 포함된 파일 구성
```text
driving-log-pwa/
├── index.html       # 메인 어플리케이션 실행 파일
├── manifest.json    # 스마트폰 홈 화면 앱 설치용 매니페스트 설정
├── sw.js            # 오프라인 실행 지원 서비스 워커
├── .nojekyll        # GitHub Pages 즉시 배포 설정 파일
├── icons/
│   ├── icon-192.png # 앱 아이콘 (192x192)
│   └── icon-512.png # 고해상도 앱 아이콘 / 스플래시 (512x512)
└── README.md        # GitHub 배포 및 스마트폰 앱 설치 설명서
```

---

## 🚀 1단계: GitHub에 업로드하기 (코딩 프로그램 없이 웹에서 1분 완성)

1. [GitHub](https://github.com/)에 로그인한 뒤 우측 상단 **`+` 버튼 → `New repository`**를 클릭합니다.
2. **Repository name**에 원하는 이름(예: `driving-log`)을 입력합니다.
3. 공개 범위를 **`Public`**으로 선택하고 맨 아래 **`Create repository`**를 클릭합니다.
4. 생성된 화면에서 **`uploading an existing file`** 링크(또는 `Add file` → `Upload files`)를 클릭합니다.
5. 이 압축파일(`driving-log-pwa.zip`)의 압축을 풀고, 폴더 안에 있는 파일 전체(`index.html`, `manifest.json`, `sw.js`, `.nojekyll`, `icons` 폴더, `README.md`)를 드래그하여 업로드 창에 끌어다 놓습니다.
   - ⚠️ **주의**: `driving-log-pwa` 바깥 폴더째로 넣지 마시고, **`index.html`이 가장 바깥(루트)에 보이도록** 내부 파일들을 드래그해 주세요.
6. 하단 초록색 **`Commit changes`** 버튼을 누르면 업로드가 완료됩니다.

---

## 🌐 2단계: GitHub Pages로 무료 앱 주소 만들기

1. 방금 올린 GitHub 저장소 상단 메뉴에서 **`Settings`**(톱니바퀴)를 클릭합니다.
2. 왼쪽 사이드바 메뉴에서 **`Pages`**를 클릭합니다.
3. **Build and deployment** 아래의 **Branch** 항목에서 `None`을 누르고 **`main`** (또는 `master`)을 선택한 뒤 옆의 **`Save`** 버튼을 클릭합니다.
4. 약 1~2분 뒤 페이지를 새로고침하면 상단에 아래와 같은 **내 전용 앱 주소**가 나타납니다:
   - `https://내깃허브아이디.github.io/driving-log/`

---

## 📱 3단계: 스마트폰에 진짜 어플처럼 설치하기

발급된 `https://내깃허브아이디.github.io/driving-log/` 주소를 스마트폰으로 열면 주소창이 없는 **독립된 어플(PWA)**로 설치할 수 있습니다.

### 🤖 안드로이드 (갤럭시 등 - Chrome 브라우저)
1. 크롬(Chrome) 앱으로 배포된 주소에 접속합니다.
2. 화면 우측 상단 **[앱설치/GitHub]** 버튼을 눌러 **[지금 앱 설치]**를 누르거나, 브라우저 우측 상단 **점 3개 메뉴(⋮) → [앱 설치]** (또는 **[홈 화면에 추가]**)를 누릅니다.
3. 휴대폰 바탕화면(앱스 화면)에 **차량운행일지** 아이콘이 생성되며, 일반 어플처럼 전체화면으로 실행됩니다.

### 🍎 아이폰 (iOS - Safari 브라우저)
1. 사파리(Safari) 앱으로 배포된 주소에 접속합니다.
2. 하단 중앙의 **공유 버튼(네모에서 화살표가 위로 나온 아이콘)**을 누릅니다.
3. 메뉴를 내려 **[홈 화면에 추가]**를 누르고 우측 상단 **[추가]**를 누릅니다.

---

## 📦 (선택) 안드로이드 설치 파일(.APK)로 추출하고 싶을 때

카카오톡이나 파일로 동료들에게 `.apk` 설치 파일을 직접 배포하고 싶다면 무료 도구인 **PWABuilder**를 사용하면 1분 만에 변환됩니다.

1. [PWABuilder (https://www.pwabuilder.com)](https://www.pwabuilder.com) 사이트에 접속합니다.
2. 입력창에 내 GitHub Pages 주소(`https://내깃허브아이디.github.io/driving-log/`)를 붙여넣고 **`Start`**를 누릅니다.
3. 분석이 끝나면 **`Package for stores`** → **Android** 항목의 **`Generate Package`** → **`Download Package`**를 누르면 안드로이드폰에 바로 설치 가능한 **`.apk` 파일**이 다운로드됩니다.
