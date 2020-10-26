### Q 컴파일 언어와 인터프리터 언어
* 컴파일 언어 : 소스 코드를 실행하기에 앞서 기계어로 번역하는 행위를 컴파일이라고 하며, 소스 코드 여러 개를 하나로 묶어서 컴파일한 후에 실행하는 언어를 컴파일 언어(C, C++, JAVA)라고 한다. 컴파일 언어로 작성한 프로그램은 컴파일하는 데는 시간이 걸리지만 실행되는 속도는 빠릅니다.
* 인터프리터 언어 : 프로그램을 한 줄마다 기계어로 번역해서 실행하는 프로그래밍 언어를 인터프리터 언어라고 한다. 자바스크립트는 인터프리터 언어이다. 인터프리터 언어는 프로그램을 바로 실행할 수 있고 동작을 확인해 가면서 프로그램을 개발할 수 있다는 장점이 있다. 반면에 프로그램 코드를 한 줄 한 줄 기계어로 번역하면서 실행하기 때문에 컴파일 언어보다 처리 속도가 느리다.

### Q 자바스크립트의 특징
1. 인터프리터 언어다.
1. 동적 프로토타입 기반 객체 지향 언어다.    
    -> 자바스크립트는 클래스가 아닌 프로토타입을 상속하는 프로토타입 기반 객체 지향 언어다. 자바스크립트에서는 객체를 생성한 후에도 프로퍼티와 메서드를 동적으로 추가하거나 삭제할 수 있        다(C++, JAVA 같은 클래스 기반 객체 지향 언어와는 다른 점임).
1. 동적 타입 언어다.   
    -> C++와 JAVA는 실행되기 전에 변수 타입이 결정되는 정적 타입 언어이다. 반면에 자바스크립트는 변수 타입이 없다. 따라서 프로그램을 실행하는 도중에 변수에 저장되는 데이터 타입이 동적        으로 바쓀 수 있다
1. 함수가 일급 객체다.   
    -> 자바스크립트의 함수는 객체이며, 함수에 함수를 인수로 넘길 수 있다.
1. 함수가 클로저를 정의한다.   
    -> 클로저로 변수를 은닉하거나 영속성을 보장하는 등 다양한 기능을 구현할 수 있다.
    
### Q ECMAScript 6
ECMAScript 6는 다른 프로그래밍 언어가 제공하는 다양한 기능을 추가하면서도 이전 자바스크립트 버전과의 호환성을 보장한다.

### Q 변수의 명명 규칙
캐멀 표기법(ex. newName), 파스칼 표기법(각 단어의 첫 글자를 대문자로 표기 ex. NewName), 밑줄 표기법(ex. new_name)

### Q 변수의 동적 타이핑
C나 JAVA 등의 프로그래밍 언어에는 정수 타입 변수, 부동소수점 타입 변수 등이 있어서 그 변수의 타입과 일치하는 데이터만 저장할 수 있다. 이처럼 변수에 타입이 있는 언어를 가리켜 정적 타입 언어라고 한다.   
실행할 때 변수에 저장된 데이터 타입을 동적으로 바꿀 수 있는 언어를 가리켜 동적 타입 언어라고 한다.

### Q 자바스크립트가 처리할 수 있는 데이터 타입
* 원시타입(숫자, 문자열, 논리값 등) : 원시 타입 데이터는 데이터를 구성하는 기본적인 요소로 불변 값으로 정의한다.
* 객체 타입 : 객체는 변수 여러 개가 모여서 만들어진 복합 데이터 타입이다. 자바스크립트에서는 원시 타입을 제오한 모든 값이 객체이다.

### Q null 과 undefiend
둘 다 값이 없음을 표현하기 위한 특수한 값임.   
    -> undefiend는 정의되지 않은 상태를 뜻 함.(변수에 값을 할당하지 않으면 결과는 undefiend)   
    -> null은 아무것도 없음을 값으로 표현한 리터럴이다. null은 주로 프로그램에서 무언가를 검색했지만 찾지 못했을 때 아무것도 없음을 전달하기 위한 값으로 사용.
    
### Q 템플릿 리터럴
템플릿이란 일부만 변경해서 반복하거나 재사용할 수 있는 틀을 말한다.   
    -> 기본적인 사용법 : 문자열을 역따옴표로 묶는다.   
    -> 템플릿 리터럴 안에는 플레이스 홀더(실제 내용물을 나중에 삽입할 수 있도록 일단 확보한 장소를 의미)를 넣을 수 있다. 플레이스 홀더는 ${...}로 표기한다.
    
### Q 객체
var card = {suit: "하트", rank: 'A'} <- {...}이 부분이 객체 리터럴임.     
객체에 포함된 데이터 하나를 가리켜 객체의 프로퍼티하고 부른다. suit와 rank는 프로퍼티이며 프로퍼티의 이름 부분을 프로퍼티 이름 또는 키라고 한다.   

card.suit // 하트   
card["rank"] // A   

변수에 대입된 객체안의 프로퍼티 값을 읽거나 쓸 때는 마침표연산자 또는 대괄호 연산자를 사용한다.   
마침표로 프로퍼티를 읽거나 쓸 때는 프로퍼티 이름 즉, 식별자만 사용할 수 있다. 대괄호로 프로퍼티를 읽거나 쓸 때는 프로퍼티 이름 또는 문자열을 반환하는 표현식을 사용할 수 있다.

### Q in 연산자로 프로퍼티가 있는지 확인하기
in 연산자를 사용하면 객체에 특정 프로퍼티가 있는지 확인할 수 있다.   
프로퍼티 이름을 뜻하는 문자열 in 객체명   
var card = {suit: "하트", rank: 'A'}   
console.log("suit" in card) // true

### Q 객체 참조 타입
생성된 객체는 메모리의 영역을 차지하는 한 덩어리가 된다. 객체 타입의 값을 변수에 대입하면 그 변수에는 개체의 참조(메모리에서의 위치 정보)가 저장된다. 이때의 변수 상태를 가리켜 그 객체를 참조하고 있다라고 한다.   
var a = crad;   
a.suit = "스페이드";   
console.log(a.suit) // 스페이드   

### Q 함수
일련의 처리를 하나로 모아 언제든 호출할 수 있도록 만들어 둔 것

함수의 실행 흐름   
1. 호출한 코드에 있는 인수가 함수 정의문의 인자에 대입된다.   
1. 함수 정의문의 중괄호 안에 작성된 프로그램이 순차적으로 실행된다.   
1. return 문이 실행되면 호출한 코드로 돌아간다. return 문의 값은 함수의 반환값이 된다.   
1. return 문이 실행되지 않은 상태로 마지막 문장이 실행되면, 호출한 코드로 돌아간 후에 undefined가 함수의 반환값이 된다.   

### Q
