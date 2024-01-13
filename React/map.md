많은 div들을 반복문으로 줄이고 싶을 때 사용

[1,2,3].map(function(){
    return '1233211'
})

1. function안에 들은 코드들을 array 자료 갯수만큼 반복 실행(복사 붙여넣기)
2. 함수의 param은 array 안에 있던 자료임
3. return에 뭐 적으면 array로 담아줌(array의 횟수 만큼)

{
    title.map(function(a, i){
        */i는 반복문 돌 때 마다 0부터 1씩 증가하는 정수/*
        return (
            <div className="list">
                <h4>{title[1]}</h4>
                <p>published on july 16th</p>
            </div>
        )
    })
}
