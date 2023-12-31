# 자바스크립트에서 undefined가 초기 값이 아니라고?

### var 키워드로 선언한 변수는 암묵적으로 'undefined'로 초기화한다.

여기에서 암묵적이다라는 의미는 사실은 'undefined'로 초기화 되는 것이 아니다 조금 더 정확히 이야기하면 'undefined'는 한 번 할당된 값이다. 즉, 진짜 초기값이 아니라는 것이다.

그렇다면 자바스크립트는 왜 암묵적으로 'undefined'를 할당하여 초기화 했다고 하는 것일까? 이유는 'undefined'로 할당하지 않으면 메모리 공간에 이전에 사용하였던 쓰레기 값이 남아 있을 수 있기 때문이다.

그래서 var 키워드로 선언한 변수는 암묵적으로 'undefined'로 할당하여 개발자가 예상하지 못하는 이상한 오류가 생기지 않도록 하는 것이다. 그리고 이를 초기화값이라고 부르는 것이다.