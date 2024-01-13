<class를 이용한 옛날 React 문법>

class Modal extends React.Component {
    constructor(props){
        super(props)
        this.state = {
            name : 'choi',
            age : 25
        }
    }
    render(){
        return(
            <div>Hi {this.state.name}
                <button onClick={()=>{
                    this.setState({age : 21})
                }}>click</button>
            </div>
            #여기 html 작성
        )
    }
}

class는 변수, 함수 보관함임
constructor, super, render 세개를 채워넣어야 함
위가 기본 템플릿