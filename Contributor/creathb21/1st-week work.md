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
