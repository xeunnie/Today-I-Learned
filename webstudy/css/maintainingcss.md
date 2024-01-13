css 덮어쓰기 및 유지보수

css 덮어쓰는 방법
1. 같은 클래스명 하단에 쓰기
2. 그냥 같은 클래스명 하단에 쓰기
3. specificity 높이기
택일하기

.custom{
    color: red;
}

덮어쓰기
1. 더 밑에 작성
    .custom{
        color: red;
    }

    .custom{
        color: blue;
    }

    중복 시, 더 아래 있는 명령을 따름

2. 우선순위 높이기
    .custom{
        color: red;
    }
    클래스는 10점

    #id {
        color: purple
    }
    아이디 부여는 100점

    style=" color: yellow "
    html 스타일은 1000점

    .custom{
        color: red !important ;
    }
    !important는 10000점(최대점)

3. specificiity 점수 높이기
    .main-bg .custom{
        color: red;
    }
    20점

    div.main-bg .custom{
        color: red;
    }
    21점

    div.main-bg p.custom{
        color: red;
    }
    22점


bootstrap은 덮어쓰지 않고 클래스를 추가함. css 파일 추가 후 html에서 더 아래에 링크를 달면 된다.

좋은 코드의 원칙
1. 내가 짠 코드가 나중에 수정이 쉽고 관리가 쉬워지면 좋은 코드
2. 확장성이 좋으면 좋은 코드
3. 양이 적으면 좋다 (선택사항)

