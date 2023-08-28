# 자바스크립트는 개발자가 메모리 제어를 못한다고?

### 변수란 하나의 값을 저장하기 위해 확보한 메모리 공간 자체 또는 그메모리 공간을 식별하기 위해 붙인 이름을 말한다.

변수는 메모리에 저장된다. 정확히는 1바이트 즉, 8비트 단위의 메모리 셀에 저장되고 이 집합체를 메모리라고 부른다.

컴퓨터는 메모리 셀을 저장 하고 읽어드린다. 그리고 각 메모리 셀은 모메리 주소를 갖는다.

그래서 직접적으로 메모리 주소를 통해서 값을 직접 접근하면 혹여나 운영체제가 사용하고 있는 값이 변경되어 시스템 자체가 멈출 수 있다.

따라서 자바스크립트는 개발자의 직접적인 메모리 제어를 허용하지 않는다.