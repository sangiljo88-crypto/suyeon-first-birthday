# 🚀 GitHub + Netlify 배포 완벽 가이드

초보자도 따라할 수 있는 단계별 설명!

---

## 📋 필요한 것

- ✅ 준비된 프로젝트 폴더 (사진, 음악 모두 들어있는 상태)
- ✅ GitHub 계정 (없으면 만들기)
- ✅ Netlify 계정 (없으면 만들기)
- ✅ GitHub Desktop 프로그램 (설치할 예정)

---

## 1️⃣ GitHub 계정 만들기

### 계정이 이미 있다면 이 단계는 건너뛰세요!

1. **[GitHub.com](https://github.com)** 접속
2. 오른쪽 상단 **"Sign up"** 클릭
3. 정보 입력:
   - Email 주소
   - Password 설정
   - Username 설정 (예: `kim-sooyeon`)
4. 이메일 인증 완료
5. 로그인!

---

## 2️⃣ GitHub Desktop 설치

GitHub Desktop은 코딩 몰라도 쉽게 파일을 업로드할 수 있는 프로그램입니다!

### 다운로드 및 설치

1. **[GitHub Desktop 다운로드](https://desktop.github.com/)** 접속
2. **"Download for Windows"** 클릭 (Mac이면 Mac용)
3. 다운로드한 파일 실행
4. 설치 완료까지 대기 (1-2분)

### 로그인

1. GitHub Desktop 실행
2. **"Sign in to GitHub.com"** 클릭
3. 브라우저가 열리면 GitHub 계정으로 로그인
4. "Authorize desktop" 클릭
5. GitHub Desktop으로 돌아오기

---

## 3️⃣ 새 Repository 만들기

Repository(저장소)는 파일들을 보관하는 공간입니다!

### GitHub Desktop에서 생성

1. GitHub Desktop에서 **"File"** → **"New repository"** 클릭

2. 정보 입력:
   ```
   Name: suyeon-first-birthday
        (영어로, 공백 없이, 하이픈 사용)
   
   Description: 수연이의 첫 번째 생일 페이지
               (선택사항, 한글 가능)
   
   Local Path: [찾아보기] 클릭해서 내 컴퓨터 위치 선택
               (예: 내문서)
   
   ✅ Initialize this repository with a README 체크
   
   Git Ignore: None
   License: None
   ```

3. **"Create repository"** 클릭

4. 완료! 이제 내 컴퓨터에 빈 폴더가 생성됩니다.

### 생성된 폴더 위치

```
내문서/
└── suyeon-first-birthday/  ⬅️ 여기에 파일을 넣어야 합니다!
    └── README.md (자동 생성됨)
```

---

## 4️⃣ 프로젝트 파일 복사하기

### 준비한 파일들을 GitHub 폴더로 복사

1. **파일 탐색기** 열기

2. 준비한 프로젝트 폴더 열기:
   ```
   수연이돌잔치/
   ├── baby_milestone.html
   ├── cover-photo.jpg
   ├── birth-photo.jpg
   ├── background-music.mp3
   └── month-0/ ~ month-12/
   ```

3. **모든 파일과 폴더 선택** (`Ctrl + A`)

4. **복사** (`Ctrl + C`)

5. 새로 생성된 **GitHub 폴더로 이동**:
   ```
   내문서/suyeon-first-birthday/
   ```

6. **붙여넣기** (`Ctrl + V`)

### 최종 폴더 구조

```
suyeon-first-birthday/
├── README.md              (GitHub가 만든 파일)
├── baby_milestone.html    ⬅️ 복사한 파일들
├── cover-photo.jpg
├── birth-photo.jpg
├── background-music.mp3
├── month-0/
├── month-1/
└── ... (나머지 월별 폴더들)
```

---

## 5️⃣ GitHub에 업로드하기 (Commit & Push)

### GitHub Desktop에서 확인

1. **GitHub Desktop**으로 돌아가기

2. 왼쪽에 **변경된 파일 목록**이 보입니다:
   ```
   ✅ baby_milestone.html
   ✅ cover-photo.jpg
   ✅ birth-photo.jpg
   ✅ background-music.mp3
   ✅ month-0/photo-1.jpg
   ... (모든 파일)
   ```

3. 왼쪽 하단 **"Summary"** 입력:
   ```
   첫 번째 업로드
   ```
   
4. **"Commit to main"** 버튼 클릭
   - 이것은 변경사항을 저장하는 것입니다

5. 상단 **"Push origin"** 버튼 클릭
   - 이것은 인터넷에 업로드하는 것입니다
   - 파일 크기에 따라 1-5분 소요

6. 업로드 완료!

### GitHub.com에서 확인

1. 브라우저에서 **[GitHub.com](https://github.com)** 접속

2. 로그인

3. 오른쪽 상단 프로필 아이콘 클릭 → **"Your repositories"**

4. **"suyeon-first-birthday"** 클릭

5. 모든 파일이 보이면 성공! 🎉

---

## 6️⃣ Netlify 계정 만들기

### 회원가입

1. **[Netlify.com](https://www.netlify.com/)** 접속

2. 오른쪽 상단 **"Sign up"** 클릭

3. **"Sign up with GitHub"** 클릭
   - GitHub 계정으로 간편 가입!

4. "Authorize Netlify" 클릭

5. 이메일 인증 (받은 이메일에서 링크 클릭)

6. 로그인 완료!

---

## 7️⃣ Netlify에 사이트 배포하기

### 새 사이트 만들기

1. Netlify 대시보드에서 **"Add new site"** 클릭

2. **"Import an existing project"** 선택

### GitHub 연결

3. **"Deploy with GitHub"** 클릭

4. "Authorize Netlify" (처음 한 번만)

5. Repository 목록에서 **"suyeon-first-birthday"** 선택
   - 안 보이면: **"Configure the Netlify app on GitHub"** 클릭
   - 그 다음: "Only select repositories" 선택
   - "Select repositories" → "suyeon-first-birthday" 선택
   - "Save" 클릭
   - 다시 Netlify로 돌아와서 Repository 선택

### 배포 설정

6. 설정 확인:
   ```
   Branch to deploy: main
   Base directory: (비워두기)
   Build command: (비워두기)
   Publish directory: (비워두기)
   ```
   
   ⚠️ **중요**: HTML 파일만 있는 정적 사이트이므로 빌드 설정 필요 없음!

7. **"Deploy [사이트명]"** 클릭

### 배포 대기

8. 배포 진행 중... (1-3분 소요)
   - 화면에 로그가 주르륵 나타남
   - 기다리세요!

9. 배포 완료! 🎉
   - **"Site is live"** 또는 녹색 체크마크 표시

---

## 8️⃣ 배포된 사이트 확인

### URL 확인

1. 사이트 대시보드에서 URL을 확인할 수 있습니다:
   ```
   https://random-name-123456.netlify.app
   ```
   
2. URL 클릭해서 사이트 방문!

3. 확인 사항:
   - ✅ 사진이 잘 보이나요?
   - ✅ 슬라이더가 작동하나요?
   - ✅ 음악이 재생되나요?
   - ✅ 유튜브 영상이 보이나요?
   - ✅ 방명록이 작동하나요?

### 도메인 이름 변경 (선택사항)

랜덤한 이름 대신 원하는 이름으로 변경할 수 있어요!

1. 사이트 대시보드에서 **"Site settings"** 클릭

2. **"Change site name"** 클릭

3. 원하는 이름 입력:
   ```
   suyeon-first-birthday
   ```
   
4. **"Save"** 클릭

5. 새 URL:
   ```
   https://suyeon-first-birthday.netlify.app
   ```

---

## 9️⃣ QR 코드 만들기

### QR 코드 생성

1. **[QR Code Generator](https://www.qr-code-generator.com/)** 접속

2. **"URL"** 선택

3. Netlify URL 붙여넣기:
   ```
   https://suyeon-first-birthday.netlify.app
   ```

4. 스타일 선택 (선택사항):
   - 색상 변경
   - 로고 추가 가능

5. **"Download"** 클릭

6. PNG 파일 저장

### QR 코드 사용

- 인쇄해서 답례품 카드에 붙이기
- 크기: 3cm × 3cm 이상 권장

---

## 🔄 나중에 파일 수정하는 법

### 파일 수정 후 다시 업로드

1. **로컬 폴더에서 파일 수정**
   ```
   내문서/suyeon-first-birthday/baby_milestone.html
   ```

2. **GitHub Desktop** 열기

3. 변경된 파일이 자동으로 감지됨

4. Summary 입력:
   ```
   사진 추가 업데이트
   ```

5. **"Commit to main"** 클릭

6. **"Push origin"** 클릭

7. **Netlify가 자동으로 다시 배포**
   - 1-2분 후 변경사항 반영!

---

## ⚠️ 자주 하는 실수

### ❌ 실수 1: Repository 이름에 공백 사용
```
❌ suyeon first birthday
✅ suyeon-first-birthday
```

### ❌ 실수 2: 파일을 잘못된 위치에 복사
```
❌ 내문서/수연이돌잔치/파일들 (GitHub가 추적 못함)
✅ 내문서/suyeon-first-birthday/파일들 (정확!)
```

### ❌ 실수 3: Push를 안 함
- Commit만 하고 Push를 안 하면 GitHub에 업로드 안 됨!
- 반드시 "Push origin" 클릭!

### ❌ 실수 4: 파일명 대소문자
```
❌ Baby_milestone.html
✅ baby_milestone.html
```

---

## 🆘 문제 해결

### 사이트가 안 열려요
1. URL을 정확히 복사했는지 확인
2. Netlify 대시보드에서 "Deploys" 탭 확인
3. 빨간색 오류가 있으면 메시지 확인

### 사진이 안 보여요
1. 파일명 확인 (대소문자, 하이픈)
2. 폴더 구조 확인
3. GitHub에 파일이 제대로 업로드되었는지 확인

### 음악이 안 나와요
1. 파일명이 `background-music.mp3`인지 확인
2. GitHub에 음악 파일이 업로드되었는지 확인
3. 모바일에서는 재생 버튼을 눌러야 함

### 방명록이 안 돼요
1. Firebase Firestore가 활성화되었는지 확인
2. 보안 규칙이 올바른지 확인
3. 브라우저 콘솔(F12)에서 오류 확인

---

## 📊 전체 프로세스 요약

```
컴퓨터에 파일 준비
        ↓
GitHub Desktop 설치
        ↓
Repository 생성
        ↓
파일 복사
        ↓
Commit & Push (GitHub 업로드)
        ↓
Netlify 가입
        ↓
GitHub 연결
        ↓
사이트 배포
        ↓
URL 확인
        ↓
QR 코드 생성
        ↓
완료! 🎉
```

---

## 💰 비용

- **GitHub**: 무료 ✅
- **Netlify**: 무료 ✅
- **Firebase**: 무료 (Spark 플랜) ✅

모두 무료로 사용 가능합니다!

### Netlify 무료 플랜 한도

- 대역폭: 월 100GB
- 빌드 시간: 월 300분
- 사이트 수: 무제한

돌잔치 페이지 하나는 무료 플랜으로 충분합니다! 👍

---

## 🎉 완료!

이제 QR 코드를 답례품에 넣고 손님들과 공유하세요!

```
📱 손님이 QR 코드 스캔
        ↓
🌐 웹사이트 열림
        ↓
🎵 음악 자동 재생
        ↓
📸 사진 감상
        ↓
💌 방명록 작성
        ↓
❤️ 감동!
```

---

## 📞 도움말

- GitHub 도움말: [docs.github.com](https://docs.github.com)
- Netlify 도움말: [docs.netlify.com](https://docs.netlify.com)
- Firebase 도움말: [firebase.google.com/docs](https://firebase.google.com/docs)

화이팅! 🎈
