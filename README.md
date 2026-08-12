# colophonlabs.kr

콜로폰랩스 공개 사이트. 순수 HTML만 올린다 — **스크립트·쿠키·외부 글꼴/이미지 요청이 없다**
(개인정보처리방침에 그렇게 적었으므로 실제로도 그렇게 유지한다).

## 구조

| 경로 | 용도 |
|---|---|
| `index.html` | **회사 소개** — 콜로폰랩스가 무엇을 만드는지 + 제품 목록 |
| `galpi/index.html` | **성경갈피 소개** — App Store Connect ▸ **마케팅 URL** |
| `galpi/features.html` | 자세한 소개 — 실제 화면 11장면 |
| `galpi/support.html` | 지원 — App Store Connect ▸ **지원 URL** |
| `galpi/privacy.html` | 개인정보처리방침 — App Store Connect ▸ **앱 개인정보 보호 ▸ 방침 URL** |
| `galpi/shots/*.jpg` | 소개용 화면(아이패드 캡처를 폭 720으로 줄인 것) |
| `privacy.html` · `support.html` | **옛 주소 스텁** — 지우지 말 것(↓) |

### ⚠️ 루트의 `privacy.html`·`support.html`을 지우지 않는다

앱 1.0 빌드에 **루트 주소가 컴파일돼 들어가** 있고, App Store Connect에도 그 주소가 등록된 적이 있다.
이미 나간 빌드의 ‘개인정보 처리방침’·‘지원’ 링크가 그 주소를 열기 때문에,
두 파일은 `/galpi/…`로 보내는 리디렉션 스텁으로 **영구히 남긴다.**
(GitHub Pages에는 서버 리디렉션이 없어 `meta refresh` + `canonical`로 처리한다.)

## 관리 규칙

- 링크는 모두 **상대 경로**다 — 프로젝트 페이지(`/galpi-site/`)와 사용자 도메인 어디에 올려도 동작한다.
- 앱 안의 같은 내용(`PrivacyView`·FAQ·`HelpInfoView.Site`)과 **문구·주소를 함께 고친다.** 한쪽만 고치지 않는다.
  앱 저장소는 비공개(`colophonlabs/galpi`).
- 개역개정 저작권 표기 문구는 대한성서공회가 지정한 문장이다. **한 글자도 바꾸지 않는다.**
- 화면 캡처를 갱신할 때: 앱 저장소의 `APP/ios/screenshots/ipad13/*.png`를 폭 720 JPEG로 줄여
  `galpi/shots/`에 같은 이름으로 덮어쓴다.
