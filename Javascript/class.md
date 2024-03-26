function으로 class만들기
```javascript
function villagerAgnes(name, personality, species){
    this.name = name;
    this.personality = personality;
    this.species = species;
}

villager.prototype.birthday = '4/21' //object에 추가하면 자식들이 사용 가능 부모 유전자에 있으면 가져다 쓸 수 있음(상속기능을 부연하는 장치)

var Agnes = new villager('Agnes')
var Antonio = new vilager('Antonio')
```

```javascript
class function {
    constructor(name, personality){
        this.name = name;
        this.personality = personality;
    }
}
new Hero()
```