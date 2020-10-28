(/)
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

### Q 웹 프로토콜이란
* 웹 프로토콜이란?   
웹 프로토콜은 웹에서 쓰이는 통신규약입니다. 통신규약이라는 것은 쉽게 설명하면, 통신을 할때 내가 이렇게 할게 너는 이렇게 해줘 라고 약속하는 것입니다.   
* Http 통신이란?   
웹 프로토콜중 하나로 HTTP가 가장 많이 쓰이는데 Hyper text Transfer Protocol의 약자입니다.
쉽게말하면, 인터넷에서 데이터를 주고 받을 수 있는 통신규약 정도로 보시면됩니다. 요청과 응답으로 이루어져있어 어떤 데이터 주세요하고 요청하면, 이 데이터 줄게요 라고 응답합니다.   
* Http 1.1과 2.0의 차이는?   
가장 큰 차이는 속도이다. 2.0같은 경우는 헤더를 압축해서 보내기도하고, 한번의 연결로 동시에 여러 메시지를 주고 받을 수도 있다.

### Q 비동기 프로그래밍
* AJAX란 무엇인가   
자바스크립트를 이용해 비동기적으로 서버와 브라우저가 데이터를 교환할 수 있는 통신 방식
보통은 서버로부터 웹페이지가 반환되면 전체를 갱신해야하는데  / AJAX를 사용하면, 페이지 일부만을 갱신하고도 동일한 효과를 볼 수 있다. 즉, 갱신이 필요한 부분만 로드하여 갱신하면 되므로 빠르고, 부드러운 화면효과를 기대할 수 있음   
* Promise와 Callback의 차이점은 무엇이며 각각의 장단점은 무엇인가.   
ES2015 이전에는 콜백형태로 비동기를 사용했다.   
콜백형태의 단점: 계속해서 콜백 내에서 작업해야되며 깊이가 깊어져(함수를 중첩하게 사용되는 경우가 발생해 콜백헬이 발생) 시안성이 낮다.   
Promise가 등장하면서 직관적으로 코딩이 가능해졌다.   
프로미스는 결과값을 가지고 있지만, then이나 catch가 나오기전에 반환하지 않는다.   
* Promise란 무엇이며 코드가 어떻게 구성되어있는가.   
//// 프로미스 선언 ////   
const plus = new Promise ((resolve, reject)=>{   
   const a=1;   
   const b=2;   
   if (a+b<2){   
       resolve(a+b); // 성공 -> then   
  }else{   
       reject(a+b); // 실패 -> catch   
  }   
});   
​
// resolve가 되면 then 으로,   
// reject가 되면 catch로 반환된다.   
plus   
  .then((success)=>{   
       console.log('성공! ',success);   
  })   
  .catch((fail)=>{   
       console.error('실패! ',fail);   
  });   
비동기 처리에 성공하면 resolve메소드를 호출해서 비동기 처리 결과를 후속처리 메소드로 전달한다.   
비동기 처리에 실패하면 reject메소드를 호출해서 에러메시지를 후속처리 메소드로 전달한다.   
후속처리메소드는 then과 catch가 있다. 둘다 Promise를 반환한다.   
then 을 가지고 메소드 체이닝을 통하여서 콜백헬 문제를 해결 할 수 있다.   

### Q Async, Await와 Promise의 차이는
Promise를 더욱 쉽게 사용할 수 있도록 ES2018(ES8)문법이다. 함수의 앞부분에 async 키워드를 추가하고, 함수 내부에서 Promise의 앞부분에 await 키워드를 사용한다. async, await를 사용할 경우 코드가 간결해지지만, 에러처리를 잡기 위해 try, catch를 사용해야한다. 동기적인 코드흐름으로 개발이 가능하다.

### Q 자바스크립트의 타입
* 자바스크립트의 Number Type은 다른 언어들과 차이점이 무엇인가, 왜 하나만 존재하는가.   
다른언어에는 int double 등 숫자타입의 다양함이 있지만, number는 하나만 있다. 정수만을 위한 타입이 없고, 모든 수를 실수로 처리한다.   
* 자바스크립트의 원시 타입은 몇가지인가? 종류는?   
boolean, string, number, undefiend, null, symbol 이렇게 6가지 종류이다.   
undefiend는 선언만 되어있고 값은 없는 상태, null은 자료형이 객체이며 빈값을 의미.   
* 자바스크립트의 호이스팅은 어떻게 이루어져 있는가.   
변수를 선언하고 초기화 했을때 선언부분이 최상단으로 끌어올려지는 현상
예를들어, 코드 상단에서 console.log(a)를 찍고 하단에서 var a=1; 이라고 하였을때 a는 undefined라고 나온다. 이런 현상을 호이스팅이라고한다. 함수의 경우 함수표현식은 호이스팅이 적용되지 않으나 일반 함수선언문은 함수 호이스팅이 적용된다.   
* 가비지켈렉터의 역할은? 어떻게 동작하는가.   
메모리 할당을 추적하고 할당된 메모리 영역이 필요하지 않은 영역일 경우를 판단해서 회수하는 것.
자바스크립트에서 변수는 직접적으로 참조 값(문자열, 객체, 배열 등)을 담고 있지 않고, 해당 값을 메모리 상에 저장 된다. 그래서 참조 값을 생성하고나서 더이상 참조할 것이 없거나 비어졌을 때 가비지 컬렉터가 동작해서 메모리가 반환됨.(메모리를 다시 재사용할 수 있는 상태가 된다)   
* 자바스크립트의 순환참조란? 어떤게 문제이고 해결방법은?   
순환 참조란 A모듈에서 B모듈을 Import하고, B모듈에서도 A모듈을 Import할 때 아직 반환되지 않은 함수를 사용하면 에러가 나는 문제입니다.   
이 문제를 해결하는 방법으로는 모듈의 Dependency 순서를 명확히 지정하는 것이고, 좀 복잡하고 Dependency가 많다면 별도의 모듈을 Import하는 파일을 만들어서 해당 파일 내부에서 모듈 Import를 관리하는 것도 하나의 방법입니다.
* 자바스크립트의 배열이 실제 자료구조 배열이 아닌데 그 이유는?   
자바스크립트의 배열은 실제 자료구조의 배열과 다르게 HashMap으로 구현되어있다. 이 HashMap을 구현하기 위해서는 연결리스트로 구현하게 되는데 연결리스트에서 값을 찾기 위해서는 탐색해나가면서 값을 찾는 불상사가 발생한다. 이를 해결하기 위해서 타이핑된배열(Int8Array,Float32Array 등) 이 추가되고 있다.   
* 이벤트 루프에 대해서 설명, 동시성 모델에 대해서 설명하시오.   
자바스크립트는 싱글 스레드 기반 언어이다. 함수를 실행하면 함수 호출이 스택에 순차적으로 쌓이고 스택의 맨위에서부터 아래로 한번에 하나의 함수만 처리 할 수 있다.   
하지만, 자바스크립트에는 이벤트 루프라는것을 통해 동시성을 지원한다. (동시에 일어나는 것이 아니라 동시에 일어나는 것처럼 보이게 하는것이다!)    
이벤트 루프는 콜 스택에서 실행 중인 게 있는지 확인하고, Event queue에 작업이 있는지 확인해서 콜스택이 비어있다면 이벤트큐 내의 작업이 콜스택으로 이동되어서 실행된다.    
* 프로토타입이란   
자바스크립트는 프로토타입을 기반으로 상속을 구현하여 불필요한 중복을 제거(중복 제거 방법은 기존의 코드를 재사용하는것!!)   
즉, 생성자 함수가 생성할 모든 인스턴스가 공통적으로 사용할 프로퍼티나 메소드를 프로토타입에 미리 구현해 놓음으로써 또 구현하는것이 아니라 상위(부모) 객체인 프로토타입의 자산을 공유하여 사용할 수 있다.   
__proto__ 접근자 프로퍼티로 자신의 프로토타입, 즉 Prototype 내부슬롯에 접근 할 수 있음.   
프로토타입체인이란? 객체의 프로퍼티에 접근하려고 할때 객체에 접근하려는 프로퍼티가 없으면, __proto__접근자 프로퍼티가 가리키는 링크를 따라 자신의 부모역할을 하는 프로토타입의 프로퍼티를 순차적으로 검색한다. 프로로타입체인의 최상위 객체는 Object.prototype이다. 이 객체의 프로퍼티와 메소드는 모든 객체에게 상속된다.   
prototype 프로퍼티 는 생성자함수가 생성할 인스턴스의 프로토타입을 가르킨다.   

### Q this
* 일반함수의 this와 화살표 함수의 this는 어떻게 다른가?   
자바스크립트의 내부함수는 일반 함수, 메소드, 콜백함수 어디에서 선언되었든지 this는 전역객체를 가르킴
일반함수의 this는 window(전역)을 가르키며, 화살표 함수의 this는 언제나 상위스코프의 this를 가르킴   
* Call, Apply, Bind 함수에 대해 설명해라.   
3가지 방법은 this를 바인딩하기 위한 방법이다.    
Call은 this를 바인딩하면서 함수를 호출하는 것, 두번째 인자를 apply와 다르게 하나씩 넘기는 것   
Apply는 this를 바인딩하면서 함수를 호출하는 것, 두번째인자가 배열   
Bind는 함수를 호출하는 것이 아닌 this가 바인딩 된 새로운 함수를 리턴함.   
* use strict모드에서의 this는?   
일반함수에서의 this는 undefined가 바인딩 됨.   

### Q ES6
* 크롬 정도의 브라우저를 제외하곤 ES6 스펙에 대한 지원이 완벽하지 않다. 해결방법은 무엇인가.   
Babel을 사용한다. ES6이상의 문법의 코드들을 브라우저가 이해할 수 있게끔 ES5이하의 문법으로 변환해줌.   
* Babel이란   
    * babel은 컴파일인가? 트랜스파일인가?   
    트랜스파일러이다. 컴파일은 한 언어로 작성된 소스 코드를 다른 언어로 바꾸는것. 트랜스파일러는 한 언어로 작     성된 소스코드를 비슷한 수준의 추상화를 가진 다른 언어로 변환   
* ES6에서 추가된 스펙에 대해 아는대로 다 말하시오.   
let, const, 화살표함수, 클래스, 프로미스, 스프레드 연산자 등   
* var와 let, const의 차이점은 무엇인가   
* Class는 무엇이고, Prototype, function의 ES5 스펙만으로 Class를 구현할 수 있는가.   
구현가능하다. 자바스크립트에는 프로토타입이라는 것이 존재하여 클래스처럼 구현할 수 있다. 클래스는 자바스크립트의 프로토타입 기반 패턴의 문법적 설탕이다.

### Q 리액트의 상태관리에 대해 알고 있는가? Redux를 사용해봤다면, 그것에 대한 설명   
리액트에서 전역의 상태를 관리하기 위해서 사용하는 방법이다. 컴포넌트간의 상태들을 한군데다가 모아놓고 공유해서 사용하는 방식.    
리액트의 상태관리는 Context API, Redux, MobX 등의 상태관리가 있으며, Context API보다 Redux를 사용하는 이유는 대규모 개발에서 유지보수성이나 작업효율을 높이기에는 Redux를 사용하는것이 좋기 때문에 많은 사람들이 Redux를 사용한다. 리액트 16.3이후 버전에서는 그래도 Context API가 개선되어 사용하기 좋아졌다.   
Redux는 사실 다른 곳에서도 많이 쓰이는 기술이었지만, react-redux라는 것이 있어서 react에서 사용하기 좋아졌다. 
react-redux에서는 3가지 규칙을 지켜야하는데   

1. 단일 스토어야 할것   
1. 읽기전용상태여야 한다. 즉 기존의 객체는 건드리지 않고 새로운 객체를 생성해서 사용하여야한다.   
1. 리듀서는 순수한 함수여야한다. 즉, 파라미터 외의 값에는 의존하지 않아야한다.   

만드는 순서는 액션 타입을 정하고, 액션 생성 함수를 만들고, 이 액션들을 사용하는 리듀서 함수(초기상태 포함)를 만들고,  index.js에서 스토어를 만들어 provider로 스토어를 props로 전달해준다.    
프레젠테이셔널 컴포넌트와 컨테이너 컴포넌트를 분리하여, 컨테이너 컴포넌트에서 connect함수를 사용해서 mapStateToProps(스토어 안의 상태를 컴포넌트의 props로 넘겨주기 위해 설정하는 함수),
mapDispatchToProps(액션 생성 함수를 컴포넌트의 Props로 넘겨주기 위해 사용하는 함수) 
이 2가지를 다음과 같이 사용   
connect(mapStateToProps, mapDispatchToProps)(타깃컴포넌트)

### Q Context-API에 대해서 설명하세요.
리액트에서 전역상태를 관리하기 위한 기능

### Q 리액트에서 클래스형과 함수형의 차이는 무엇인가.
클래스형은 라이프사이클 메소드를 사용하고, 함수형에서는 useEffect등 Hook을 사용한다.   
클래스형은 render함수가 반드시 필요, 함수형이 선언하기 더 간편하다.   

### Q 라이프 사이클 메소드에 대해서 설명하세요.
클래스형에 라이프사이클 메소드에는 크게 mount, update, unmount 3가지 과정으로 나뉜다. 자세하게는    
constructor -> getDerivedStateFromProps -> render -> componentDidMount ->    
getDerivedStateFromProps -> shouldComponentUpdate -> render -> getSnapshotBeforeUpdate   
-> componentDidupdate    
mount에서 컴포넌트가 만들어질때 componetDidMount에서 비동기처리 같은것을 주로하고, shouldComponentUpdate에서 업데이트 직전에 랜더링시(상태가변경)에 조건으로 재랜더링을 하냐마냐 결정을 할 수 있고, componentDidUpdate 업데이트 직후에 호출되는 메소드이고 unmount에서 컴포넌트가 소멸된 시점에 타이머나 비동기 API를제거 하는 곳이다. 

### Q 타입스크립트를 사용해본 경험이 있는가, 타입스크립트에 대한 본인의 생각과 도입시의 장점을 말해달라.
Typescript는 동적타입언어인 Javascript의 약점을 보완하기 위해서 타입을 지정해주는 것이다.    
타입이 필요한 이유는 결론은 메모리를 절약하기 위해서이다. 메모리에 저장된 것을 읽어들일때, 값을 메모리에 저장할때, 값이저장되어있는 것을 참조할때의 크기들을 알아야 하기 때문이다.   
또한, 에러를 잡기가 쉬워지고, 다른 동료와 협업 할때 코드의 예측도 가능해지고, 코드에디터의 도움을 더 받을 수 있다. 리액트의 경우 (브라우저는 javascript밖에 모르기떄문에) tsx파일을 javascript로 변환하는 트랜스파일링이 필요하다. 이때 변환하는 과정에서 에러를 잡을 수 가있다. 런타임에 오류를 잡는 것보다 훨 좋다!   
또한, Babel을 안써도 된다.   

### Q Angular와 React의 차이점은 무엇인가.
우선 Angular는 프레임워크이고, React는 라이브러리이다.   
Angular는 양방향 바인딩개념으로 Model과 view가 연결되어있어 데이터 값이 한쪽에서 변화하면 다른쪽에서도 바로 업데이트가 진행된다. 서비스라는 개념은 컴포넌트간의 의존성관리를 용이하게 해준다. Directive를 이용하여 커스텀 HTML태그를 작성할 수 있다.    
React는 Virtual DOM을 가지고 있다. 가상 DOM이 있기때문에 상태를 비교하여 부분적으로 랜더링 할 수 있어 속도가 빠르다. 오직 UI컴포넌트를 만들기 위한 라이브러리이다.    
Angular는 HTML스크립팅이 templete 기반, React는 JSX 이용 / Angular는 기본이 Typesciprt   

### Q 라이브러리와 프레임워크에 대해서 설명하시오.
라이브러리와 프레임워크의 차이는 자유도 차이 인것 같다. 프레임워크는 짜여짐 패턴이나 틀 기반에서 내가 코딩을 하는 것이고, 라이브러리는 내가 가져다 사용해서 자유롭게 사용하는 방식이다.

### Q 라이브러리와 프레임워크에 대해서 설명하시오.
라이브러리와 프레임워크의 차이는 자유도의 차이 인것 같다. 프레임워크는 짜여진 패턴이나 틀 기반에서 내가 코딩을 하는 것이고, 라이브러리는 내가 가져다 사용해서 자유롭게 사용하는 방식이다.   

### Q 두 명의 프론트엔드 개발자가 있다 git을 관리하는 방식은?
git repository를 하나파서 다른 동료가 fork를 해서 사용하는 방식. PM과 팀원의 구조를 가질 수도있고 동시에 Pull request를 가능하게끔 권한을 줄 수 도 있다. 각자의 팀장의 레포가 origin이라하고, 팀원의 포크딴 레포를 rmorigin이라고 한다면 각자의 origin에서 develop브랜치에서 작업을 한뒤 최종 작업이 완료되면 팀장의 origin의 마스터로 push한다. 

### Q 메소드 체이닝이란 무엇이며, 이것의 장단점은 무엇인가?
메소드 체이닝의 장점은 코드가 짧아진다는 장점이 있고, 단점은 에러가 났을때 어느 부분의 메소드에서 오류가 났는지 확인이 어렵다.

### Q 메모라이제이션이란?
메소드 체이닝의 장점은 코드가 짧아진다는 장점이 있고, 단점은 에러가 났을때 어느 부분의 메소드에서 오류가 났는지 확인이 어렵다. 

### Q 메모라이제이션이란?
불필요한 연산이나 계산을 하지 않고 기억을 해놓고 그 기억해놓은 것을 활용한는 방법

### Q Restful API가 무엇인가, 아는대로 다 말해달라
REST API는 URI로 접근가능하고 내용이 JSON,XML 등으로 표현된 자원에 대한 행위를 HTTP Method로 정의한다.   
RESTful하다라는 것은 REST API의 설계의도를 명확하게 지켜주는 것이다. 슬래시를 통해 계층관계를 표시한다던가 숫자는 id를 나타낸다든가 동사보단 명사를 위주로 쓴다든가 하는.

### Q CORS(Cross-Origin Resource Sharing)는 무엇인가 왜 이러한 방법이 정의 되었으며, 본인이 코드를 작성하면서 CORS와 관련하여서 경험하였던 이슈는 무엇인가.
CORS란 도메인 또는 포트가 다른 서버의 자원을 요청하면 발생 하는 문제    
경험 많음.   
웹 프론트 측에서 request header에 CORS 관련 옵션을 넣어주고, 서버에서는 해당 프론트 요청을 허용하면 됨(주로 cors라이브러리를 사용해서 해결)

### Q Eslint가 무엇인가.
Eslint는 소스코드를 스캔하여 문법적오류나 잠재적 오류까지 찾아내고 오류의 이유를 볼 수 있게 해주는 도구

### Q Prettier가 무엇인가.
prettier는 정해진 규칙대로 코드를 이쁘게 할 수 있는 도구, 들여쓰기나 따옴표 등

### Q WebPack이란
webpack은 모듈 번들러로 파일 확장자에 맞는 로더에게 위임해서 하나로 묶어준다 최종 배포용 파일을 만들어줌
'<script>'태그가 여러개 있을 때 순서보장도 중요하기 때문에 이런것도 Webpack에서 해줌.   

### Q 패키지매니저로 주로 어떤거 사용하는지, npm과 yarn은 어떤게 다른가.   
주로 yarn을 사용하며 배포시 puuty에서는 npm을 사용한다. 과거 깃허브에서 받은 소스코드를 npm i로 패키지를 설치 했을 때 이전과 버전정보가 다른 환경문제가 생길 수 있었는데 이것을 처리하기 위해서 yarn.lock 파일에서 처리할 수 있었다. 하지만, 현재는 npm의 package-lock.json에서 이 처리를 동일하게 사용할 수 있다.   

### Q 배포를 해본적이 있는가, 어떻게 배포를 해보았나.
yes

### Q 적응형과 반응형의 차이는?
반응형 웹은 하나의 템플릿을 사용해 모든 기기에 대응하는데 반해, 적은형 웹은 선별된 기기 유형에 따라 별도의 독립적인 템플릿이 요구된다.

### Q package.json파일의 역할은?
패키지의 버전을 관리하는 파일이다.

### Q package.json에서 dependencies와 devDependencies의 차이는?
"dependencies": 프로덕션 환경에서 응용 프로그램에 필요한 패키지.   
"devDependencies": 로컬 개발 및 테스트에만 필요한 패키지.   

### Q 프로세스와 스레드의 차이
프로세스는 운영체제로부터 자원을 할당받는 작업의 단위이고 스레드는 프로세스가 할당받은 자원을 이용하는 실행 단위이다. 멀티프로세싱보다 멀티스레딩을 하는 이유는 운영체제로부터 자원을 할당 하는 프로세싱 작업을 많이 하는 것 보다 스레딩을 여러개 하는것이 훨씬 더 시스템 자원을 효율적으로 관리할 수 있다.   

### Q CSR과 SSR의 차이
CSR의 과정 :   
  - 서버가 브라우저에게 응답을 보냄 -> 브라우저는 JS를 다운 받음 -> 브라우저는 리액트를 실행 -> 페이지가 보여지고 상호작용 함   
SSR의 과정 :   
 - 서버가 브라우저에게 HTML 응답 랜더링하기 위한 준비가 되었다고 보냄 -> 브라우저가 페이지랜더링, 페이지가 보여지고 브라우저는 JS 다운받음 -> 브라우저 리액트 실행 -> 페이지 상호작용 가능   

CSR은 마지막 단계 전까지 화면에 보여지지가 않고 로딩중 / SSR은 미리 페이지가 보여진다.   
즉, CSR은 초기로딩속도가 느리긴하지만, 화면전환에 있어서 클라이언트에서 이루어져서 빠른 전환이 가능
SSR은 초기로딩속도가 빨라서 사용자가 느끼기엔 좋지만, 동작은 하지않음. 그리고 화면전환에 있어서 서버에 요청해야하므로 서버에 부담을 줄 수 있음.     
어떤게 더 좋다보다 서비스마다 사용자의 요구마다 다름.   

### Q 이벤트 위임이란
이벤트 위임이란 자식 엘리먼트의 이벤트를 부모엘리먼트에서 감지할 수 있으니 이벤트를 하나하나 등록 하는 것이 아니라 부모에게 이벤트를 위임 하는 방법

### Q DOM을 건드리는 방식과 아닌 방식들의 차이
직접 DOM을 건드리는 경우 DOM의 구조를 파악하고 있어야하며, 클래스명이다 태그명이 바뀌는 경우 다시 DOM을 변경해야한다.    
Angular의 경우 view와 model을 연결시키는 바인딩작업이 있고 변화감지를 통해서 상태를 보고 있다가 업데이트되는식이다.    
React의 경우 가상 DOM이 있고, 가상 DOM이 실제 DOM과 비교하여 state가 변화되었는지 감지 한다.   

### Q 반응형 프로그래밍이란.
반응형 프로그래밍이란 데이터 스트림이라는 하나의 일관된 형식으로 만들고, 이 데이터 스트림을 구독하여 데이터 스트림의 상태 변화에 반응하는 방식으로 동작하는 애플리케이션을 만드는 것. 예를들어, Tv랑 Tv방송국이 있다고 가정했을때, Tv방송국이 일정한 시간 단위로 영상에 대한 프레임을 계속해서 방출(emit)하고 TV는 방송국을 관찰하고 있다가 새로운 영상을 방출하면 이를 획득하는 방식이다. 여기서 방송국의 역할이 옵저버블, Tv가 옵저버, 영상프레임이 Notification이다.

### Q inline vs inline block
inline은 text크기만큼만 공간을 점유하고 줄바꿈을 하지않음.   
inline-block은 inline속성과 block속성의 특징을 둘다 가지고 있다. inline속성과 다르게 width,height 적용 가능하고 line-height를 커스텀하게 적용할 수 있다.

### Q 가상돔(virtual DOM)
Virtual DOM은 실제 DOM 변화를 최소화 시켜주는 역할을 합니다.   
먼저 브라우저는 HTML 파일을 스크린에 보여주기 위해 DOM 노드 트리 생성, 렌더트리 생성, 레이아웃, 페인팅 과정을 거칩니다. DOM 노드는 HTML의 각 엘리먼트와 연관되어 있기 때문에 HTML 파일에 20개의 변화가 생기면 DOM 노드가 변경되고 그 이후의 과정역시 20회 다시 이루어 집니다. 작은 변화에도 매우 복잡한 과정들이 다시 실행되기 때문에 DOM 변화가 잦을 경우 성능이 저하됩니다.   
Virtual DOM은 뷰에 변화가 있다면, 그 변화가 실제 DOM에 적용되기 전에 Virtual DOM에 적용시키고 최종 결과만 실제 DOM에 전달합니다. 따라서 20개의 변화가 있다면 Virtual DOM은 변화된 부분만 가려내어 실제 DOM에 전달하고 실제 DOM은 그 변화를 1회로 인식하여 단 한번의 렌더링 과정만 거치게 됩니다.

### Q URL과 URI 차이
* URI(Uniform resource Identifier) 네트워크 상에서 자원 위치를 알려주기 위한 규약. URI의 존재는 인터넷에서 요구되는 기본조건으로서 인터넷 프로토콜에 항상 붙어 다닙니다.   
* URL(Uniform Resource Locator) 통합 자원 식별자로 인터넷에 있는 자원을 나타내는 유일한 주소.   
* URI가 URL의 상위 개념. (URL이 URI안에 포함 되어있다고 생각하면 될것 같습니다. URI 의 하위 개념으로는 URL 말고 URN도 있음.)   

https://example.com 의 경우 https://example.com 이라는 서버를 나타내기 때문에 URL이면서 URI   
https://example.com/skin 의 경우 example 서버의 skin이라는 인터넷상의 자원의 위치를 의미하기에 URL 이면서 URI   
https://example.com/one/two/abc.html 의 경우 example 서버의 one/two 디렉토리 아래의 abc.html을 가리키므로 URL이면서 URI   
https://example.com/123 의 경우 좀 다르다. 여기서 URL은 https://example.com까지이고, 내가 원하는 정보에 도달하기위해 123이라는 식별자가 필요하다. 즉, URI 이지만 URL은 아닌 것이다.   
https://example.com/one?id=123 의 경우도 마찬가지로 URL은 https://example.com/one 까지이고 내가 원하는 정보에 도달하기 위해서는 ?id=123이라는 식별자가 필요한 것이다. 이또한 URI이지만 URL은 아닌것.

### Q float를 해제하는 방법에 대해서 아는대로 설명하세요.
float란 '뜨다'라는 단어를 뜻하며 사용용도는 이미지를 어떻게 띄어서 텍스트와 함께 배치할 것인지 정하는 속성이다.   
inherit: 부모 요소에서 상속   
left: 왼쪽에 부유하는 블록 박스를 생성. 페이지 내용은 박스 오른쪽에 위치하며 위에서 아래로 흐름.   
right: 오른쪽에 부유하는 블록 박스를 생성. 페이지 내용은 박스 왼쪽에 위치하며 위에서 아래로 흐름. 이후 요소에 clear 속성이 있으면 페이지 흐름이 달라짐. none 이 아니라면 display 속성은 무시된다.   
none - 요소를 부유시키지 않음   
left와 right를 통해 부유속성을 지정시 display는 무시됩니다. (none은 제외)   
또한 이후 요소에 clear 속성이 있으면 페이지 흐름이 달라집니다.   
다만 레이아웃을 설정하는 float 속성에서 페이제의 원래의 흐름이 달라지게 되고 이를 해제하는 방법이 있는데 clear속성을 이용한다.   

* float 해제하는 방법   
1. float된 요소의 부모태그에 강제로 높이 값을 지정해준다.(단점: 반응형시 자동 높이 값 설정 불가)   
1. float된 요소의 부모태그에 overflow:hidden을 적용해준다.(단점: 해당 요소 안의 컨텐츠를 박스 외부로 표현해줄 수 없음)   
1. float된 요소의 부모태그에 overflow:auto를 적용해준다.(단점: 특정 브라우저에서 스크롤 바가 표시됨)   
1. float된 요소의 부모태그에 float을 또 설정해준다.(단점: 가운데 배치 불가능)   
1. float된 요소의 다음에 나오는 태그에 clear:both를 지정합니다.(단점: clear:both가 적용된 요소에는 margin-top 적용 불가)   
1. float된 요소의 부모태그에 가상요소를 만들고 해당 요소에 clear:both를 지정해준다.

### Q HTML5에 들어와서 doctype이 어떻게 간결화 되었는지 설명해주세요.
html의 뼈대를 만드는 과정에서 가장 먼저 등장하는 코드는 HTML, HEAD, BODY태그가 아닌 DOCTYPE이다. HTML을 통해 '뼈대'를 구성한다고 했는데, 그 뼈대는 브라우저 상의 화면에 렌더링 되는 것을 의미한다. HEAD 태그의 내용들은 보통 화면단에는 출력되지 않아도 이 문서가 어떻게 해석될 것인디, 어떤 뷰 포트를 가질 것 인지 어떤 제목을 가질 것인지를 나타낸다. BODY태그 내에 내용들은 사용자에게 출력된다. 그렇다면 브라우저에게, 이 문서가 HTML 문서이며, 버전은 5이다를 알려줄 필료가 있다. 그래서 HTML5에 간략화된 '<!DOCTYPE html>'을 통해서 HTML로 작성하였으며 버전은 5이다를 브라우저에게 알려준다. 최상단에 DOCTYPE이 존재하지 않게 되면 예상과 다르게 브라우저에 출력될 수 있을것이다.   
HTML4에서 HTML5로 넘어오면서 왜 간략화되었을까?   
HTML5이전 버전에서는 모드별로 다른 모드를 제공했는데 엄격모드, 호환 모드, 프라임셋 모드 등이 존재했다. HTML5에 들어와 그전 버전에 비해 엘리먼트, 어트리뷰트, API 등이 추가되었고 DOCTYPE도 포함하여 간략화됐다는게 특징이다. 추측으로는 과거 브라우저들은 통일성이 없었고 '표준'이라는 개념이 없었다면 현대의 브라우저들은 차이점은 존재하되 표준이라는 기준점을 세운 것 같다. 그리하여 DOCTYPE html로 간략화되고 표준호환 모드를 지원하게 되어 신경 쓸 부분을 줄일 수 있게 됐다. 이는 개발자의 생산성 향상에 많은 영향을 미쳤다고 판단된다.

### Q REALDOM, VIRTUALDOM 각각 설명하시오.
Realdom 은 문서객체모델로, xml, html 문서를 위한 API 이다. Virtualdom 은 실제 돔을 추상화한 객체를 조작한다.

### Q 버츄얼돔은 왜 좋은가. 어떻게 동작하는가. JQUERY의 돔 직접참조에 비해서 무엇이 개선되었는가.
Realdom은 동적으로 조작하기 어렵다. HTML 문서는 정적이기 때문에, js로 동적으로 움직이게 한다. jquery는 직접 돔을 수정한다. dom 은 트리구조이므로, 노드를 추가/삭제하는 경우 그 하위 노드들을 다시 정렬해야한다. 돔을 여러 번 수정하는 경우 성능이슈가 발생할 수 있다.    
virtual Dom은 수정될 내용을 처리하여, 리얼돔에 덮어씌운다. 여러 번 수정하더라도, 비교하여 바뀐 부분만 실제 dom 에 적용한다. dom 관리가 더 쉬워진다.   

### Q 버츄얼돔이 동작하는 DIFF알고리즘에 대해 설명하시오.
수정 정 버츄얼돔과 수정 후 돔을 비교(DIFF)하여, 수정 된 부분만 실제 돔에 적용하는 것이다. 하나의 앱에서 여러 개의 컴포넌트는 독립적으로 작동되고, 분류, 이동된다. 이로인해 컴포넌트는 부모 컴포넌트가 수정될 때, 값이 변경될 때 리렌더링된다.

### Q props 와 state는 언제 쓰는가
1)	Props   
부모 컴포넌트가 자식 컴포넌트한테 전달하는 데이터로, (자식 입장에서)읽기 전용이다.   

2)	State   
자신이 들고 있는 값을 말한다. (읽기 전용인 props와 비교해보자면, 쓰기 전용이라고 볼 수 있겠다) 

### Q Hook과 mobx는 무엇이고 왜 쓰는가
1)	Hook   
클래스형 컴포넌트를 사용했던 이유는 state관리와 life cycle method의 사용때문이었다. 복잡하고 뚱뚱하지만 클래스의 힘을 빌려야만 React가 원활하게 작동할 수 있었던 것이다.   
그런데 hooks의 등장으로 인해 함수형 컴포넌트에서도 이러한 클래스형 컴포넌트의 작업들을 할 수 있게 되었다. 기존의 클래스형 컴포넌트가 가지고 있던 복잡성, 재사용성의 단점들까지 해결했다. 특히나 OOP를 선호하지 않는 개발자에게 있어서 React를 함수 중심으로 사용할 수 있게 되었다는 것은 매우 큰 장점이다.   

2)	Mobx   
Mobx는 프론트엔드를 위한 어플리케이션 상태 관리 라이브러리다. 주로 React와 함께 사용되며, 상태 관리 라이브러리라는 특성 때문에 종종 Redux와 비교된다. 한마디로 말해, Mobx는 상태를 Observable하게 관리할 수 있도록 돕는 라이브러리다

### Q 순수함수란 무엇인가.
순수 함수란 동일한 인자를 넣었을 때 항상 동일한 리턴값을 반환하고 외부에 영향을 받지 않는 함수를 말한다.

### Q 서버사이드 렌더링이란 무엇인가.
어떠한 웹 패이지 접속시, 그 페이지를 화면에 그려주는 것. 요청시마다 새로고침이 일어나며 서버에 새로운 페이지에 대한 요청을 하는 방식이다.   
이때, view가 어떻게 보여질지 또한 서버에서 해석하여 보내주는데, 이러한 방식을 서버사이드 렌더링 방식이라고 한다.

### Q SPA란 무엇이고 어떤 장점이 있는가.
단일 페이지 어플리케이션 줄여서 SPA는 현재 웹개발의 트랜드가 되는 차세대 패러다임이다. 전통적인 웹은 요청시마다 새로고침이 일어나며 페이지가 로딩될때마다 서버로부터 리소스들을 전달받아 해석한뒤 화면에 랜더링 하게된다. 그러나 전통적인 방식의 웹은 현재의 풍부한 웹환경을 표현하기에 속도적인 측면에서 많은 리스크를 가지고있었고 이를 해소하기위해 캐싱과 압축이라는 방식으로 어느정도 해소하였지만 결국 브라우저는 모든 CSS, 자바스크립트, HTML을 해석한뒤에 이들을 화면에 렌더링한다. 단일 페이지 어플리케이션은 브라우저에 로드되고 난 뒤에 페이지 전체를 서버에 요청하는 것이 아니라 최초한번 페이지전체를 로딩한 후 이후부턴 데이터만 변경해서 사용할 수 있는 웹 어플리케이션을 말한다. 개발자들은 단일 페이지 어플리케이션을 만들기 위해 Backbone.js, Angular.js등의 자바스크립트 라이브러리를 사용한다.   

### Q Npm 옵션 중 –g, --save의 의미는 무엇인가.
뒤에 –save 또는 –S를 하면 dependencies에(npm5부터는 --save옵션이 기본적으로 설정되어 있기 때문에 안 붙여도 된다), --save-dev 또는 -D하면 devDependencies에 추가 된다. 그리고 –g를 하면 글로벌 패키지에 추가된다. 글로벌 패키지에 추가하면 이 프로젝트뿐만 아니라 다른 프로젝트도 해당 패키지를 사용할 수 있다.

### Q 리액트 클래스구조에서 export, import의 의미는 무엇인가.
export문은 지정된 파일(또는 모듈)에서 함수 또는 오브젝트, 원시 타입들을 export하는데 사용된다.   
import문은 외부 모듈이나 다른 스크립트 등으로부터 export된 기능을 가져오는데 사용된다.   

### Q Non blocking과 blocking을 설명하시오.
-	Non-blocking이란, 어떤 쓰레드에서 오류가 발생하거나 멈추었을 때 다른 쓰레드에게 영향을 끼치지 않도록 만드는 방법들을 말한다.1 공유 자원(메모리, 파일 등)를 사용하는 멀티 쓰레드 프로그래밍을 할 때, 특정 공유 자원을 사용하는 부분에서 뮤텍스나 세마포어 등을 사용하여 여러 쓰레드에서 동시에 접근하지 못하도록 개발자가 보장하는 것이 전통적인 방법이었다. 반면 Non-blocking algorithm(Wait-freedom, Lock-freedom 등)을 사용하면 공유 자원을 안전하게 동시에 사용할 수 있다.(장점 : 네트워크 통신이 완료될 때까지 기다리지 않고 다른 작업을 수행할 수 있으므로 경우에 따라 효율이나 반응속도가 더 뛰어나다. 단점 : 설계가 복잡해진다.)   
-	blocking이란, 네트워크 통신에서 요청이 발생하고 완료될 때까지 모든 일을 중단한 상태로 대기해야 한는 것을 블로킹 방식이라 한다. 블로킹 방식의 소캣통신은 결과가 올 때까지 다른 작업을 중단하고 하염없이 기다린다.

### Q 콜백함수란?
콜백 함수는 함수 안에서 어떤 특정하 시점에 호출되는 함수를 말합니다. 보통 콜백 함수는 함수의 매개변수로 전달하여 특정 시점에서 콜백 함수를 호출합니다. 

### 기타
* 왜 개발자가 되려고 하는가   
* 개발자로서의 본인의 비전을 이야기 해달라   
* 비전공자로써 갖고 있는 컴플렉스가 있는가   
* 운영체제같은 컴퓨터공학(cs)에 대한 기초지식이 있는가   
* 최근에 관심갖거나 공부 하고 싶은 개발 기술은 무엇인가   
* 프로젝트 협업 과정을 경험한 적이 있는가   
* 공부 방법   
개발자가 되기 위해서 어떻게 공부하였는가   
학습시 주로 이용하는 웹페이지나, 동영상 강좌 페이지는 어디인가   
최근의 읽은 개발 관련 서적은 무엇인가   
즐겨 보는 개발 관련 유튜브가 있는가   
회사 기술 스택에 맞추어 단기간 내에 언어와 프레임워크를 학습 하여야 할 때, 어떻게 공부하고 해결할 것인가   
* 포트폴리오 제작시에 비인기 라이브러리를 사용한 경험이 있는가      
* 이러한 비인기 라이브러리에 대한 정보를 어디서 얻는가 왜 활용하였는가
