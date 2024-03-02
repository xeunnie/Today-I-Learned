* useParams
useParams라는 함수를 임포트 해오면 현재 /:url파라미터 자리에 유저가 입력한 값을 가져올 수 있ek. 이걸 변수에 저장해서 쓸 수 있다.

import { useParams } from 'react-router-dom'

function Detail(){
  let {id} = useParams();
  console.log(id)
  
  return (
    <div className="container">
        <h4>{props.data[id].title}</h4>
    </div>
  )
}