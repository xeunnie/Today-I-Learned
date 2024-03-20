# PWA
- 모바일 바탕화면 설치 가능
상단 URL바가 제거된 크롬 브라우저로 앱과 유사한 모습을 가진 웹
- 오프라인 동작
sevice-worker.js파일과 브라우저 캐시가 있으면 가능
- 설치 과정 간단
간단  팝업정도의 설치 유도 가능

* 만드는 방법
1. 파일 2개에 사이트 로컬경로가 있으면 브라우저가 PWA로 인식함(HTTPS 사이트여야함)
manifest.json과 service-worker.js 라는 이름의 파일 두개 필요
manifest는 yarn build하면 자동으로 만들어줌
2. service-worker.js 만드는 법
```
npx create-react-app 프로젝트명 --template cra-template-pwa
```
없으면 다시 만들어야함 그리고 index.js 파일 속
```javascript
serviceWorkerRegistration.unregister(); //이 부분을
serviceWorkerRegistration.register(); //이렇게 수정하기
```
