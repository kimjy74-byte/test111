[README_GITHUB.md](https://github.com/user-attachments/files/30569271/README_GITHUB.md)
# 🐱 GitHub Pages 웹 중계 설정 및 404 에러 해결 가이드

업무망 사내 방화벽에서 `*.trycloudflare.com` 주소가 차단된 경우, **GitHub Pages**를 무료 웹 중계 서버로 활용하여 차단 없이 사진을 수신할 수 있습니다.

---

## 🚨 404 Error (Page Not Found) 발생 원인 및 1분 해결법

배포 사이트(`https://kimjy74-byte.github.io/test111/`) 접속 시 404 에러가 나는 이유는 다음 2가지 중 하나입니다.

### 1️⃣ 원인 A: GitHub 저장소 루트(최상위)에 `index.html` 파일이 없음
* **해결법**: 
  1. 본 프로그램의 `c:\자료실\github-relay\index.html` 파일의 전체 내용을 복사합니다.
  2. GitHub의 `test111` 저장소(Repository) 페이지로 이동합니다.
  3. **[Add file]** ➔ **[Create new file]** 클릭 후 파일 이름을 **`index.html`**로 입력합니다.
  4. 복사한 코드 내용을 붙여넣고 **[Commit changes...]** 버튼을 누릅니다.

---

### 2️⃣ 원인 B: GitHub Pages 기능이 활성화되지 않음
* **해결법**:
  1. GitHub의 `test111` 저장소 상단 메뉴에서 **[Settings]** 탭으로 들어갑니다.
  2. 좌측 메뉴에서 **[Pages]**를 클릭합니다.
  3. **Build and deployment** 항목 아래 **Source**를 **`Deploy from a branch`**로 선택합니다.
  4. **Branch**를 **`main`** (또는 `master`), 폴더를 **`/ (root)`**로 선택한 후 **[Save]**를 클릭합니다.
  5. 1~2분 후 페이지를 새로고침하면 `https://kimjy74-byte.github.io/test111/` 주소가 정상 동작합니다!

---

## 📱 배포 후 수신기 사용법

1. PC에서 `start_server.bat` 실행 (`http://localhost:8080` 오픈)
2. 대시보드 좌측 상단 **`🐱 GitHub Pages (웹중계)`** 탭 선택 (기본 주소 `https://kimjy74-byte.github.io/test111` 자동 적용)
3. 스마트폰으로 화면의 QR 코드를 스캔하고 핀코드 전송
4. 사진을 선택 후 전송하면, 사내 망 차단 없이 PC의 사진 폴더(`C:\Users\kimjy\Pictures`)에 자동 수신됩니다!
