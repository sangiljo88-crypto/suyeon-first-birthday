# 수연이 돌잔치 성장기록 페이지 사용 가이드

## 📁 폴더 구조 설정

HTML 파일과 같은 폴더에 다음과 같이 사진을 정리하세요:

```
프로젝트 폴더/
│
├── baby_milestone.html (메인 HTML 파일)
├── cover-photo.jpg (커버 대표 사진)
├── birth-photo.jpg (탄생 사진)
├── background-music.mp3 (배경음악 파일) ⭐ NEW!
│
├── month-0/ (0개월 사진 폴더)
│   ├── photo-1.jpg
│   ├── photo-2.jpg
│   ├── photo-3.jpg
│   ├── photo-4.jpg
│   ├── photo-5.jpg
│   ├── photo-6.jpg
│   ├── photo-7.jpg
│   ├── photo-8.jpg
│   ├── photo-9.jpg
│   └── photo-10.jpg
│
├── month-1/ (1개월 사진 폴더)
│   ├── photo-1.jpg
│   ├── photo-2.jpg
│   └── ... (photo-10.jpg까지)
│
├── month-2/ ~ month-12/ (각 월별 폴더, 위와 동일한 구조)
│
```

**중요**: 각 month-X 폴더에는 photo-1.jpg부터 photo-10.jpg까지 총 10장의 사진을 넣어주세요!

## 🎬 유튜브 영상 추가 방법

1. 유튜브에 영상을 업로드합니다
2. 영상 URL에서 VIDEO_ID를 확인합니다
   - 예: `https://www.youtube.com/watch?v=dQw4w9WgXcQ`
   - VIDEO_ID는 `dQw4w9WgXcQ` 부분입니다

3. HTML 파일을 텍스트 에디터로 열고 다음 부분을 찾습니다:
```html
<iframe 
    src="https://www.youtube.com/embed/VIDEO_ID"
```

4. `VIDEO_ID`를 실제 영상 ID로 교체합니다:
```html
<iframe 
    src="https://www.youtube.com/embed/dQw4w9WgXcQ"
```

## 🎵 배경음악 추가 방법

### 1단계: 음악 파일 준비

1. 원하는 배경음악을 준비합니다 (MP3 형식 권장)
2. 파일 이름을 `background-music.mp3`로 변경합니다
3. HTML 파일과 같은 폴더에 넣습니다

### 2단계: 음악 파일명 확인

만약 다른 이름을 사용하고 싶다면, HTML에서 다음 부분을 찾아서:
```html
<audio id="bgMusic" loop>
    <source src="background-music.mp3" type="audio/mpeg">
```

파일명을 수정합니다:
```html
<audio id="bgMusic" loop>
    <source src="내음악파일.mp3" type="audio/mpeg">
```

### 음악 플레이어 기능

- ✅ **자동 재생 시도** (페이지 로드 시 바로 재생)
- ✅ 재생/일시정지 버튼
- ✅ 볼륨 조절 (PC)
- ✅ 음소거 기능
- ✅ 자동 반복 재생
- ✅ 모바일 최적화

**🔔 자동재생 안내:**
- PC 브라우저: 대부분 자동 재생됩니다
- 모바일: 브라우저 정책상 자동 재생이 차단될 수 있습니다
- 자동 재생 실패 시: 작은 알림이 나타나며, 플레이어의 재생 버튼을 눌러주시면 됩니다

### 음악 추천

돌잔치 페이지에 어울리는 음악:
- 클래식: 슈베르트 '자장가', 모차르트 '아이네 클라이네 나흐트무지크'
- 동요: 편안한 버전의 클래식 동요 모음
- 잔잔한 피아노: 유튜브에서 "Baby music" 또는 "Lullaby" 검색
- 직접 녹음: 부모님이 직접 부르는 노래도 특별해요!

### 음원 다운로드 사이트

**무료 음원 (상업적 이용 가능):**
- [YouTube Audio Library](https://www.youtube.com/audiolibrary)
- [Free Music Archive](https://freemusicarchive.org/)
- [Incompetech](https://incompetech.com/)
- [Bensound](https://www.bensound.com/)

⚠️ **저작권 주의**: 상업적 이용이 가능하고 크레딧 표기가 필요 없는 음원을 선택하세요!

### 음악이 재생 안 될 때

1. **파일 형식 확인**: MP3 파일인지 확인
2. **파일명 확인**: `background-music.mp3`가 맞는지 확인
3. **위치 확인**: HTML 파일과 같은 폴더에 있는지 확인
4. **브라우저 자동재생 정책**: 
   - 페이지 로드 시 자동으로 재생을 시도하지만, 브라우저가 차단할 수 있습니다
   - 특히 모바일에서는 대부분 차단됩니다
   - 이 경우 오른쪽 하단의 ▶️ 버튼을 눌러서 재생하세요
5. **볼륨 확인**: 음소거 상태가 아닌지, 볼륨이 0이 아닌지 확인

💡 **팁**: 
- PC 크롬/엣지에서는 자동재생이 잘 됩니다
- 모바일에서는 사용자가 직접 재생 버튼을 눌러야 하는 경우가 많습니다
- Safari는 특히 자동재생을 엄격하게 차단합니다

### 음악 표시 이름 변경

HTML에서 이 부분을 찾아서:
```html
<div class="music-info" id="musicInfo">배경음악</div>
```

원하는 텍스트로 변경:
```html
<div class="music-info" id="musicInfo">수연이를 위한 노래</div>
```

## 🔥 Firebase 설정 방법 (방명록 기능)

### 1단계: Firebase 프로젝트 생성

1. [Firebase Console](https://console.firebase.google.com/)에 접속
2. "프로젝트 추가" 클릭
3. 프로젝트 이름 입력 (예: "suyeon-birthday")
4. Google 애널리틱스는 선택사항 (필요없으면 비활성화)
5. 프로젝트 생성 완료

### 2단계: 웹 앱 추가

1. Firebase 프로젝트 페이지에서 "웹" 아이콘 클릭 (</>)
2. 앱 닉네임 입력 (예: "돌잔치페이지")
3. "Firebase Hosting 설정" 체크하지 않음
4. "앱 등록" 클릭

### 3단계: 설정 정보 복사

Firebase SDK 설정 화면에서 `firebaseConfig` 객체를 복사합니다:

```javascript
const firebaseConfig = {
  apiKey: "AIzaSy...",
  authDomain: "your-project.firebaseapp.com",
  projectId: "your-project",
  storageBucket: "your-project.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:abc..."
};
```

### 4단계: HTML 파일에 설정 붙여넣기

1. `baby_milestone.html` 파일을 텍스트 에디터로 엽니다
2. 다음 부분을 찾습니다:
```javascript
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
    ...
};
```

3. 위에서 복사한 실제 설정 정보로 **전체를 교체**합니다

### 5단계: Firestore 데이터베이스 설정

1. Firebase Console에서 왼쪽 메뉴 "Firestore Database" 클릭
2. "데이터베이스 만들기" 클릭
3. **"테스트 모드에서 시작"** 선택 (중요!)
4. 위치 선택: `asia-northeast3 (Seoul)` 권장
5. "사용 설정" 클릭

### 6단계: 보안 규칙 설정

1. Firestore Database 페이지에서 "규칙" 탭 클릭
2. 다음 규칙으로 교체:

```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /guestbook/{document} {
      // 읽기는 모두 허용
      allow read: if true;
      // 쓰기는 필드 검증
      allow create: if request.resource.data.keys().hasAll(['name', 'message', 'timestamp'])
                    && request.resource.data.name is string
                    && request.resource.data.message is string
                    && request.resource.data.name.size() > 0
                    && request.resource.data.message.size() > 0
                    && request.resource.data.name.size() <= 50
                    && request.resource.data.message.size() <= 500;
    }
  }
}
```

3. "게시" 클릭

## 🚀 배포 방법 (GitHub + Netlify)

### 1. GitHub에 업로드

1. [GitHub](https://github.com)에서 새 Repository 생성
2. Repository 이름: `suyeon-birthday` (또는 원하는 이름)
3. Public으로 설정
4. 로컬에서 Git 명령어 실행:

```bash
git init
git add .
git commit -m "첫 번째 생일 페이지"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/suyeon-birthday.git
git push -u origin main
```

### 2. Netlify 배포

1. [Netlify](https://www.netlify.com/)에 가입/로그인
2. "Add new site" → "Import an existing project" 클릭
3. "GitHub" 선택
4. Repository 선택 (`suyeon-birthday`)
5. Build settings는 기본값 그대로 둠
6. "Deploy site" 클릭

### 3. 배포 완료!

- Netlify가 자동으로 URL을 생성합니다 (예: `https://suyeon-birthday-abc123.netlify.app`)
- 이 URL로 QR 코드를 만들면 됩니다!

## 📱 QR 코드 만들기

배포된 URL을 받으면:

1. [QR 코드 생성기](https://www.qr-code-generator.com/) 방문
2. URL 입력
3. QR 코드 다운로드
4. 답례품 카드에 인쇄!

## ✏️ 내용 수정하기

HTML 파일을 텍스트 에디터로 열어서 다음을 수정하세요:

- **아이 이름**: `수연이` → 실제 이름
- **날짜**: `2024.11.02` → 실제 생년월일
- **출생 정보**: 시간, 몸무게, 키 수정
- **월별 설명**: 각 개월의 `month-description` 부분 수정
- **감사 메시지**: 하단 감사 인사 수정

## 💡 팁

1. **사진 크기**: 가로 1200px 정도로 리사이즈하면 로딩이 빠릅니다
2. **사진 포맷**: JPG 권장 (용량 작음)
3. **사진이 10장 안 되면**: 부족한 만큼 같은 사진을 복사해서 넣으세요
4. **테스트**: 배포 전에 HTML 파일을 브라우저로 열어서 테스트하세요
5. **방명록 스팸 방지**: Firebase 보안 규칙에서 글자수 제한이 설정되어 있습니다

## ⚠️ 주의사항

- Firebase는 무료 플랜으로도 충분히 사용 가능합니다
- 하루 방문자가 많을 경우 Firebase 무료 한도를 확인하세요
- 개인정보가 포함된 사진은 주의해서 업로드하세요

## 🆘 문제 해결

### 배경음악이 재생되지 않을 때
- 음악 파일이 HTML 파일과 같은 폴더에 있는지 확인
- 파일명이 `background-music.mp3`가 맞는지 확인
- 브라우저 콘솔(F12)을 열어서 오류 확인
- 모바일에서는 수동으로 재생 버튼을 눌러야 함
- 일부 브라우저는 사용자 상호작용 없이는 자동재생을 차단함

### 방명록이 작동하지 않을 때
- 브라우저 콘솔(F12)을 열어서 오류 확인
- Firebase 설정이 제대로 되었는지 확인
- Firestore 규칙이 올바른지 확인

### 슬라이더가 작동하지 않을 때
- 사진 파일명이 정확한지 확인 (photo-1.jpg, photo-2.jpg, ...)
- 폴더명이 정확한지 확인 (month-0, month-1, ...)

### 유튜브 영상이 안 보일 때
- VIDEO_ID가 정확한지 확인
- 유튜브 영상이 "공개" 또는 "일부 공개"로 설정되었는지 확인

---

행복한 돌잔치 되세요! 🎉✨
