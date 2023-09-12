# 자바스크립트, 반복문 while문 편

### while문은 반복 횟수가 명확할 때 사용하는 for문과 달리 반복 횟수가 불명확할 때 사용되며, 조건식의 평가가 참이면 코드 블록을 반복한다

#### while문

```
var count = 0
while(count < 10){
    console.log(count);
    count ++
}
```

while문은 위의 형태로 사용한다. count가 10이 되면 조건식이 false가 되기 때문에 반복을 멈추게 된다. 그때까지 while문은 계속해서 반복하여 실행된다. for문과 다른점은 증감식을 코드블록 안에서 사용한다는 것이다.

```
var count = 0
while(true){
    console.log(count);
    count++
    if(count===10) break;
}
```

그리고 조건식에 true를 넣으면 무한루프가 된다. 이러한 무한루프의 탈출은 if문으로 조건을 만들고 break문으로 코드블록을 탈출하게 할 수 있다. while문의 또 다른 형태이다.

#### do...while문

```
var count = 0
do{
    console.log(count);
    count++
}while(count < 3);
```

do...while문은 while문과 유사하지만 코드블록을 먼저 실행 후 조건식을 평가한다. 상황에 따라서 적절히 활용할 수 있다.
