# 자바스크립ㅌ트, 명시적 타입으로 변환하기

자바스크립트는 동적 타입 언어이지만 개발자의 의도대로 명시적으로 타입을 변환할 때가 있다. 그렇기 때문에 오늘은 명시적 타입에 대해서 알아볼 것인데, 분자열 타입으로 변환, 숫자타입으로 변화, 불리언 타입으로 변환에 대해서 살펴보자.

#### 문자열 타입으로 변환

문자열 타입으로 변환하기 위해서는 다음과 같은 세 가지 방법이 있다.

- toString() 메서드 사용
- String 함수 사용
- 문자열 연결 연산자 사용

```
let num = 123;
let str = num.toString(); // "123"
str = String(num); // "123"
1 + ''; // "1"
```

#### 숫자 타입으로 변환

숫자로 타입을 변환하기 위해서는 다음과 같은 방법이 있다.

- Number() 함수 사용
- parseInt() 함수 사용
- parseFloat 함수 사용
- `+` 단항 연산자 사용
- `*` 산수 연산자 사용

```
let str = "123"
let num = Number(str); // 123
num = parseInt(str); // 123
num = parseFloat(str); // 123
num = +str; // 123
let num = str*1; // 123
```

#### 불리언 타입으로 변환

불리언 타입으로 변환하기 위해서는 다음과 같은 방법이 있다.

- Boolean() 함수 사용
- `!!` 부정 연산자 사용

```
let truthyStr = "hello";
let bool = Boolean(truthyStr); // true
bool = !!truthyStr // true
```
