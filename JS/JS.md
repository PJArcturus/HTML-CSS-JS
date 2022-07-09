# JavaScript
- 문법
    - JavaScript 언어 문법
    - 문법의 내용
        - 데이터 / 변수 / 연산자
        - 명령문
        - 함수
        - 배열 / 객체 / Class
        - 추가 문법

- 활용
    - HTML DOM
    - HTML / CSS / JS 종합 활용
    - Open API: 객체와 연결

## JS Basic
- version
    - ES5
    - ES6

- 작성방식
    - External: JS 파일 생성
    - Internal
        - HTML 파일에 JS 코드를 작성
        - JS 코드 블럭을 따로 구분해서 작성
    - Inline
        - HTML Tag에 JS 코드를 작성
- 작성 위치
    - JS가 실행되는 시점에 HTML이 로딩(렌더링)되어 있어야 한다.
    - JS가 실행되는 방식: 최초 한번만 실행됨

## JS 문법

### 데이터 / 변수 / 연산자
- 데이터
    - 숫자
    - 문자
```
숫자: 0, 1, 2, 3, 4, 5 ...
문자: 가, 나, 다..., a, b, c...
```
- 데이터 타입(종류)
    - 숫자: 정수, 실수 ... 
    - 문자
        - 코드상에서 문자는 따옴표로 묶임
        - 낱개 글자, 묶음 글자...
    - Boolean(논리값)
        - True: 참
        - False: 거짓
```
1 + 1 = 2

'a' + 1 = a1

'1' + 1 = 11
```

★★ JavaScript는 데이터 타입을 업격하게 구분하지 않음 ★★ 

- 변수(Variable)
    - 데이터를 저장하는 공간
    - 변수는 선언(정의) 한 이후에 사용
    - 변수 선언 예약어(Keyword)
        - var(ES5): 타입 구분 안함, 데이터 변경 자유로움
        - let(ES6): 타입 구분 안함, 데이터 변경 자유로움
        - const(ES6): 타입 구분 안함, 데이터 변경 불가

```
JAVA
정수 변수 선언: int number1;
실수 변수 선언: float number2;
문자 변수 선언: char text;

ES5 / ES6
정수 변수 선언: var number1; | let number1;  | const number1;
실수 변수 선언: var number2; | let number2;  | const number2;
문자 변수 선언: var text;    | let text;     | const text;
```

- 연산자

- 산술 연산자
    - +, *, −, /
    - %: 나머지 연산

- 할당(대입) 연산자
    - =: 값을 변수에 저장

```
const PI = 3.141592;
```

- 산술 + 대입연산(재귀)
```
let a = 10;

a = a + 5

a += 5
```

★★ 산출, 대입 연산어 반복 실행되면 일정 값을 지속적으로 연산

- 카운터

```
a += 1 => a++
a -= 1 => a--
```

- 비교연산자
    - ==, === : 같음
    - !==, !=== : 다름
    - 비교 연산자를 사용한 식의 결과는 참 또는 거짓으로 표현

- 논리연산자
    - 논리값(참/거짓)을 연산
    - AND: && - 연산하는 여러개의 논리값 중 모두 참이어야 연산결과가 참
    - OR: || - 연산하는 여러개의 논리값중 모두 거짓이어야 연산결과가 거짓
    - NOT: ! -  연산 결과의 반대값 표시

### 명령문

- 프로그래밍 언어의 실행 흐름을 변경
- 조건문 / 분기문
    - if: 조건/상황에 대한 다른 결정에 대해 각각 다른 실행방식을 선택
        - if
        - else if
        - else
```
if(결과값이 bool 데이터인 식){
    결과 값이 참일 때 실행코드
}


if(bool1){
    bool1이 참일 때 실행코드
} else if(bool2){
    bool2가 참일 때 실행코드
}


if(bool) {
    bool이 참일 때 실행코드
} else {
    bool이 거짓 일 때 실행코드
}


if(bool1){
    bool1이 참일 때 실행코드
} else if(bool2){
    bool2이 참일 때 실행코드
} else {
    bool1, bool2 모두 거짓일 때 실행코드
}
```
```
if(a>10){}
if(true){}
if(a+1)(): 값이 숫자 - 0: false, 정수: true
if(1){}
```
    - switch: 
        - 식의 결과값에 따라 실행 분기
```
let a = 0;
switch(a+1) {
    case 1:
        실행 코드
        break;
    case 2:
        실행 코드
        break;
}
```

- 반복문
    - for: 결정된 반복횟수 만큼 반복 실행하는 구문
        - 구문1, 구문2, 구문3이 유기적으로 연결되어 반복횟수를 결정
    ```
    for(초기값 구문1; 비교식 구문2; 수식 구문3){
        반복 실행 코드
    }

    1) 초기값 구문1이 최초 한번 실행
    2) 비교식 구문2 실행 -> 참 또는 거짓 -> 거짓: 반복구문실행 종료
    3) 참일 때 실행코드가 실행
    4) 수식 구문3 실행
    5) 2)부터 반복 실행
    ```

    ```

    // i=i+1 => i+=1 => i++

    for(let i=0; i>3; i++){
        코드블록
    }

    1. i=0
    2. i<3 => true
    3. 코드블록 실행
    4. i++ => i=1
    ```

    ```
    for(let i=0; i<5; i++){}: 5번 반복
    for(let i=1; i<=5; i++){}: 5번 반복
    for(let i=0; i<10; i+=2): 5번 반복
    ```

    - while
        - 조건식의 결과값이 참 일때 반복 실행
    ```
    while(조건식) {
        실행 코드
    }

    조건식의 결과값이 참 일때 계속 반복 실행
    ```
### 함수

- 특정 작업을 실행할 수 있도록 만들어진 코드 블럭
- 함수 하나가 독립적으로 실행될 수 있음
- 코드를 그룹화
- 함수를 실행하기 위해서 해당 함수를 호출
- 매개변수: 외부로부터 값을 받아서 실행할 때 사용하는 변수


### 배열 / 객체 / Class

- 집합 형태의 데이터

#### 배열

- 같은 타입의 데이터들을 나열해서 패키지화 한 것
```
let array = [1, 2, 3, 4, 5]

let arr = [1, 2, 3, 4, "a"]

```

#### 객체

- 어떤 대상을 데이터화 시킨 집합 데이터

객체 데이터
- Property: 객체 데이터화 시킨 것, 객체가 가지고 있는 
- Method: 객체에 포함된 함수, 기능 정의

#### Class

- 객체 데이터를 만들 수 있게 하는 설계도

### 추가 문법

#### 변수 Scope

- Scope
    - Global Scope
        - 변수는 모든 범위에서 접근 가능
    - Function Scope
        - 해당 함수 범위에서만 접근 가능
    - Block Scope
        - 해당 블록 범위에서만 접근 가능

```
<script>
// Global Scope

let a = 1;
var _a = 1;

function myFunction() {
    //function scope

    let b = 2;
    var _b = 2;

    for(statement) {
        // block scope()
        
        let c = 3;
        var _c = 3;
    }
}

if(condition) {
    // block scope(2)

    let d = 4;
    var _d = 4;
}

</script>
```

## JS 활용

- 데이터 입출력
- UI 효과

### HTML DOM

- DOM(Document Object Model): HTML Element들을 객체화 시킨 모델
- HTML DOM을 사용하여 HTML Element를 제어

### DOM 접근 API(Application Programming Interface)

- API: DOM 객체 메소드

```
HTML4
document.getElementById("id"): id로 DOM 접근
document.getElementsByClassName("class"): class로 DOM 접근
document.getElementsByTagName("tag"): tag로 DOM 접근


HTML5
document.querySelector("#id")
document.querySelector(".class")
document.querySelector("tag")

document.querySelectorAll(".class")
document.querySelectorAll("tag")
```