# 자바스크립트, 조건문 switch문 편

```
switch(표현식){
    case 표현식1 :
    switch 표현식과 표현식 1이 일치하면 실행
    break;
    default:
    switch 표현식과 일치하는 case문이 없을 때 실행
}

```

switch문은 다음과 같이 표현식과 일치하는 case문을 실행시켜 준다. 그리고 표현식과 일치하지 않는 case가 없다면 default문을 실행시킨다.
이는 if...else문의 else와 같은 역할을 해주는 것이다. if...else문과 다른점은 if...else문은 true,false 즉, 불리언 값으로 실행할 코드블록을 결정하지만, switch문은 불리언 값보다는 숫자값과 문자열을 통해서 다양한 case(상황)에 따라서 실행할 코드블록을 결정한다.

switch문의 특징 중 하나는 fall through(풀스로)라는 현상이 있다는 것이다. 이는 case문의 마지막에 break문을 사용하지 않으면 표현식에 적합하는 case 표현식일지라도 코드블록에서 탈출하지 않고 다음 case로 넘어가 결국 마지막 case의 값을 출력하게 되는 현상이다. 그렇기 때문에 case문의 마지막에는 break를 꼭 붙여주어야 한다.

```
var test="";
switch(표현식){
    case 표현식1:
    case 표현식2:
    case 표현식3:
    test="표현식1+2+3"
    break;
}
```

하지만 이러한 풀스로를 활용하여서 위에 처럼 여러 개의 case문을 하나의 조건으로 사용하여 다양한 상황에 대처할 수 있다.
