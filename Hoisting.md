## 호이스팅 (Hoisting) 개념
> 함수 안에 있는 선언들을 모두 끌어올려서 해당 함수 유효 범위의 최상단에 선언하는 것을 말한다

### 호이스팅이란?
자바스크립트 함수는 실행되기 전에 함수 안에 필요한 변수값들을 모두 모아서 유효 범위의 최상단에 선언한다
- 자바스크림트 parser가 함수 실행 전 해당 함수를 한번 훑는다.
- 함수 안에 존재하는 변수/함수선언에 대한 정보를 기억하고 있다가 실행
- 유효범위 : 함수 블록 `{}` 안에서 유효

즉, 함수 내에서 아래쪽에 존재하는 내용 중 필요한 값들을 끌어올리는 것이다.
- 실제로 코드가 끌어올려지는건 아님, 자바스크립트 Parser 내부적으로 끌어올려서 처리하는 것
- 실제 메모리에는 변화가 없다.

### ❗️ 변수 호이스팅(var, let, const 키워드
- var 변수 선언과 함수선언문에서만 호이스팅이 일어난다.
- var 변수/ 함수의 선언만 위로 끌어 올려지며, 할당은 끌어 올려지지 않는다.
- let/const 변수 선언과 함수표현식에서는 호이스팅이 발생하지 않는다.

> 호이스팅은 함수선언문과 함수표현식에서 서로 다르게 동작하기 때문에 주의해야 한다.
변수에 할당된 함수표현식은 끌어 올려지지 않기 때문에 이때는 변수의 스코프 규칙을 그대로 따른다.

### 변수생성과 호이스팅
__1단계 : 선언단계 (declaration phase)__
변수를 실행 컨텍스트의 변수 객체에 등록한다.
이 변수 객체는 스코프가 참조하는 대상이 된다.

__2단계 : 초기화 단계 (Initialization phase)__
변수 객체에 등록된 변수를 위한 공간을 메모리에 확보한다.
이 단계에서 변수는 undefind로 초기화

__3단계 : 할당단계 (Assignment phase)__
undefined로 초기화된 변수에 실체 값을 할당한다.


#### 🔑호이스팅 사용 시 주의!
> 코드의 가독성과 유지보수를 위해 호이스팅이 일어나지 않도록 주의해야 한다
- 호이스팅을 제대로 모르더라도 함수의 변수를 가급적 코드 상단부에서 선언하면, 호이스팅으로 인한 스코프 꼬임 현상은 방지할수 있다.
- let/const 를 사용하자!
