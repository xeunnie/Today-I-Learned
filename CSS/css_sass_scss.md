* 정의
- css(cascading style sheets): 종속형 시트
- sass(syntactically awesome style sheets)
- scss(sassy scss)
아래 둘은 대충 더 멋진 CSS들

* 약간의 문법 차이가 있지만 비슷
- SCSS: 좀 더 범용적으로 사용가능, CSS의 호환성 장점 가짐, 중괄호로 중첩 표현, 세미콜론으로 속성 구분, 대부분의 프레임워크가 SCSS문법 활용
- SASS: 중첩으로 들여쓰기 사용, 속성 구분은 줄바꿈

- CSS는 불필요한 셀렉터, 연산 기능의 한계, 구문의 부재의 문제점 있음

* scss를 사용하는 이유
css문법과 완벽하게 호환 가능. 가속성과 재사용성도 높음
- 제공 기능
1. 변수 할당
$font-stack: Helvetica, sans-serif;
$primary-color: #333;
자주 사용하는 색이나 폰트 변수로 지정 가능

2. 중첩 구문
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
한번 열은 중괄호 안에 여러개 처리 가능

3. 모듈화
@use 'base';

.inverse {
  background-color: base.$primary-color;
  color: white;
}
@use 문법을 사용해서 파일 분할하고 모듈화 하기 가능

4. mixin
@mixin theme($theme: DarkGray) {
  background: $theme;
  box-shadow: 0 0 1px rgba($theme, .25);
  color: #fff;
}

.info {
  @include theme;
}
.alert {
  @include theme($theme: DarkRed);
}
.success {
  @include theme($theme: DarkGreen);
}
함수처럼 디폴트 파라미터를 지정할 수 있고, 파라미터 받아서 속성 부여 가능 (재사용 가능)

5. 확장 & 상속
%message-shared {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

%equal-heights {
  display: flex;
  flex-wrap: wrap;
}

.message {
  @extend %message-shared;
}

.success {
  @extend %message-shared;
  border-color: green;
}

.error {
  @extend %message-shared;
  border-color: red;
}

.warning {
  @extend %message-s
}

@extend 사용 시 css속성 집합을 상속받을 수 있다. 위의 경우 %message-shared는 css 출력이 되는데, %equal-heights는 확장이 안됐으므로 출력이 안된다.

6. 연산자
@use "sass:math";

.container {
  display: flex;
}

article[role="main"] {
  width: math.div(600px, 960px) * 100%;
}

aside[role="complementary"] {
  width: math.div(300px, 960px) * 100%;
  margin-left: auto;
}
math.div와 같은 계산도 가능하지만 sin, cos, tan, random, max, min 같은 계산도 가능

* 적용 원리
sass,scss가 css의 전처리기(pre-processor)라고도 하는데, scripting언어라 sass언어랑 scss언어는 곧바로 웹에 적용은 불가능함.웹은 기본적으로 css파일로 동작하므로 별도의 컴파일 과정을 거치고 css로 변환하여 사용하게 됨.

* 단점
그렇다보니 컴파일 시간이 소요되고, 전처리기를 위한 도구가 필요함

* 사용 시 주의사항
scss 첫 사용 시 다운 받아야 한다. 아니면 "Cannot find module 'sass'"이런 오류 뜸.
yarn add sass -g
npm install sass -g
-g는 떼도 되는 것 같아보인다.