# 자바스크립트, 전역 스코프와 지역 스코프란 무엇일까?

자바스크립트를 공부하다 보면, '스코프'라는 개념을 자주 보게 된다. 스코프는 변수나 함수의 참조 범위를 의미하며, 이는 코드의 유지 보수성, 가독성, 에러 관리 관점에서 굉장히 중요한 개념이다.

### 전역 스코프와 전역 변수

전역이란, 코드의 가장 바깥 영역을 의미한다. 여기에서 선언된 변수는 전역 변수가 되며, 전역 스코프를 가진다.

```
var x = "global x";
var y = "global y";
```

위 코드에서 x,y는 전역 변수이다. 전역 변수는 코드의 어디서든 참조가 가능하다.

### 지역 스코프와 지역 변수

반면, 지역이란 함수의 내부를 말한다. 함수 내부에서 선언된 변수는 지역 변수가 되며, 지역 스코프를 가진다.

```
function outer(){
  var z = "outer's local z";
}
```

여기에서 z는 지역 변수이다. 이 변수는 outer 함수 내에서만 참조가 가능하며, 그 외의 위치에서는 참조 할 수 없다.

자바스크립트에서 스코프는 변수의 유효 범위를 결정한다. 적절한 스코프 관리는 코드의 신뢰성과 효율성을 높여준다.
