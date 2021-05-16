# Creathb21's Problems



### 🎁 Evaluation, Expression, Statement

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Evaluation, Expression, Statement


```Javascript 코드 뒤에는 종종 ; 쌍반점(semi-colon)을 볼 수 있는데, 이것은 Statement들을 구분짓고 암시적으로 이 Statement가 끝났다라는 뜻으로 사용됩니다. 

문제 1 : 다음의 문제들을 알맞은 정답과 매칭하세요.
1. 프로그래밍에서 코드란 무엇인가요? 
2. 프로그래밍에서 Statement이란 무엇인가요? 
3. 프로그래밍에서 Expression이란 무엇인가요? 
4. 프로그래밍에서 Evaluation이란 무엇인가요? 

a. 컴퓨터에게 어떠한 값을 가져오라는 명령
b. 컴퓨터가 읽을 수 있는 언어
c. 컴퓨터가 코드를 읽고 계산을해서 내는 결과값
d. 컴퓨터에게 무엇을 하라고 내리는 명령


문제 2 : 
let math = 2 + 3;
console.log(math);

다음은 5를 출력하는 간단한 코드입니다. 여기서 어떤것이 Statement, Expression 그리고 Evaluation인지 생각해보세요.



````


<details><summary><b>Answer</b></summary>

<p>

```javascript
1. b
2. d
3. a
4. c

let math = 2 + 3;        // ==> Evaluation 
console.log(math);       // ==> Statement
````

 </p>
 </details>
 <br>
 <br>


### 🎁 variables

<br>

### 난이도 : 🌶

<br>

#### ☁︎  variables

```javascript

vary(변한다) + able(할 수 있다) 

변수란 "어떤 관계나 범위 안에서 여러 가지 값으로 변할 수 있는 수"를 말합니다.

Javascript내에서 변수를 생성할려면, 먼저 변수를 선언(declaration)해줘야합니다.
let food;

이 food라는 변수를 파일내에 선언함으로써, 이 food 변수는 파일내에 존재하게됩니다. 우리는 이 food라는 변수를 사용 할 수 있고, 값을 할당할 수 있습니다.

변수에 값을 담을때 우리는 이것을 초기화(Initialization)라고 부릅니다.
let food = "pizza";

더 쉬운 예제를 들자면, 
let box = "something" 은 값을 담는 상자를 파일내에 존재한다고 선언하고, 상자안을 우리가 원하는 값(something)으로 초기화합니다.
변수에 값을 게속해서 재할당 할 수 있습니다.
box = "toy";
box = "food";

변수에 할당되는 값이 문자일 경우  " "나 ' '로 묶어줘야합니다.

Javascript내에서 변수를 선언할때 사용되는 키워드는 let, var, const등 이 있고, 각각의 다른 용도를 가지고있습니다. 


문제 1 : let 키워드를 사용해 juice라는 변수를 선언하고, juice 변수에 apple juice라는 값을 할당하세요. 그리고 console.log()를 이용해 juice변수를 출력하세요.

```

<details><summary><b>Answer</b></summary>
<p>

```javasript
let juice; 
juice = apple juice;
console.log(juice);
```

</p>
</details>
<br>
<br>

### 🎁 let and const

<br>

### 난이도 : 🌶

<br>

#### ☁︎ variables


 ```javascript

문제 1 : 지금까지 배운 선언과 초기화 개념을통해, iceCream이라는 주어진 변수의 값을 출력해보세요. 출력되는 값은 
choco
vanilla
이여야 합니다

문제 2 : const 키워드를 이용해 변수를 선언 및 초기화해보세요.


// 문제 1
let iceCream; // 선언(Declaration)
// iceCream = " " // 초기화(Initialization)
// console.log() // 출력


// 문제 2

````



<details><summary><b>Answer</b></summary>

  <p>

```javascript
문제1 
let iceCream;
iceCream = "choco vanila"
console.log(iceCream);

문제2
const candy = red;

````

 </p>
 </details>
 <br>
 <br>


### 🎁 Datatypes

<br>


### 난이도 : 🌶

<br>

#### ☁︎ Data type


```javascript

자바스크립트에서 사용되는 데이터 유형(Data type)은 여러가지가 있습니다.


다음은 대표적으로 사용되는 데이터 유형들 입니다.
string = 문자열
number = 숫자
boolean = 참 혹은 거짓(true or false)을 가진 데이터를 return합니다
undefined = 변수가 선언만되고 아직 값이 할당(초기화)되지 않았을때를 얘기합니다.
null = 0과 같음

아직 배우지않는 데이터 유형들
object
symbol(ES6에서 추가됨)

문제 1 : 현재 아래의 변수들은 선언(declaration)만 되어있는 상태입니다. 아래의 변수들에 이름에 각각의 맞는 데이터 유형(data type)을 할당하세요.

let dataTypeString;
let dataTypeString;
let dataTypeNumber;
let dataTypeBoolean;
let dataTypeUndefined;
let dataTypeUndefined2;
let dataTypeNull;

````

<details>
<summary><b>Answer</b></summary>

<p>

```javascript

let dataTypeString = "nobody";
let dataTypeString = "JYP";
let dataTypeNumber = 3;
let dataTypeBoolean = 3 > 1;
let dataTypeUndefined;
let dataTypeUndefined2 = undefined;
let dataTypeNull = null;



````

</p>
</details>
<br>
<br>

### 🎁 Type Conversion

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Type Conversion


 ```javascript
Type Conversion
Type = 유형
Conversion = 변형하다 
String = 문자열
Number = 숫자

Type Conversion은 데이터의 유형을 변형한다는 뜻 입니다.
Javascript에서 사용할 수 있는 여러 데이터 유형들, 숫자, 문자열, Boolean 등을 다른 데이터 유형으로 바꿀 수 있습니다.
숫자 -> 문자열
문자열 - > 숫자...

let value = 13; 
console.log(typeof value);
a라는 변수는 13이라는 숫자 데이터 유형인 값을 가지고 있습니다. 
이 변수가 가진 데이터 유형을 보려면 typeof 변수이름 을 입력하면됩니다
결과값으로 number 가 출력됩니다.

우리는 이 13이라는 숫자를 String()함수를 이용해 문자열로 변환시킬 수 있습니다.
value = String(value) // 데이터 유형을 String()함수를 이용해 String로 변경
console.log(typeof value); // 13이 숫자가아닌 문자열로 출력됨

반대로 문자열 데이터 유형을가진 값을 숫자로 변형시킬 수 있습니다.
let str = "123";
str = (typeof str) // String 출력

let num = Number(str); // 데이터 유형을 Number()함수를 이용해 Number로 변경
console.log(typeof num); // Number 출력



문자열 데이터 유형인 "I am"과 숫자 데이터 유형인 13을 더하면 어떻게될까요?
console.log("I am" + 12)
I am12 가 출력이 됩니다.

앞 강의에 Variable에서 문자열(string)을 사용할려면 문자열을 " "나 ' '로 묶어줘야한다고 했었습니다, 그 말은 2는 숫자지만, "2"는 문자열이 된다는 뜻입니다.

이번에는 a라는 변수를 5 + "6"로 초기화하여, 출력하면 어떻게될까요?
let a = 5 + "6";
console.log(a);
56이 출력이됩니다.





문제 1 :
let c = 13;
13이라는 숫자 데이터 유형을 가지고 있는 변수 C가 있습니다.
이 숫자 13을 문자열로 변형해보세요.


문제 2 :
let something = "1000";
"1000" 이라는 문자열 데이터 유형을 가지고 있는 변수 something가 있습니다.
이 문자열을 숫자로 변형해보세요.

문제 3 :
let b = '12' + '21';
b를 출력하면 뭐가 나올까요?

문제 4 :
let d = "I am" + " "  + 12;
d를 출력하면 뭐가 나올까요?

````



<details><summary><b>Answer</b></summary>

  <p>

```javascript
문제1 :
let c = 13;
c = String(c)
console.log(typeof c);  // string 

문제2 : 
let something = "1000";
something = Number(something)
console.log(typeof something);   / number

문제3 : 
let b = '12' + '21'; 
console.log(b);    // 1221

문제 4 :
let d = "I am" + " "  + 12;
console.log(d);    // I am 12
````

 </p>
 </details>
 <br>
 <br>

### 🎁 Operators

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Operators


 ```javascript


자바스크립트에서는 다양한 연산자(Operators)가 사용되고 있습니다.
논리 연산자, 비교 연산자, 대입 연산자, 불 연산자..



Operators : 연산자는 변수나 값의 연산을 위해 사용되는 부호를 칭합니다.
예시 : 2 + 3 에서 2와 3의 연산을위해 + 연산자가 사용됩니다.

Operands : 피연산자는 연산에 필요한 값을 뜻합니다.
예시 : 3 + 5 에서 + 연산자를 이용해 피연산자인 3과 5를 더했습니다.

Unary Operator : 연산자가 1개의 피연산자를 가지고있으면 우리는 이 연산자를 Binary Operator라고 부릅니다.
예시 : -1 , 빼기 연산자는 피연산자인 1을 가지고 있음.

Binary Operator : 연산자가 2개의 피연산자를 가지고있으면 우리는 이 연산자를 Binary Operator라고 부릅니다.
예시 : 1 + 2 , 더하기 연산자는 피연산자인 1과 2를 가지고 있음.

Ternary Operator : 연산자가 3개의 피연산자를 가지고있으면 우리는 이 연산자를 Ternary Operator라고 부릅니다

우선 순위(Priority of Operators) : 한 Expression중에 여러개의 연산자가 존재한다면, 어느것을 먼저 계산해야할지 생각해야합니다. 이것을 우리는 연산자의 우선 순위라고 합니다.

````



<details><summary><b>Answer</b></summary>

  <p>

```javascript

````

 </p>
 </details>
 <br>
 <br>
