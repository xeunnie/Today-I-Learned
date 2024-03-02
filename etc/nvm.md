참고(https://funveloper.tistory.com/203) / https://velog.io/@mayinjanuary/NVM-%EC%9D%B4%EB%9E%80-%EB%85%B8%EB%93%9CNode.js-%EB%B2%84%EC%A0%84-%EA%B4%80%EB%A6%AC%ED%95%98%EB%8A%94-%EB%B2%95

* nvm
node version manager로 node.js를 설치하고 관리하는 기능을 가짐

1. 설치
1) mkdir ~/.nvm
2) ~/.zshrc 파일을 열고, 아래 내용을 작성하기
 export NVM_DIR="$HOME/.nvm"
[ -s "$HOMEBREW_PREFIX/opt/nvm/nvm.sh" ] && \. "$HOMEBREW_PREFIX/opt/nvm/nvm.sh" # This loads nvm
[ -s "$HOMEBREW_PREFIX/opt/nvm/etc/bash_completion.d/nvm" ] && \. "$HOMEBREW_PREFIX/opt/nvm/etc/bash_completion.d/nvm" # This loads nvm bash_completion
3) brew install nvm
4) nvm -v 설치된 버전 확인
5) nvm ls-remote이나 nvm list available 설치된 버전 목록 확인