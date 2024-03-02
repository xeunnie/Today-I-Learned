* 깃페이지
깃허브 저장소의 내용을 웹페이지로 호스팅해주는 서비스, 레포지토리에 올린 소스를 직접 웹 페이지에 보여줌, 웹 서버를 호스팅하는 것도 가능함

https://xeunnie.github.io
이 url로 나오는데 최대 저장 용량은 1기가라 큰 프로젝트는 불가능함
repository명을 “userName.github.io” 형식이 아닌 자유형식으로 지정하되, 별도의 GitHubpages 활성화 설정을 해주면 “userName.github.io/repoName”형식으로 호스팅이 가능

* 추가 페이지 만들기
  일단 레포지토리 셋팅에서 브랜치를 main으로 저장해주면 몇 분 뒤 deploy된 페이지가 올라온다. 그 곳에 올리면 된다

  바로 바로 depoly 하고 싶은 경우 npm i gh-pages 후 package.json 파일에서 명령어 부분을 수정해줘야 한다. 홈페이지 추가랑, deploy, build 명령어 추가!

* 깃 페이지에 이미지가 안뜰 때 경로를 수정하면 된다.
  https://velog.io/@yoosion030/github-page-%ED%8C%8C%EC%9D%BC%EA%B2%BD%EB%A1%9C
