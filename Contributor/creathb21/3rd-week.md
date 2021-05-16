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
someFn(2,,4);


출력값을 작성하세요.


````

<details>
<summary><b>Answer</b></summary>

<p>

```javascript



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
