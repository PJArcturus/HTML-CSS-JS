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
    - HTML / CSS / JS 종합 활용
    - HTML DOM
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

- 반복문
    - for
    - while

### 함수

### 배열 / 객체 / Class

### 추가 문법

## JS 활용