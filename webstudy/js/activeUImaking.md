* 동적 UI 만들기
1. html, css로 미리 ui 디자인 해놓고 필요하면 평소엔 숨기기
2. 버튼을 누르는 등의 action이 들어가면 ui가 보여지도록 자바스크립트 코드 짜기

예시) alert 박스 띄우기
<div class="alert" id="alert">
<button onclick="document.getElementById('alert').style.display = 'block';"> 버튼 </button>
</div>

* 자바스크립트 function 문법
1. function 키워드 쓰고 소괄호, 중괄호 붙이기
2. 소괄호 왼쪽에 작명하기
3. 긴 코드를 중괄호에 담기

function(){
    긴 코드
}

예시) alert여는 코드 function으로 축약하기
<button onclick="alertOpen()">aler open btn</button>
<script>
    function alertOpen(){
        document.getElementById('alert').style.display = 'block';
    }
</script>

* 자주 겪는 에러들
1. js 코드는 밑에 짜야함 -> js가 html을 조작하는 것이기 때문에 html이 위에 와야함
2. 셀렉터나 메소드, id 오타 에러
에러나면 console 열기
-> cannot read properties of null 뜨면 id 이름이 잘못됐다는 뜻
-> ~~is not a function은 함수명이 잘못됐다는 뜻

* function에 사용할 param 문법
예시1)
function alertOpen(param){
    document.getElementById('alert').style.display = param;
}
alertOpen('none');
alertOpen('block');

예시2)
function plus(){
    2 + 1
}
function plus2(){
    2 + 2
}
function plus3(){
    2 + 3
}
이거를 파라미터로
function plus(param){
    2 + param
}
plus(1);
plus(2);
plus(3);

* getElementByClassName 셀렉터
id말고 class 명으로 찾는 셀렉터
document.getElementByClassName('title1')[0].innerHTML = '안녕';
title1클래스를 가진 div들 중에서 첫 태크 내용이 '안녕'으로 바뀜
이 외에도 getElementByTagName이나, getElementByName도 있지만 class랑 id를 많이 씀

* EventListener
document.getElementById('clicker').addEventListener('click', function(){
    실행할 함수
})
아이디가 clicker인 요소를 클릭하면 실행할 함수를 클릭해주세욥

- 만약 id를 쓰는 요소와 클릭될 요소가 다른 경우
<div class="alertBox" id="alert"><button id="close">close</button></div>
document.getElementById('close').addEventListener('click', function(){
    document.getElementById('alert').style.display = 'none'
});

* event 예시들
'click', 'mouseover', 'scroll', 'keydown' 등 수 십가지 있음
https://developer.mozilla.org/en-US/docs/Web/Events

* 콜백함수
파라미터로 함수가 들어가는 것을 콜백함수라고 함.
순차적으로 실행하고 싶을 때 많이 보이는 함수 형태, 함수 안에 함수 형태를 뜻함