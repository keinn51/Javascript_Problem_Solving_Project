# Creathb21's Problems



### 🎁 Object Destructuring

<br>

### 난이도 : 🌶

<br>

#### ☁︎  Object Destructuring


```javascript
요약 :

object이므로 curly brace로 destructuring을 해야 한다.
array와 달리 object는 순서에 상관없이 destructuring을 할 수 있다.


let superman = {
  name: `Superman`,
  job: `Hero`,
  hourlyPayment: 20,
  address: `Gangnam Samsung Remian`,
}

// array의 값 순서 위치에 맞게 변수에 값 할당한다
let arr = [1, 2, 3, 4];

let [a, c, b] = arr;
console.log(a); // 1
console.log(b); // 3
console.log(c); // 2

// object의 key 이름에 맞는 값이 할당 된다.
let {name, address, job, tel = `010227777`} = superman; // object에도 default값을 줄 수 있다., 물론 function도 줄 수 있다.

console.log(name); // Superman
console.log(job); // Hero
console.log(address); // Gangnam Samsung Remian
console.log(tel); // 010227777

-------------------------------------------------------------

Object를 naming하기

let {name: n, address: a, job: j, tel = `010227777`} = superman;

console.log(n); // Superman
console.log(j); // Hero
console.log(a); // Gangnam Samsung Remian
console.log(tel); // 010227777



*/

/*
문제1 :
var o = {p: 42, q: true};
var {p: foo, q: bar} = o;
 
console.log(foo);
console.log(bar);

출력 값을 작성하세요

````


<details><summary><b>Answer</b></summary>

<p>

```javascript

````

 </p>
 </details>
 <br>
 <br>



### 🎁 JSON 기초

<br>

### 난이도 : 🌶

<br>

#### ☁︎  JSON 기초


```javascript

요약 :

JSON(JavaScript Object Notation) == language among various programs written in various languages, 여러 다른 언어로 쓰여진 것들과 데이터를 주고 받을 수 있다.



let text = '{ "employees" : [' +
'{ "firstName":"John" , "lastName":"Doe"},' +
'{ "firstName":"Anna" , "lastName":"Smith"},' +
'{ "firstName":"Peter" , "lastName":"Jones" }]}';

-----------------------single quote vs. back tick-------------------------------

let text = '{ "employees" : [
{ "firstName":"John" , "lastName":"Doe"},
{ "firstName":"Anna" , "lastName":"Smith"},
{ "firstName":"Peter" , "lastName":"Jones" }
]}';


console.log(text)
---------------------------------------------------------------------

parase() method로 JSON string을 Javascript Object로 바꿔줄 수 있다.
let obj = JSON.parse(text); // 변환해주면 Javascript Object로 된다.
console.log(obj);
console.log(obj.employees);
console.log(obj.employees[0]);
console.log(obj.employees[0].firstName);



````


<details><summary><b>Answer</b></summary>

<p>

```javascript

````

 </p>
 </details>
 <br>
 <br>
 
 
 
### 🎁 Send, Receive, and Store data using JSON

<br>

### 난이도 : 🌶

<br>

#### ☁︎  Send, Receive, and Store data using JSON


```javascript

요약 :

JSON 데이터를 표시해보기(데이터를 주고 받기)


let text = '{ "employees" : [
{ "firstName":"John" , "lastName":"Doe"},
{ "firstName":"Anna" , "lastName":"Smith"},
{ "firstName":"Peter" , "lastName":"Jones" }
]}';


let obj = JSON.parse(text);

document.getElementById("app").innerHTML =
obj.employees[1].firstName + " " + obj.employees[1].lastName;

// Sending Data
let myObj = {name: "John", age: 31, city: "New York"};
let myJSON = JSON.stringify(myObj);
console.log(myJSON); // text화된 데이터를 볼 수 있음

// Receiving Data
let myJSON = '{"name":"John","Age":31,"city":"New York"}';

let myObj = JSON.parse(myJSON);
document.getElementById("app").innerHTML = myObj.name;

// Storing data;
let myObj = '{"name":"John","Age":31,"city":"New York"}';
let myJSON = JSON.stringify(myObj);
localStorage.setItem("testJSON", myJSON); // localStroage란 내컴퓨터 안에 있는 조그마한 데이터베이스

// Retrieving data:
text = localStorage.getItem("testJSON");
obj = JSON.parse(text);
document.getElementById("app"").innerHTML = obj.name;



````


<details><summary><b>Answer</b></summary>

<p>

```javascript

````

 </p>
 </details>
 <br>
 <br>



### 🎁  Rest and Spread

<br>

### 난이도 : 🌶

<br>

#### ☁︎   Rest and Spread


```javascript


요약 :

let abc = [`a`, `b`, `c`];
let def = [`d`, `e`, `f`];

let alpha = [abc, def];
console.log(alpha); // [[`a`, `b`, `c`], [`d`, `e`, `f`]] => [Array[3]], [Array[3]]
console.log(alpha[0][0]); // [[`a`, `b`, `c`], [`d`, `e`, `f`]] => a
console.log(alpha[0][1]); // [[`a`, `b`, `c`], [`d`, `e`, `f`]] => b
console.log(alpha[1][1]); // [[`a`, `b`, `c`], [`d`, `e`, `f`]] => e

-----------------------------------------------------------------------------
let total = [`a`, `b`, `c`, `d`, `e`, `f`];

// [`a`, `b`, `c`, `d`, `e`, `f`]; 이렇게 한번에 출력하는 방법 => Spread(하나를 여럿으로 전환)
let beta = [...abc, ...def];
console.log(beta);

-------------------------------------------------------------------------
// Rest(여럿을 하나로 전환) == Collector == Gather
functino sum(first, ...others) {
  console.log(...others);
  for (let i = 0; i < others.length; i++) {
    first += others[i];
  }
  return first;
}

console.log(sum(1, 2, 3)); // ...others == 2, 3
console.log(sum(1, 2, 3, 4, 5)); // ...others == 2, 3, 4, 5
console.log(sum(1, 2, 3, 4, 5, 6, 7)); // ...others == 2, 3, 4, 5, 6, 7

-------------------------------------------------------------------------

let params = [`superman`, 1, true];
let otherParams = [`birdman`, ...params];
let otherParams2 = [`birdman`, params]; // spread를 하지 않으면  array 자체로 나타난다.
console.log(otherParams);
console.log(otherParams2);


````


<details><summary><b>Answer</b></summary>

<p>

```javascript

````

 </p>
 </details>
 <br>
 <br>



### 🎁 Closure

<br>

### 난이도 : 🌶

<br>

#### ☁︎  Closure


```javascript

요약 :


1. Function 내부를 들여다 볼 때, local scope라는 것이 만들어진다.
2. Global or Local Scope는 이름 리스트.
3. 같은 scope에 찾는 값이 없으면 원래 scope보다 더 넓은범위의 scope에서 찾아 온다.

function heroName() {
  let name2 = "Superman";

  return function() {
    console.log(`Hi, I am ${name2}`);
  }
}

let name2 = "Batman";

let result = heroName();

console.log(result); // 중요한 사실, 여기서 결과를 return 하는게 아닌 function을 return 한다.
console.log(result());

*/

/*

문제1 :

var counter = 0;

// Function to increment counter
function add() {
  var counter = 0; 
  counter += 2;
}

add();
add();
add();

console.log(counter);

출력 값을 적으세요.

*/

/*

문제2 :

function add() {
  var counter = 0; 
  counter += 2;
  return counter;
}

add();
add();
add();

console.log(counter);

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



### 🎁 Scope

<br>

### 난이도 : 🌶

<br>

#### ☁︎  Scope


```javascript




요약 :

function heroName(firstName, lastName) {

  function getFullName() {
    return firstName + " " + lastName;
  }

  console.log("Hello, " + getFullName() );
  console.log("Bye, " + getFullName());
}

heroName(`Kim`, `Superman`);

*/

/*

문제1 :

function outerFunction () {
  const outer = `I'm the outer function!`

  function innerFunction() {
    const inner = `I'm the inner function!`
    console.log(outer) // I'm the outer function!
  }

  console.log(inner) // Error, inner is not defined
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



### 🎁 

<br>

### 난이도 : 🌶

<br>

#### ☁︎  


```javascript





````


<details><summary><b>Answer</b></summary>

<p>

```javascript

````

 </p>
 </details>
 <br>
 <br>



### 🎁 Independent Scope

<br>

### 난이도 : 🌶

<br>

#### ☁︎  Independent Scope


```javascript

요약 :

function makeCounter() {
  let count = 0;

  return function() {
    return count++;
  };
}

let counter1 = makeCounter();

console.log( counter1() ); // 0, count => 1
console.log( counter1() ); // 1, count => 2
console.log( counter1() ); // 2, cuont => 3

let counter2 = makeCounter();
console.log( counter2() ); // 0, count => 1, 3이 나오지 않고 0부터 다시 시작(새로운 scope를 만듬)
console.log( counter2() ); // 1, count => 2
console.log( counter2() ); // 2, cuont => 3


문제 1 :


function makeCounter() {
  let count = 0;

  return function() {
    let count = 1;
    return count++;
  };
}

let counter1 = makeCounter();

console.log( counter1() );
console.log( counter1() );
console.log( counter1() );

let counter2 = makeCounter();
console.log( counter2() );
console.log( counter2() );
console.log( counter2() );

출력값을 적으세요.

문제 2 :

function makeCounter() {
  let count = 0;

  return function() {
    return count++;
  };
}

console.log( makeCounter()() );
console.log( makeCounter()() );
console.log( makeCounter()() );
console.log( makeCounter()() );
console.log( makeCounter()() );

힌트 : makeCounter() 는 scope를 새로만드는 역할이기도 하다.

출력값을 적으세요.



````


<details><summary><b>Answer</b></summary>

<p>

```javascript

````

 </p>
 </details>
 <br>
 <br>



### 🎁 setTimeout and setInterval

<br>

### 난이도 : 🌶

<br>

#### ☁︎  setTimeout and setInterval


```javascript

요약 :

function sayHi() {
  console.log('Hello');
}
sayHi();
setTimeout(sayHi, 2000); // 2000/1000 = 2초뒤, 일정시간이 지난뒤에 기능 수행

---------------------------------------------------------------------------

function sayHi(phrase, who) {
  console.log( phrase + ', ' + who);
}

sayHi("Hello", "John"); // Hello, John
setTimeout(sayHi, 1000, "Hello", "John"); // 1초뒤 Hello, John

---------------------------------------------------------------------------

function 형태를 제공

setTimeout(() => console.log('Hello));
setTimeout(() => console.log('Hello), 1000);
setTimeout(() => console.log('Hello), 2000);

---------------------------------------------------------------------------

굉장히 중요한 코드


let timerId = setTimeout(() => console.log("never happens"), 1000);

evaluate란 return값을 만들어 낸다는 뜻이다.

---------------------------------------------------------------------------

setTimeout한것을 취소하기

clearTimeout(timerId);
console.log(timerId);

---------------------------------------------------------------------------

// 정해진 시간 간격으로 반본적으로 기능 실행
let timerId = setInterval(() => console.log('tick'), 1000); // side effects

// 정해진 시간에 기능실행
setTimeout(() => {
  clearInterval(timerId);
  console.log('stop');
}, 5000)

*/

/*
문제1 :

5초뒤에 현재시간을 보여주는 코드를 작성하세요.
*/


/*
문제2 :

3, 6, 9 형식으로 3초마다 출력되게 하고 30이 출력이 되면 중단하게 하는 코드를 작성하세요.



````


<details><summary><b>Answer</b></summary>

<p>

```javascript

````

 </p>
 </details>
 <br>
 <br>
