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

### Q let, const, var
const 문으로 선언한 상수 값은 수정할 수 없지만, 상수 값이 객체이거나 배열일 경우에는 프로퍼티 또는 프로퍼티 값을 수정할 수 있다.

### Q 객체의 메서드
객체의 프로퍼티 중에서 함수 객체의 참조를 값으로 담고 있는 프로퍼티를 가리켜 메서드라고 부른다.   
var circle = {   
    center : {x:1.0, y:2.0},   
    radius : 2.5,   
    area: function() {   
        return Math.PI * this.radius * this.radius;   
     }   
   }   
함수 객체 안에 적힌 this는 그 함수를 메서드로 가지고 있는 객체를 가리킨다.(this.radius가 circle.radius 임)

### Q 함수를 활용하면 얻을 수 있는 장점
01. 재사용할 수 있다.   
1. 만든 프로그램을 이해하기 쉽다.   
1. 프로그램 수정이 간단해진다.

### Q 생성자로 객체 생성하기
JAVA, C++ 와 같이 클래스(붕어빵 틀)를 사용하면 프로퍼티가 똑같은 객체를 얼마든지 만들 수 있다. 하지만 자바스크립트에는 클래스가 없다. 대신 생성자(new)라고 하는 함수로 객체를 생성할 수 있다.   

function Card(suit, rank){   
    this.suit = suit;   
    this.rank = rank;   
    };
var card = new Card("하트", "A");   
console.log(card) // Card {suit: "하트", rank: "A"}   

생성자와 new 연산자로 생성한 객체를 그 생성자의 인스턴스(생성한 실체)라고 부른다.

### Q Array 생성자로 배열 생성
var events = new Array(2, 4, 6, 8) /// [2, 4, 6, 8]   
Array 생성자의 인수가 한 개고 그 값이 양의 정수면 이때 인수는 배열 길이를 뜻하므로 배열이 그 길이만큼 생성된다.   
var x = new Array(3);   
console.log(x.length); // 3

### Q 피연산자
0,-0, 빈 문자열(""), NaN, null, undefiend <- false   
0을 제외한 숫자, 빈 문자열을 제외한 문자열 <- true   

### Q 이벤트 처리기
웹 브라우저에서 동작하는 프로그램은 기본적으로 이벤트 주도형 프로그램이다. 이벤트란 사용자가 버튼을 클릭하는 행위처럼 단말기와 애플리케이션이 처리할 수 있는 동작이나 사건을 뜻한다. 이벤트 주도형 프로그램이란 이벤트가 발생할 때까지 기다렸다가 이벤트가 발생했을 때 미리 등록해 둔 작업을 수행하는 프로그램을 말한다.
* GUI(그래픽 유저 인터페이스)

### Q 자바스크립트 프로그램 실행 문맥의 구성
실행 문맥은 실행 가능한 코드가 실제로 실행되고 관리되는 영역으로 실행에 필요한 모든 정보를 컴포넌트 여러 개가 나누어 관리하도록 만들어져 있다. 그중에서 가장 중요한 컴포넌트는 렉시컬 환경 컴포넌트, 변수 환경 컴포넌트, 디스 바인딩 컴포넌트이다. 렉시컬 환경 컴포넌트와 변수 환경 컴포넌트는 타입이 같고 실제로 with 문을 사용할 때를 제외하면 내부 값이 같으므로 똑같이 취급해도 무방하다. 디스 바인딩 컴포넌트는 그 함수를 호출한 객체의 참조가 저장되는 곳이다. 실행 문맥의 구성 요소인 렉시컬 환경 컴포넌트는 자바스크립트 엔진이 자바스크립트 코드를 실행하기 위해 자원을 모아 둔 곳으로 구체적으로는 함수 또는 블록의 유효 범위 안에 있는 식별자와 그 결과값이 저장되는 곳이다. 자바스크립트 엔진의 해당 자바스크립트 코드의 유효 범위 안에 있는 식별자와 그 식별자가 가리키는 값을 키와 값의 쌍으로 바인드(묶다)해서 렉시컬 환경 컴포넌트에 기록한다.   

* 프로그램 실행과 실행 문맥   
실행 문맥(Execution Context)은 스택이라는 구조로 관리된다. 스택이란 일종의 자료 구조로 데이터를 아래에서부터 쌓아 올려서 마지막으로 추가한 데이터를 먼저 꺼내는 '후입선출'방식으로 관리된다. 스택에 데이터를 쌓는 행위를 push, 스택의 가장 윗 부분에서 데이터를 빼내는 행위를 pop이라고 한다. 실행 문맥은 프로그램 실행 중에 스택에 push되어 실행된다. 가장 먼저 실행하는 코드는 전역 코드이며, 이 때문에 스택의 맨 아랫부분에는 항상 전역 코드를 실행하기 위한 실행 문맥이 자리 잡고 있다. 전역 코드 안에서 함수를 실행하면 그 함수를 실행하기 위한 실행 문맥을 스택에서 push한다. 그리고 그 함수의 작업을 끝내고 함수를 호출한 부분으로 제어권이 돌아오면 스택에서 pop한다. 이때 실행하는 한수가 특정 함수의 내부에 정의된 중첩 함수라면 중첩 함수의 실행 문맥을 새로 만들어서 스택에 push한다. 중첩 함수의 실행 문맥이 외부 함수의 실행 문맥안에 중첩되지 않는다는 점을 꼭 기억하자.   

### Q 클로저란 무엇이며, 왜 이러한 패턴을 사용하는가
function Person(name, age){   
    var _name = name;   
    var _age = age;   
    return {   
        getName: function() {return _name;},   
        getAge: function() {return _age;},   
        setAge: function(x) {_age = x;}   
        }   
        }   
var person = Person("Tom", 18);   
console.log(person.getName()); // Tom   
console.log(person.getAge()); // 18   
person.setAge(19);   
console.log(person.getAge()); // 19   

반환된 내부함수가 자신이 선언됐을때의 환경인 스코프를 기억하여 자신이 선언되었을때의 환경 밖에서 호출되어도 그 환경에 접근할 수 있는 함수, 자신이 생성될때의 환경을 기억하는 함수이다.

사용하는 이유   
1. 현재 상태를 기억하고 변경된 최신 상태를 유지하기 위해   
1. 전역 변수의 사용을 억제 하기위해   
1. 정보를 은닉하기 위해   
1. 실수를 줄이기 위해   

### Q 브라우저의 렌더링 과정에 대해서 상세하게 설명하시오.
브라우저 주소창에 www.naver.com을 치면 -> 네이버 서버를 찾아간다. -> DNS(실제 서버가 어디에있는지 알고 있는 서버)가 연결해줄 곳을 찾음 -> (여기서 주소 앞에 HTTPS가 붙었다면 HTTPS방식으로 통신하겠다.) -> 서버의 기본설정이 대부분 index.html되어 있어 서버에서 이파일을 클라이언트로 보냄 -> 브라우저는 텍스트로 이루어진 index.html 파일을 파싱한다. -> 한줄한줄 읽으면서 DOM트리를 만들어나감 -> 중간에 link 태그를 만나 css요청이 끝나면 중단된 html을 다시 읽고 DOM트리를 만들어나감. -> 중간에 LINK태그를 만나 CSS요청이 발생하면, 요청과 응답과정을 거치고 CSS를 파싱함 -> CSS파싱이 끝나면 중단된 html을 다시읽고 DOM트리를 완성 -> 완성된 DOM트리와 CSSOM트리를 합쳐 Render Tree를 만들고 그린다. js코드를 실행하기 위해 파싱을 중단 -> 제어권한을 자바스크립트 엔진에게 넘기고, 자바스크립트 코드 또는 파일을 로드해서 파싱하고 실행

### Q Http와 Https 통신 방식의 차이
결정적 차이는 보안이다.   
1. http방식은 네트워크상에서 정보를 누군가가 마음대로 열람, 수정이 가능 / https는 누가 볼수없도록 막음.   
1. http방식이 https방식보다 빠르다.   
1. https는 설치 및 인증서를 유지하는데 추가적인 비용이 발생   
민감한 정보가 있는 페이지의 경우 https 그럴필요가 없으면 http로 만들면 된다.

### Q OOP 특징에 대해 설명하라.
Object Oriented Programming 객체지향 프로그래밍이라고한다.   
<특징>   
1. 상속: 클래스개념에서 상위 클래스로 부터 하위 클래스에 유산을 물려받는것과 같이, 부모의 메소드나 변수를 사용할 수 있는 것을 말함.
1. 다형성: 같은 함수가 있다고 칠대 그 하수가 매개변수에 따라 다른 역할을 할 수 도 있다.
1. 캡슐화: 보통 데이터를 은닉시킨다고 표현하는데, 외부에서 쉽게 데이터를 접근할 수 없게 만들기도하고, 데이터 구조와 데이터를 다루는 방법들을 한데다 묶는것.
1. 추상화: 공통적인 속성이나 기능을 묶어서 이름을 붙이는 것(a,b,c이런게있다고 치면 이런것을 알파벳이라고 묶을 수 있다)

### Q 함수형 프로그래밍
* 함수형 프로그래밍에 대해 설명해달라
 함수형 프로그래밍은 순수함수와 보조 함수의 조합을 통해 로직내에 존재하는 조건문과 반복문을 제거하여 복잡성을 해결하고 변수의 사용을 억제하여 상태 변경을 피하려는 프로그래밍 패러다임이다.   
* 함수형 프로그래밍에 개념에서 순수함수란 무엇인가
순수함수는 같은 입력이 주어지면, 같은 출력을 반환해야하고, side effect(부작용) 이 없어야한다.
결국, 함수형 프로그래밍은 순수함수를 통해 sideeffect를 최대한 억제하여 오류를 피하고 프로그램의 안정성을 높이려는 노력의 한 방법   
* OOP와 함수형 프로그래밍의 가장 큰 차이점은 무엇인가
객체지향은 객체 안에 상태를 저장하고, 이 상태를 이용해서 메소드를 추가하고 상태변화를 설정하고 조정하기위해 다양한 기능을 사용한다. 이에 반해 함수형 프로그래밍은 상태를 제어하는것보다 상태를 저장하지 않고 없애는데 주력한다. 
예를들면, 객체 지향은 상태를 저장하는 필드와 그 필드들을 이용해 기능을 제공하는 메소드를 만들고 클래스를 만듭니다. 반면 함수형은 몇몇 자료구조(list, map, set) 등을 이용해 최적화된 동작을 만들어낸다.
