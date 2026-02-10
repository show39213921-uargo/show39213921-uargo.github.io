# u-argo.com 법적 문서 (GitHub Pages용)

Google Play 정책 준수를 위한 웹 페이지입니다.

## 사용 방법

이 폴더의 **HTML 파일**과 **assets** 폴더를 **show39213921-uargo.github.io** 저장소 **루트**에 복사해 두세요.

- `index.html` — Dreamshare(꿈의나라) 랜딩 페이지  
- `privacy.html` — 개인정보처리방침  
- `terms.html` — 서비스 이용약관  
- `delete-account.html` — 계정 삭제 요청  
- `assets/` — 로고·스크린샷 이미지 (logo.png, screen1.png 등, `assets/README.md` 참고)
- `.well-known/assetlinks.json` — Android 앱 연결용 Digital Asset Links (Google 검색·App Links 인정용)
- `robots.txt` — 크롤러 허용 규칙 (Google 서치콘솔 색인용)
- `sitemap.xml` — 색인할 URL 목록 (서치콘솔에서 참조)

배포 후 예시 URL (GitHub Pages 기본 도메인):

- `https://show39213921-uargo.github.io/privacy.html`
- `https://show39213921-uargo.github.io/terms.html`
- `https://show39213921-uargo.github.io/delete-account.html`

u-argo.com 도메인을 GitHub Pages에 연결했다면 `https://u-argo.com/privacy.html` 등으로 접근할 수 있습니다.

## 수정 시 참고

- **index.html (SEO)**: 검색·크롤링용 canonical, Open Graph, Twitter Card URL이 `https://u-argo.com/`로 되어 있습니다. GitHub Pages만 쓸 경우 `index.html`에서 해당 URL을 실제 배포 주소(예: `https://show39213921-uargo.github.io/`)로 바꿔주세요. `rel="alternate" android-app://...` 로 앱 패키지와 연결해 두었습니다.
- **robots.txt / sitemap.xml**: `Sitemap` URL이 `https://u-argo.com/sitemap.xml`로 되어 있습니다. GitHub Pages만 쓸 경우 두 파일에서 `u-argo.com`을 실제 도메인으로 바꿔주세요.
- **.well-known/assetlinks.json**: 패키지 `com.dreamshare.uragoai`와 현재 릴리즈 키스토어 SHA-256 지문으로 작성되어 있습니다. 서명 키를 바꾸면 `keytool -list -v -keystore ...` 로 새 지문을 구한 뒤 이 파일의 `sha256_cert_fingerprints`를 수정해야 합니다. 배포 시 `https://u-argo.com/.well-known/assetlinks.json` 에서 JSON이 보이도록 루트에 `.well-known` 폴더를 함께 올리세요.
- **delete-account.html**: 이메일은 `uargoofficial@gmail.com`으로 설정되어 있습니다. Google 폼 링크(`https://forms.gle/YOUR_GOOGLE_FORM_ID`)는 실제 폼 URL로 교체하세요.
- **privacy.html**: Notion에 있는 개인정보처리방침 원문이 있다면 해당 내용으로 섹션을 보완·대체할 수 있습니다.
- 시행일·최종 수정일은 각 문서 상단의 meta 영역에서 수정하세요.
