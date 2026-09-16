# lavakangjun.github.io

GitHub Pages 사용자 사이트. Pico 앱 소개 페이지와 `app-ads.txt`를 올려 둔다.

## 왜 사용자 사이트인가

`app-ads.txt`는 **도메인 루트**에 있어야 광고 구매자가 찾는다.
프로젝트 사이트(`lavakangjun.github.io/Pico/`)로 만들면 `/Pico/app-ads.txt`가 되어
인식되지 않는다. 그래서 저장소 이름이 반드시 `lavakangjun.github.io`여야 한다.

## 파일

| 파일 | 용도 |
|---|---|
| `index.html` | 앱 소개 페이지 |
| `app-ads.txt` | AdMob 인벤토리 판매 권한 선언 |
| `.nojekyll` | Jekyll 처리를 건너뛰고 파일을 그대로 서빙 |

## app-ads.txt

```
google.com, pub-4602481899762111, DIRECT, f08c47fec0942fa0
```

`pub-4602481899762111`은 AdMob 퍼블리셔 ID다. 앱 ID
`ca-app-pub-4602481899762111~4950998751`의 가운데 숫자와 같다.
`f08c47fec0942fa0`은 구글의 인증기관 ID로, 모든 퍼블리셔가 쓰는 고정값이다.

## 인증 순서

AdMob은 **앱스토어 등록 정보에 적힌 웹사이트**를 읽어 그 도메인의 `app-ads.txt`를
크롤링한다. 그래서 앱이 스토어에 올라가기 전에는 인증이 끝나지 않는다.

1. 이 저장소를 `lavakangjun.github.io` 이름으로 GitHub에 올린다
2. 저장소 Settings → Pages에서 `main` 브랜치를 소스로 지정한다
3. `https://lavakangjun.github.io/app-ads.txt`가 열리는지 확인한다
4. 앱스토어 등록 정보의 마케팅 URL을 `https://lavakangjun.github.io`로 적는다
5. AdMob 콘솔 → 앱 → app-ads.txt 상태가 "인증됨"으로 바뀌는지 본다 (최대 24시간)

## 남은 일

- [ ] 개인정보 처리방침 페이지 (`privacy.html`) — 앱스토어 심사에 필요하다.
      AdMob과 Crashlytics가 데이터를 수집하므로 그 내용이 들어가야 한다.
- [ ] 문의 이메일을 `index.html` 푸터에 적는다
- [ ] 출시 후 `index.html`의 App Store 링크를 실제 주소로 바꾼다
