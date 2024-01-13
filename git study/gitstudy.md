CLI: command line interface 명령어를 직접 타이핑하는 인터페이스
GUI: graphic user interface 버튼을 클릭하여 깃을 다루는 인터페이스

git: 버전관리 소프트웨어
버전관리: 코딩할 때 원하는 시점마다 버전을 만들어 자유롭게 수정하게 해주는 것. 내가 만든 버전 뿐만 아니라 동료가 만든 버전으로 이동할 수 있고, 동료와 내 버전을 비교해서 최신본으로 코드를 업데이트 할 수 있음

깃 초기화를 하면 .git이라는 숨겨진 폴더(로컬 저장소)가 만들어진다. 로컬 저장소에 만든 버전 정보, 원격 저장소 주소 등이 저장

*완전 초기 설정
1) homebrew 설치
2) 이름을 master에서 main으로 바꿔주는 것인데 요즘 유행
git config --global init.defaultBranch main
3) git의 기본 에디터가 Vim 말고 VSCode로 변경
git config --global core.editor "code --wait"
4) git user setting하는 방법
git config --global user.email "plumxeun@gmail.com"
git config --global user.name "chloe_choi"

* 깃 초기 설정
1) git init
작업 폴더에 깃 쓰고싶으면 쓰는 것. 시작 시 깃이 감시 시작
git init 경로명: 컴퓨터 프로젝트 폴더에 git을 쓸것을 명령, 원하는 폴더에서 깃 초기화 하면 그때부터 사용 가능
git status: 깃 상태 확인
git log: 로그 확인
git diff: 커밋 비교

git remote: 원격 저장소 별칭 확인
git remote -v: 원격 저장소 별칭과 URL 확인
git remote add: 원격 저장소와 연결
git remote rm: 원격 서버 삭제

git add 변경한 파일 중 올리길 원하는 것만 선택
git commit -m "first commit" 선택한 파일들을 한 파일로 만들고 설명 적어주기
git log 생성한 커밋 보기

git config --global user.name "Seungeun Choi":깃 사용자 등록
git config --global user.email plumxeun@gmail.com: 깃 사용자 등록

git remote add origin http://gitgub.com: 원격 저장소 깃허브에서 만들고 커밋 푸시하기

git clone 원격 저장소URL 새폴더 이름: 깃허브 저장소 복제 (https://github.com/아이디/이름.git . 점 찍어 줘야 현재 폴더에 생성, 안찍으면 새폴더 생성)
git pull 또는 git fetch: 커밋 가져오기
git push 원격저장소별칭 브랜치 이름: 커밋 전송하기

git branch: 현재 브랜치 확인
git branch 브랜치 이름: 브랜치 생성
git checkout 브랜치 이름: 브랜치 이동

git stash: 스태시 저장
git stash pop: 스태시 읽기

git merge 브랜치 이름: 브랜치 이름
git rebase 옵션 커밋id: 브랜치 이름
git reset: 리셋
git revert: 리버트 취소 커밋

git tag: 태그 관리
git push 원격저장소별칭 태그이름: 태그 전송

git으로 추적 가능한 파일의 4가지 상태
untracked 추적 안됨
tracked 수정 없음, 수정함, 스테이지됨
작업 공간에 있는 "수정함", "추적 안됨" 파일을 스테이지에 올려 "스테이지됨"
커밋하면 "수정없음" 상태로 돌아가서 다시 파일 수정할 수 있다.
