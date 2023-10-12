# 자바스크립트, 참조에 의한 전달과 외부 상태 변경

오늘 살펴볼 내용은 자바스크립트에서의 함수 호출에서 매개변수와 인수가 어떻게 전달되는지, 그리고 이로 인한 외부 상태의 변경에 대해서 알아보자

### 값에 의한 전달 vs 참조에 의한 전달

자바스크립트에서는 원시 타입과 객체 타입에 따라 변수의 값이 함수 내로 전달되는 방식이 다르다.

#### 값에 의한 전달

원시 타입(Number, String, Boolean 등)의 경우, 변수의 실제 값이 복사되어 함수의 매개변수로 전달된다.

```
function changeVal(primitive){
  primitive += 100;
  console.log(`내부에서 변경한 값: ${primitive}`);
}

var num =100
chageVal(num);
console.log(`원래 값: ${num}`);

// 내부에서 변경한 값: 200
// 원래 값: 100
```

#### 참조에 의한 전달

반면 객체 타입의 경우, 변수의 참조값이 함수의 매개변수로 전달디 된다.

```
function changeObj(obj){
  obj.name="Kim";
}

var person = {name: "Lee"};
changeObj(person);
console.log(person.name); // "Kim"
```

### 외부 상태의 변경과 부수 효과

함수 내부에서 객체의 속성을 변경하면, 이 변경은 함수 외부의 객체에도 반영이 된다. 이렇게 되면 외부 상태가 예기치 않게 변경되어 프로그램의 복잡성이 증가하고, 디버깅이 어려워진다.

```
function addProperty(obj){
  obj.newProp = "i'm new!";
}

var myObj = { existingProp: "i'm existing!"};
addProperty(myObj);

console.log(myObj.newProp); // 출력:"I'm new!"
```

### 불변 객체와 방어적 복사

이러한 문제를 해결하기 위한 한가지 방법은 객체를 불변을 만드는 것이다. 불변 객체는 한 번 생성되면 그 상태를 변경할 수 없다. 이렇게 하면 함수 내부에서 객체를 변경하더라도 원본 객체는 영향을 받지 않는다.

자바스크립트에서는 Object.freeze() 메서드를 사용하여 객체를 불변으로 만들 수 있다.

```
var immutableObj = Object.freeze({name:"Lee"});
```

자바스크립트에서 함수를 사용할 때는 값의 전달 방식과 외부 상태의 변경에 주의해야 한다. 가능하다면 불변 객체를 사용하거나, 객체를 변경할 필요가 있을 때는 방어적 복사를 통해 원본 객체를 보호하는 방법을 고려하는 것이 좋다.
