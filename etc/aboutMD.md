* header 만들기
<img src="https://capsule-render.vercel.app/api?type=모양&color=색상코드&height=높이&section=header&text=텍스트&fontSize=텍스트크기" />

* footer 만들기
<img src="https://capsule-render.vercel.app/api?type=모양&color=색상코드&height=높이&section=footer&text=텍스트&fontSize=텍스트크기" />

- type 종류
wave: default / egg / shark / slice / rect / soft / rounded / cylinder / waving / transparent
- 참고사항
띄어쓰기는 %20으로 나타내기, 컬러코는 # 빼고 작성하기

* widgets 추가하기
- 사용한 언어 비율 나타내는 위젯 추가하기
1. [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=깃허브 아이디)](https://github.com/anuraghazra/github-readme-stats)
2. 	<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=본인아이디&layout=compact">
- 본인의 깃허브에 대한 평판 나타내는 위젯
[![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=깃허브아이디)](https://github.com/anuraghazra/github-readme-stats)
![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=깃허브아이디&hide=contribs,prs&show_icons=true&theme=테마)

* badge 만들기
- 이모지 링크
1. https://simpleicons.org/
2. https://gist.github.com/rxaviers/7360908 링크 걸고싶으면 <a href="url"><h3>:muscle: Problem Solving</h3></a> 이런식으로!
- 프레임워크 뱃지 링크
1. https://github.com/Envoy-VC/awesome-badges
2. 한국어를 잘 채워넣으면 됨
<img src="https://img.shields.io/badge/아이콘내용-바탕색?style=flat&logo=로고이름&logoColor=white"/>
- 첨부 예시
![js](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=JavaScript&logoColor=white)

* 타이핑 애니메이션 넣기
- 참고할 링크
https://readme-typing-svg.demolab.com/demo/
- 첨부 예시
[![Typing SVG](https://readme-typing-svg.demolab.com/?lines=첫번째+줄+의+텍스트;두번째+줄+의+텍스트)](https://git.io/typing-svg)

* 토글 넣기
- html의 detail과 summary를 이용하여 토글 만들기
<details>
    <summary>
        토글 제목
    </summary>
    토글 안 내용
</details>

* 제목 분류하기
#갯 수가 h태그 갯 수랑 동일함
#h1 ###h3 이런식

* 중앙 정렬 하고 싶을 때
제일 처음에 <div align=center> 제일 마지막에 </div>