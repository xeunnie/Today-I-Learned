* Router

- 리액트로 페이지 만들기
페이지를 나눌 때 html 기반 사이트는 그냥 여러 html파일을 만듦.
하지만 리액트는 html 파일 하나만 사용하고 다른 페이지를 요청하면 내부 div를 그냥 갈아치워벌임
이때 react-router-dom이라는 외부 라이브러리 설치해서 구현하는게 일반적

- 라우터 돔 셋팅하기
터미널에 npm install react-router-dom@6입력해서 설치하기

1. 셋팅은 index.js 파일에 가서

import { BrowserRouter } from "react-router-dom";

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
      <BrowserRouter>
        <App />
      </BrowserRouter>
  </React.StrictMode>
);

이런식으로 감싸면 되는 부분

2. 다른 페이지를 나눠주고 싶을 때, App.js파일 들어가서

import { Routes, Route, Link } from 'react-router-dom'

function App(){
  return (
    (생략)
    <Routes>
      <Route path="/detail" element={ <div>상세페이지</div> } />
      <Route path="/about" element={ <div>어바웃페이지</div> } />
    </Routes>
  )
}

Routes를 만들고 그 안에 Route 작성

<Link to="/">홈</Link>
<Link to="/detail">상세페이지</Link>
이런식으로 원하는 곳에 링크 만들기 가능