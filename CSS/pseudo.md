pseudo-class와 pseudo-element를 이용하여 클래스 일부 수정 가능!

<input>과 같은 태그의 기본 디자인 값도 shadow DOM의 pseudo를 사용하면 바꿀 수 있다.

-webkit-은 크롬, 사파리, 앳지에서만 적용되는 스타일. 브라우저마다 쉐도우 돔은 살찍씩 다름

예제: <input>태그에 스타일을 주고 싶다면>
<label>태그에 스타일을 주고, <input>의 스타일엔 appearance:none을 준다
예제2: <input placeholder="hello">
input:-webkit-input-placeholder{
    color: blue;
}
예제3 <input type="range">
개발자 도구 속, input의 user agent stylesheet속 태그를 확인할 수 있음
input[type="range" i]::-webkit-slider-thumb{
    ~~
}여기서 위에를 아래처럼 수정한다
input[type=range]::-webkit-slider-thumb{
    appearance: none;
    background:red;
    width: 50px;
    height: 50px;
}