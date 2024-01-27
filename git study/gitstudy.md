CLI: command line interface 명령어를 직접 타이핑하는 인터페이스
GUI: graphic user interface 버튼을 클릭하여 깃을 다루는 인터페이스

git: 버전관리 소프트웨어
버전관리: 코딩할 때 원하는 시점마다 버전을 만들어 자유롭게 수정하게 해주는 것. 내가 만든 버전 뿐만 아니라 동료가 만든 버전으로 이동할 수 있고, 동료와 내 버전을 비교해서 최신본으로 코드를 업데이트 할 수 있음

깃 초기화를 하면 .git이라는 숨겨진 폴더(로컬 저장소)가 만들어진다. 로컬 저장소에 만든 버전 정보, 원격 저장소 주소 등이 저장

* 완전 초기 설정
1) homebrew 설치
2) 이름을 master에서 main으로 바꿔주는 것인데 요즘 유행
git config --global init.defaultBranch main
3) git의 기본 에디터가 Vim 말고 VSCode로 변경
git config --global core.editor "code --wait"
4) git user setting하는 방법
git config --global user.email "plumxeun@gmail.com"
git config --global user.name "chloe_choi"

* 깃 명령어 1탄
1) git init
작업 폴더에 깃 쓰고싶으면 쓰는 것. 시작 시 깃이 감시 시작
2) git add . / git add 파일 명
버전 기록할 파일 고르는 명령어. "."은 전체 파일 스테이징하는 명령어
3) git commit -m "메세지"
기록 명령어. 영구적 버전 생성 완료
[git add와 git commit 사이의 상태는 staging area라고 부름, commit된 버전은 repository에 저장]
4) git status
어떤 파일들을 스태이징 해놨는지,어떤 파일들이 수정됐는지 확인가능

* branch 기능
HEAD는 내 위치
1) git branch 브랜치 명
브랜치 하나 생성해줌
2) git switch 브랜치명
브랜치 명으로 브랜치로 이동, 브랜치 스위치 시 커밋된 내용이 이관되지 않는 독립된 브랜치로 유지
3) git merge 브랜치명
깃 스위치해서 메인으로 이동한 뒤, 머지하면 합쳐짐
4) git branch -d 브랜치명
브랜치는 머지해도 남아있음 머지 완료된 브랜치는 삭제
5) git branch -D 브랜치명
머지 안한 브랜치 삭제

* git merge 방식
case 1. 3-way merge: 각 브랜치에 신규 commit이 있는 경우(가장 일반적인 방법)
case 2. fast-forward merge: 기준 브랜치에 신규 commit이 없는 경우 -> 자동으로 commit하는 브랜치가 main이 됨 (싫으면 git merge --no-ff 브랜치명 설정하기)
case 3. git rebase & merge: rebase & fast-forward merge인데 fast-forward 머지랑 비슷함
case 4. squah & merge: "git merge --squash 새브랜치명" 사이드 브랜치 내용은 출력은 안되면서 반영은 되면서 깃 그래프로는 커밋 역사 순간 이동해줌
안중요한 브랜치는 squash feature/develop 브랜치는 3-way 머지

* git rebase
간단하고 짦은 브랜치들에 쓰면 깔끔해져서 많이 씀. 단점으로 conflict 많이남
일반 merge를 하고 싶으면 1.중심 브랜치 이동(git switch main) 2. git merge 새로운 브랜치명
rebase & merge 하고 싶으면 1.새로운 브랜치로 이동(git switch 새로운 브랜치) 2.git rebase 중심브랜치명

* git 되돌리기
1) 파일 복구하는 법 "git restore 파일명" / 특정 커민 시점으로 파일을 복구하는 법 "git restore --source 커밋아이디" / git restore --staged 파일명
2) 커밋 취소하는 법 "git revert 커밋아이디" => 에디터나 vim 뜸 커밋 메세지 적고 커밋하면 커밋아이디의 내용 없어짐 / 최근 커밋 취소 "git revert HEAD"
3) 과거로 모든걸 되돌리기 "git reset --hard 커밋아이디" / "git reset --soft 커밋아이디" 리셋인데 변동사항 지우지 않고 staging / "git reset --mixed 커밋아이디" 변동사항 지우지 말고 unstaging

* conflict 해결법
컴플릭트난 파일 가서 원하는 코드만 남기고 수정해주고 깃애드 커밋 뿅뿅 (수동으로 해야함)


* 쓸일 적은 명령어들
) git log
커밋한 내역들을 쭉 확인 가능
참고로 git log --all --oneline --graph 옵션 넣으면 그래프로 그려줌!
입력 후에 vim켜지니까 j,k로 위아래 스크롤하고 q키 눌러서 종료하기
) git restore
스테이징된 파일을 취소하는 명령어
)git diff / git difftool
최근 commit이랑 현재 파일 사이의 차이점 보여줌 diff는 에러가 많아서 별로고 difftool이 시각적으로 훨씬 나음
(vim 뜨는데 hjkl 방향키로 잘 움직이긔 ":q"나 ":qa"하면 종료 뿅)
git difftool 커밋아이디 (아이디 2개까지 입력 가능)
이렇게 치면 잘 보여줌 근데 깃 그래프가 젤루 낫다




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
