# 27년 해외 비전트립 · 신청 페이지

이 폴더에는 QR로 접속할 수 있는 1페이지 소개·신청 사이트가 들어있습니다.
아래 두 단계만 하면 실제로 배포되고, 신청서가 jcm7163@naver.com으로 자동 도착합니다.

---

## 📌 1단계 · Formspree 연결 (신청 이메일 받기)

1. https://formspree.io 접속 → **Sign up** (jcm7163@naver.com로 가입)
2. 대시보드에서 **New form** 클릭
3. Form name: `비전트립 27 신청서` / 받는 이메일: `jcm7163@naver.com`
4. 생성되면 나오는 form endpoint 주소를 복사합니다.
   예: `https://formspree.io/f/xrgvabcd`
5. `index.html`을 열고 **`YOUR_FORM_ID`** 를 찾아 방금 복사한 ID(`xrgvabcd` 부분)로 바꿉니다.

   찾을 곳:
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
   바꾼 후:
   ```html
   <form action="https://formspree.io/f/xrgvabcd" method="POST">
   ```

6. 무료 플랜은 **월 50건**까지 무료입니다. (17명 모집이니 충분)

---

## 📌 2단계 · GitHub Pages 배포 (QR 공개 URL 만들기)

1. https://github.com 접속 → 로그인 (없으면 가입)
2. 우측 상단 **+** → **New repository**
3. Repository name: `vision-trip` (또는 원하는 이름)
   - Public 선택
   - **Add a README file** 체크 해제
4. **Create repository** 클릭
5. 다음 화면에서 **uploading an existing file** 링크 클릭
6. 이 폴더(`vision-trip-uganda`) 안의 **모든 파일**을 드래그해서 업로드
   - `index.html`
   - `images/` 폴더 전체 (34장)
   - `videos/` 폴더 전체 (3개)
   - `README.md`
7. **Commit changes** 클릭 → 업로드 완료까지 몇 분 대기
8. 저장소 상단의 **Settings** → 왼쪽 **Pages** 클릭
9. **Source** 를 `Deploy from a branch` 로 두고, Branch를 `main` / `/root` 선택 → **Save**
10. 1~2분 후 다음 주소로 접속됩니다:
    ```
    https://<본인아이디>.github.io/vision-trip/
    ```

---

## 📌 3단계 · QR 코드 만들기

접속 URL이 나오면 아래 사이트에서 QR 생성:
- https://qr.naver.com  (네이버 QR)
- https://www.qr-code-generator.com

만든 QR을 인쇄물·주보·현수막에 넣으면 됩니다.

---

## 🖼 사진 · 영상 파일 정리

- `images/` : 34장의 답사 사진 (01~34번)
- `videos/` : 3개의 영상 클립 (video1~3.mp4)

바꾸고 싶은 사진이 있으면 같은 파일명으로 덮어쓰거나, `index.html`의 파일 경로를 수정하면 됩니다.

---

## ✉️ 신청서가 담기는 항목

- 학생 정보: 이름·학년·연락처·이메일
- 보호자 정보: 이름·연락처·참가 동의
- 여권 정보: 번호·유효기간
- 영적 준비: 지원 동기·기도제목

접수되면 `[비전트립 27] 새로운 신청서가 접수되었습니다`라는 제목으로 jcm7163@naver.com에 도착합니다.

---

## 🛠 유지보수 팁

- 모집이 마감되면 `index.html`의 신청 폼 위에 **"모집이 마감되었습니다"** 문구를 추가하면 됩니다.
- 사진을 추가·교체하고 싶으면 `images/` 폴더에 파일을 넣고 GitHub에 다시 업로드하세요.
- 티켓팅 이후 세부 일정(D-day, 훈련 스케줄 등)을 페이지에 추가하고 싶으면 알려주세요.
