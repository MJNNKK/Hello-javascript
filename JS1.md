# 1강 자바스크립트로 무엇을 할 수 있나?

## 자바스크립트로 할 수 있는 것들

- 자바스크립트는 HTML을 제어할 수 있다.


### 첫 번째 프로그램
- ex1.html 을 작성하고 크롬 브라우저로 연다.
<!--
<!DOCTYPE html>
<html>
<body>
<h2>자바스크립트 연습장</h2>
<p id="demo">지금은 몇시인가요?</p>
</body>
</html>
-->


- 개발자 도구 - 콘솔에서 아래 명령을 실행<br/>
var demo = document.getElementById('demo');<br/>
demo.innerHTML = Date();

### 두 번째 프로그램
demo.style.color = "red";<br/>
demo.style.background = "black";

### 세 번째 프로그램
var demo = document.getElementById('demo');<br/>
var size = 10;<br/>
function big() {<br/>
    demo.style.fontSize = size + "px";<br/>
    size = size + 1;    <br/>        
}<br/>
var tid = setInterval(big, 100);






# 2강 자료형

## 자료형이란?

- 어떤 종류의 데이터를 사용하는 것인지 컴퓨터에게 알려주는 것
- 자료형마다 사용 가능한 연산자(Operator)를 따로 가지고 있습니다.
- 자료형이 같아야 연산을 할 수 있습니다!

## 자료형의 종류

Number<br/>
String<br/>
Boolean<br/>
Null<br/>
Undefined

- 그리고 하나의 객채가 더 있습니다.
Object<br/>

## Number Type

- 정수와 실수는 모두 Number 타입입니다.
5;<br/>
3.0;<br/>
-4.8

## 숫자의 연산자

- 4칙연산, 괄호, 나머지 등이 있습니다.
+, -, /, *, (, ), %

## 문자열

"I am string";<br/>
"Hello " + "world";<br/>

- 문자열에도 +가 됩니다.(참고로 문자열은 "Immutable" 특징을 가집니다.)

## typeof 연산자

- 데이터 유형을 알려주는 중요 연산자!!
typeof 5;<br/>
typeof -4.8;<br/>
typeof "5";

## 생각해보기

5 + 4;<br/>
5 + "4";<br/>
5 * "4";

## 불리언

ture;<br/>
false;<br/>
5 > 3;<br/>
5 == 5;<br/>
5 > 5;

## 논리연산자

- 논리연산자에는 &&, ||, ! 등이 있다.
ture;<br/>
!ture;<br/>
ture && false;<br/>
ture || false;






# 3강 변수

## 변수란?

- **데이터(값)을 담을 수 있는 그릇**입니다. 데이터들은 컴퓨터 메모리 어딘가에 저장되는데 그<br/>
**값들을 구별짓고 재사용 하기 위해서 변수를 씁니다.**

## 변수 선언하기

- 변수를 사용하기 위해서는 먼저 선언이 필요합니다.<br/>
var a;<br/>

## 변수와 대입 연산자

- 변수에 값을 넣고 싶을 때 = 연산자를 사용한다! =는 수학에서의 같다가 아니라 변수에 값을 할당할 때<br/>
사용하는 대입연산자 입니다. 같다는 주로 ===를 사용합니다.

## 변수 사용하기

- 여러가지 방식이 있습니다. 차근차근 이해해 봅시다.
var a = 7;<br/>
var b = 10;<br/>
var c = a + b; //17<br/>

- 아래의 내용이 어렵다는 분들이 많습니다. 어떤 뜻일까요?<br/>
b = b + 1;

## 변수 이름 잘 짓기

- 변수의 이름은 매우 중요합니다. 일반적으로는 소문자로 시작, 영어, 숫자, _를 주로 사용합니다. 카멜케이스나<br/>
스네이크 케이스 표기법을 사용

### 카멜 케이스
nonenumPeoplenone

### 스네이크 케이스
nonenum_Peoplenone






# 4강 연산자 및 기타

## 증감연산자

- C언어의 잔재인데 조금 쓸데없이 복잡합니다. 우리는 a++; 스타일만 사용합시다.<br/>
var a;<br/>
a++;<br/>
a = 0;<br/>
a++;<br/>
a--;

## 비교 연산자

- 비교 연산자를 수행한 결과값은 Boolean입니다. 비교 연산자에는 >, <, >=, <=, ===, != 등이 있습니다.<br/>
var a = 3;<br/>
var b = 5;<br/>
var c = "5";<br/>
a > b;<br/>
a < b;<br/>
b === c;

## 문자열의 길이 구하기

var a = "hello"<br/>
a.length;

## 문자열 간단히 조작하기

var a = "KheLLo"<br/>
a[0];<br/>
a[1]; = "H"; //안 됨<br/>
a.slice(1,4);<br/>
a.toUpperCase();<br/>
a.toLowerCase();<br/>

## undefined, null, NaN

- undefined: 값이 정해지지 않았다.
- Null: 값이 비어있다.
- NaN: 값이 아니다.=== 계산 불가능

## console.log()

- 개발자 콘솔에 뭔가를 찍어주는 메서드 입니다.
var a = 1;<br/>
var b = "더하기";<br/>
var c = 2;<br/>
console.log(a + "" + b + "" + c + "=" + a + c);

## alert() 과 pronmpt()사용해보기
var ans = prompt("How are you?");<br/>
alert(ans);






# -연습문제1

두 수를 입력받아 4칙연산의 결과를 표시해 봅시다.<br/>
BMI를 계산하는 프로그램을 작성해 봅시다.<br/>
화씨를 입력받아서 섭씨로 바꾸는 프로그램을 작성해 봅시다.<br/>
입력한 문자열의 길이를 알려주는 프로그램을 작성해 봅시다.<br/>


## 답안 예시

- ex1-1.html
<!--
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">    
</head>
<body>
    <script>
    여기에 답 작성
    </script>
</body>
</html>
-->

## 풀이 영상
## 해답 보기

- 아래 링크에는 문제의 해답이 있습니다. 먼저 혼자 풀어보고 문제의 답을 보세요.<br/>
  https://gist.github.com/honux77/adfc9f0d86209fa7f0a084c779aa75ec

## 연습문제 1-1

- 두 수를 입력받아 4칙연산의 결과를 표시해 봅시다.
<!--
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <h2>연습문제 1-1</h2>
    <script>
        var a1 = prompt("숫자 1을 입력하시오");
        var a2 = prompt("숫자 2를 입력하시오");
        var b1 = Number(a1);
        var b2 = Number(a2);
        console.log(b1 + b2);
        console.log(b1 - b2);
        console.log(b1 * b2);
        console.log(b1 / b2);
    </script>
</body>
</html>
-->
## 연습문제 1-2

- Bmi를 계산하는 프로그램을 작성해 봅시다.
<!--
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <h2>연습문제 1-2</h2>
    <script>
        var a1 = prompt("키를 입력해 주세요");
        var a2 = prompt("몸무게를 입력해 주세요");
        var b1 = Number(a1);
        var b2 = Number(a2);
        var c = b1 / 100;
        console.log("당신의 BMI는" + b2 / (c * c) + "입니다");
    </script>
</body>
</html>
-->
## 연습문제 1-3

- 화씨를 입력받아서 섭씨로 바꾸는 프로그램을 작성해 봅시다.
<!--
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <h2>연습문제 1-3</h2>
    <script>
        var a = prompt("화씨를 입력하세요");
        var b = Number(a);
        var c = (b - 32) / 1.8;
        console.log("섭씨는" + c + "입니다.")
    </script>
</body>
</html>
-->
## 연습문제 1-4

- 입력한 문자열의 길이를 알려주는 프로그램을 작성해 봅시다.
<!--
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <h2>연습문제 1-3</h2>
    <script>
        var a = prompt("글자 수를 알고싶은 내용을 작성 하시오")
        console.log("작성한 내용의 글자 수는" + a.length + "입니다")
    </script>
</body>
</html>
-->
