# 자바스크립트, 단축평가 활용하기

### 단축평가는 표현식을 효율적으로 계산하기 위한 방법으로 논리 연사자, 옵션널 체이닝 연산자, null 병합 연산자를 통해서 구현할 수 있다.

#### 논리연산자와 단축평가

```
let result = true || "hello" // true
let result = false || "hello" // "hello"

let result = true && "hello" // "hello"
let result = false && "hello" // false
```

`||`연산자는 첫 번째 피연산자가 `true`라면 두 번째 피연산자를 확인하지 않고 첫 번째 피연산자를 반환한다. 첫 번째 피연산자가 `false`인 경우는 두 번째 피연산자를 반환한다.

#### 옵셔널 체이닝 연산자

```
let name = user?.address?.city; // use나 address가 null이면 undefined
```

옵셔널 체이닝 연산자란 `?`로 표기한다. 이는 객체의 중첩된 속성에 안전하게 접근할 수 있게 해준다. 예를 들어 객체가 null이거나 undefined이면 연산이 중단되고 undefined가 반환되고, 그렇지 않으면 우항의 프로퍼티 참조를 이어간다. 이러한 옵셔널 체이닝은 변수가 null 또는 undefined가 아닌지 확인하고 프로퍼티를 참조할 때 유용하게 사용된다.

#### Null 병합 연산자

```
let displayText = inputText ?? 'default'; // inputText가 null/undefined면 'default'
```

Null 병합 연산자 `??`은 좌항의 값이 null 또는 undefined일 경우에만 우항의 값을 반환한다. 그렇지 않으면 좌항의 피연산자를 반환한다. 하지만 falsy값들(0, false, null, undefined, NaN, -0, "")에 대해서는 왼쪽 피연산자값을 그대로 반환한다.

```
function greet(name){
  let displayName = name ?? 'Guest';
  console.log(`Hello,${diplayName}!`)
}

greet(null); // "Hello Guest!"
greet('John') // "Hello John!"
```

그렇기 때문에 변수에 기본값을 할당할 때 매우 유용하다. 예를 들면, 하마수의 매개변수에 기본값을 설정할 때 사용할 수 있다. 위와 같이 name이 null이거나 undefined인 경우에만 결괏값이 Guest가 되고, 다른 falsy 값들은 그대로 유지된다.
