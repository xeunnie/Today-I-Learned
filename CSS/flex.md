참고 링크: https://velog.io/@mooongs/flex1%EC%9D%98-%EC%9D%98%EB%AF%B8

* flex 속성

0. flex와 표현 정리
- flex-basis: flex item의 기본크기
- flexible: 너비에 따라 유동적으로 변화
- inflexible: 화면이나 플렉스 컨테이너 너비 변경이랑 상관 없이 원래 크기 유지

1. flex-grow
- flex-basis보다 늘어날 수 있는지 결정하는 속성
- 디폴트 값은 0으로 inflexible한 상태를 의미
- 숫자의 의미 -> flex-basis를 제외한 나머지 여백을 해당 비율로 나눠갖는 다는 뜻 -> 1 이상의 값이 나오면 너비에 따라 유동적으로 변화한다는 것 = flexible

2. flex-shrink
- flex-basis보다 줄어들 수 있는지 결정하는 속성
- 디폴트 값은 1, 1 이상의 속성 값이 주어지면 해당 비율로 줄어들 수 있음을 의미 = flexible
- 값으로 0이 오면, flex-basis보다 줄어들지 않음, 고정 너비 설정 가능 = inflexible

3. flex-basis
- flex item의 기본 크기로, 디폴트 값인 auto 일 때는 컨텐츠 너비만큼을 의미, flex-direction이 row일 때는 너비 크기, column일 때는 높이 크기를 의미

4. flex: 속성
1) flex 뒤에 오는 속성에 따른 내용
- 값 1개일 때
숫자 넣을 시 -> flex-grow
길이 or 퍼센트 -> flex-basis
none, auto, initial 중에 하나 지정 가능
- 값 2개일 때
1번째 값은 숫자(flex-grow),
2번째 값이 숫자 -> flex-shrink
길이 or 퍼센트 -> flex-basis
- 값 3개일 때
flex-grow에 쓸 숫자
flex-shrink에 쓸 숫자
flex-basis에 쓸 길이 or 퍼센트, auto
2) flex: 1의 의미는?
flex: 1의 의미를 풀어서 보면
flex-grow: 1;
flex-shrink: 1;
flex-basis: 0%
flex-basis가 0 -> 점유 크기를 0으로 만든 후 화면 비율에 따라 유연하게 늘어날 수 있음
부모의 flex container의 너비가 변할 때도 동일한 비율로 늘어나고 줄어듦