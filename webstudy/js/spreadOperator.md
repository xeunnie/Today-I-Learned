* spread operator
1) array나 object 자료형 왼쪽에 붙임
뜻은 별거없고 괄호를 벗겨주세요~ 라는 뜻

...[1,2,3] 이렇게 쓰면

그 자리에 1,2,3 이 남음, 걍 괄호 벗기기용 연산자

2) array나 object 자료형을 복사할 때 많이 사용
let data1 = [1,2,3];
let data2 = [...data1];
console.log(data1 === data2)
그냥 data1에 있던 자료들을 괄호 벗긴담에 다시 array로 만들어주세요~ 라는 뜻 -> 새로운 array로 인식

완전 독립적인 array 복사본을 생성
object 자료형도 마찬가지

그리고 독립적인 사본을 shallow copy 아니면 deep copy 라고 함