# Creathb21's Problems



### 🎁 The switch statement

<br>

### 난이도 : 🌶

<br>

#### ☁︎ The switch statement


```javascript
문제 1 : 

var day;
switch (new Date().getDay()) {
  case 0:
    day = "Sunday";
    break;
  case 1:
    day = "Monday";
    break;
  case 2:
    day = "Tuesday";
    break;
  case 3:
    day = "Wednesday";
    break;
  case 4:
    day = "Thursday";
    break;
  case 5:
    day = "Friday";
    break;
  case  6:
    day = "Saturday";
}
console.log(day);

출력값을 작성하세요.

````


<details><summary><b>Answer</b></summary>

<p>

```javascript

Sunday
(현재의 요일이 출력 된다.)

````

 </p>
 </details>
 <br>
 <br>


### 🎁 Functions 개념

<br>

### 난이도 : 🌶

<br>

#### ☁︎  Functions 개념

```javascript
문제 1 : 

function myMessage() {

}

위 구조 자체를 Function Declaration 이라고 한다.

이 구조안에
function head 와 function body가 있는데 이를 다른 말로 작성하세요.


문제 2 :

function을 호출한다고 할 때 보통 Call이라고 한다.
이 외에도 동의어로 2가지를 더 작성하세요.



문제 3 :

function에서 아무것도 return하지 않을경우 return되는 값을 작성하세요.


```

<details><summary><b>Answer</b></summary>
<p>

```javasript

문제 1 : head == parameter == argument,
body{} == implementation(이행,  실행)


문제 2 : Call/implement/execute a function => function을 호출한다.


문제 3 :
undefined가 return된다고 본다.

```

</p>
</details>
<br>
<br>

### 🎁 Functions and Scope

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Functions and Scope


 ```javascript

요약 :

javascript에서 scope는 local과 global로 나뉜다.

scope는 먼저 같은 scope에 있는 값을 찾아오고
없으면 다른 scope에서 찾아온다.

중요한건 global에서 local에 있는 scope는 참조하지 못하지만
local에서 global scope는 참조할 수 있다.

````



<details><summary><b>Answer</b></summary>

  <p>

```javascript


````

 </p>
 </details>
 <br>
 <br>


### 🎁 Functions and Arguments

<br>


### 난이도 : 🌶

<br>

#### ☁︎ Functions and Arguments


```javascript
요약 :

Function Declaration == Function Definition

someFn(5, 6) == we apply someFn to 5 and 6 == we call someFn with 5 and 6

문제 1 :

function someFn(a, b = 2, c) {
  return a * b * c;
}

someFn(2,3,4);
someFn(2,3);
someFn(2);
someFn(2,4);


출력값을 작성하세요.


````

<details>
<summary><b>Answer</b></summary>

<p>

```javascript

someFn(2,3,4);  // 24
someFn(2,3);   // NaN
someFn(2);  // NaN
someFn(2,,4);   // NaN



````

</p>
</details>
<br>
<br>

### 🎁 Function expressions and arrows

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Function expressions and arrows


 ```javascript
요약 :

Block needs no no semicolon.
블록은 {}자체로 세미콜론이 없어도 된다.

--------------------------------------------------
=기호를 사이에 두고, 왼쪽의 Term/Name/Variable은 보이지만, ==> myVar은 global scope로 인식
=기호의 오른쪽은 어디서도 안 보인다. ==> function myFn(arg)의 scope가 myVar 안쪽에 숨음

let myVar = function myFn(arg) {
  return arg ** 2;
}

--------------------------------------------------
argument로 Value가 아닌 function자체를 줄 수 있다.


문제 1 :

function log(array) {
 console.log(array[0]);
 console.log(array[1]);
}
log([1, 2, 3]);
log([1, 2, 3, 4, 5, 6]);

출력값을 작성하세요.
````



<details><summary><b>Answer</b></summary>

  <p>

```javascript

````

 </p>
 </details>
 <br>
 <br>

### 🎁 First Order Functions

<br>

### 난이도 : 🌶

<br>

#### ☁︎ First Order Functions


 ```javascript


// 요약 :

// function을 return하는 값으로도 쓸 수 있다.

function myFn2(arg1) {
  return function myFn1(arg2) {
    return arg2 * 10;
  }
}

let returnedFn1 = myFn2(7);
let returnedFn2 = myFn2(7)(15);

console.log(returnedFn1);
console.log(returnedFn2);

// first oder function이란?
// function을 arg로 받거나 function자체를 return하는 function



// 문제 1 :

function myFn(f, v){
	return f(f(v));
}
function plusthree(v){
	return v + 3;
}
myFn(plusthree,7);

// 출력값을 작성하세요.

````



<details><summary><b>Answer</b></summary>

  <p>

```javascript

````

 </p>
 </details>
 <br>
 <br>
 
 ### 🎁 Callbacks

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Callbacks


```javascript
// 요약 :

// 콜백은 First Order Funciton중에 한개이다.
// CallBack == a First Order Function
// function이 다른 arg로 전달되어서 다른 function안에서 호출되는 것

function myFn1(a, b) {
  let result = (a > 5)? b(10) : b(1);
  return result;
}

function myFn2(arg) {
  return arg * 6;
}

let outerResult = myFn1(2, myFn2);

console.log(outerResult);


/*
문제 1 :

function ask(question, yes, no) {
  if (confirm(question)) yes()
  else no();
}

function showOk() {
  alert( "You agreed." );
}

function showCancel() {
  alert( "You canceled the execution." );
}

위에 3가지 function이 선언 되어있다.
callback을 이용해서 ask함수를 호출할 때 showOk와 showCancel function도 같이 호출 시켜보세요.
*/


/*
문제 2 :

function first(){
  // Simulate a code delay
  setTimeout( function(){
    console.log(1);
  }, 500 );
}
function second(){
  console.log(2);
}
first();
second();

출력값을 작성하세요.
````


<details><summary><b>Answer</b></summary>

<p>

```javascript

````

 </p>
 </details>
 <br>
 <br>


### 🎁 Function Declaration and Function Expression

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Function Declaration and Function Expression


```javascript
// 요약 :

// Function Declaration
function myFn(arg) {
  return arg + 3;
}

// ----------------------------------------------------------------

// Function Expression == Operation == Operators(연산자) + Operands(피연산자)

let a = 1;
let b = a + 1;
let c = function myFn(arg) {
  return arg + 3;
}


// ----------------------------------------------------------------
// 어떻게 보면 Function Declaration과 Function Expression은 같아 보이지만 차이점이 있다.

// Function Declaration은 코드를 읽어오는 순서에 상관없이 함수가 어디에 정이 되어 있는 정의 되어 있기만하면 함수를 불러 올 수 있다.

// 하지만

// Function Expression은 코드를 읽어오는 순서를 지켜야 한다.
// 호출 되는 위치보다 위쪽에 함수가 정의 되어 있어야 함수를 호출할 수 있다.


/*

문제1 :

function sayHi() {
  alert( "Hello" );
}

function bar() {
    return 3;
}

위 코드를 function Expression 방식으로 바꾸세요.

*/


/*

문제2 :

var today = function today() {return new Date()}
today();

위 코드가 작동할지 안할지 예, 아니오로 답해주세요.


````


<details><summary><b>Answer</b></summary>

<p>

```javascript

````

 </p>
 </details>
 <br>
 <br>



### 🎁 Arrow Function

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Arrow Function


```javascript

문제 1 :

function plus(a, b) {
  return a + b;
}

위 코드를 더 같결하게 만드세요.
````


<details><summary><b>Answer</b></summary>

<p>

```javascript

````

 </p>
 </details>
 <br>
 <br>



### 🎁 Object

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Object


```javascript
요약 : 

Primitive types == 기본적인 타입(=원시적인타입) == Integer,strnig, boolean ..

Structed types == 구조를 가진 타입 == object, array, tuples ...

------------------------------------------------------------------
constructor : 새 오브젝트를 만드는 것
let myObject = new Object();

console.log(myObject);

------------------------------------------------------------------
object는 key : value 형식으로 구성된다.
key에는 ""를 붙여줘도 문법적으로 틀리진 않는다.
하지만 다른 사람이 보았을 때 헷갈리므로 camelcase를 쓰는게 났다.


밑에는 object호출하는 방법 

let heroes = {
  name: "Superman",
  age: 33,
  "current address": "제주시 한경면 판포리",
};

console.log(heroes.name);
console.log(heroes.age);
console.log(heroes["current address"]);

*/

/*
문제1 :

Primitive타입과 Structed types이 있는데 Object는 어디 타입에 속하는지 적으세요.
*/

/*
문제2 :

Object는 mutable일지 unmutable을지 생각해보세요.

````


<details><summary><b>Answer</b></summary>

<p>

```javascript

````

 </p>
 </details>
 <br>
 <br>



### 🎁 Object - adding properties

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Object - adding properties


```javascript
요약 : 

기존의 object에 새로운 properties를 추가 할 때 key에 ""를 붙이는 문법을 쓴다. 하지만 이 방법도 해서는 안된다.
ex)
key에 "current Address" 이렇게 해서는 안된다. 대신 CamelCase를 쓰자
=> currentAddress

나중에 배울 내용
외부에서 properties를 추가할 때는 [] 방식으로 한다.


let heroes = {
  name: "Superman",
  age: 33,
  currentAddress: "제주시 한경면 판포리",
};

let newKey = "sex"; // don't do that
heroes[newKey] = "male" // don't do that

console.log(heroes.name);
console.log(heroes.age);
console.log(heroes.currentAddress);
console.log(heroes["newKey"]); // don't do that


*/

/*
문제1 :

let person = {
  firstName: "SeoYeon",
  age: "25"
}

console.log(person.firstName + " is " + person.age + " years old.");

출력값을 작성하세요.

````


<details><summary><b>Answer</b></summary>

<p>

```javascript


````

 </p>
 </details>
 <br>
 <br>



### 🎁 Object constructor function

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Object constructor function


```javascript
요약 : 

function makeHeroes(name, age, address) {
  return {
    name,
    age,
    address,
  }
}

function makeHeroes(name, age, address) {
  return {
    name: name,
    age: age,
    address: address,
  }
}

위 2개의 function은 같은 의미를 지닌다.
그리고 이 2개의 function을 구조를 가지고 있는 데이터 타입을 만들어내는 function이라고 해서
object constructor function이라고 한다.


*/


/*
문제1 :

var Pastry = {
  // initialize the pastry
  init: function (type, flavor, levels, price, occasion) {
    this.type = type;
    this.flavor = flavor;
    this.levels = levels;
    this.price = price;
    this.occasion = occasion;
  },
}

위 코드를 더 간결하게 작성해보세요.

````


<details><summary><b>Answer</b></summary>

<p>

```javascript

````

 </p>
 </details>
 <br>
 <br>



### 🎁 Object ( for...in )

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Object ( for...in )


```javascript
요약 : 

어떤 Object에 있는 key만 뽑아서 보는 방법

let codes = {
  "49" :"Germany",
  "41" :"Switzerland",
  "44" :"Great Britatin",
  "1" :"USA",
};

//key라는 단어는 임의로 정한것으로 어떠한 단어가 오더라도 상관없다.
for(let key in codes) { 
  console.log(key); // key가 숫자이면 작은순서부터 출력
}

*/

/*
문제1 : 

var arr = [3, 5, 7];
arr.foo = "hello";

for (var i in arr) {
   console.log(i); 
}

for (var i of arr) {
   console.log(i); 
}

출력 값을 적으세요.

````


<details><summary><b>Answer</b></summary>

<p>

```javascript

````

 </p>
 </details>
 <br>
 <br>



### 🎁 Object - copy by reference

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Object - copy by reference


```javascript

요약 : 

let student1 = {
  name: "Superman",
  study: "JavaScript",
}

let student2 = student1;
let student3 = student2;

student2.name = "Batman";

console.log(student1.name);
console.log(student2.name);
console.log(student3.name);

출력값은 
Batman
Batman
Batman
이 나오는데

그 이유는 Object를 복사해서 새로 만든게 아닌 Object의 메모리 주소값을 복사했기 때문이다.

*/

/*

문제1 :

let obj = {
  a: 1,
  b: 2,
};
let copy = obj;

obj.a = 5;
console.log(copy.a);

출력 값을 적으세요.

````


<details><summary><b>Answer</b></summary>

<p>

```javascript

````

 </p>
 </details>
 <br>
 <br>


