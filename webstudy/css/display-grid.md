display:grid
모눈종이에 색칠하는 방식,

칸 배정하기
grid-column : 1 / 4; 가로 1번 선부터 4번 선까지 배정
grid-row : 2 / 4; 세로 2번 선부터 4번 선까지 배정


.grid-containr {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    grid-template-rows: 100px 100px 100px;
    grid-gap: 10px;
    grid-template-areas:
    "nav-header nav-header nav-header nav-header"
    "sidebar sidebar . ."
    "sidebar sidebar . ."
}
.grid-nav {
    grid-area: "nav-header";
}
.grid-sidebar {
    grid-area: "sidebar";
}