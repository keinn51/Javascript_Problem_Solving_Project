# Creathb21's Problems



### ๐ The switch statement

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ The switch statement


```javascript
๋ฌธ์  1 : 

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

์ถ๋ ฅ๊ฐ์ ์์ฑํ์ธ์.

````


<details><summary><b>Answer</b></summary>

<p>

```javascript

Sunday
(ํ์ฌ์ ์์ผ์ด ์ถ๋ ฅ ๋๋ค.)

````

 </p>
 </details>
 <br>
 <br>


### ๐ Functions ๊ฐ๋

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ  Functions ๊ฐ๋

```javascript
๋ฌธ์  1 : 

function myMessage() {

}

์ ๊ตฌ์กฐ ์์ฒด๋ฅผ Function Declaration ์ด๋ผ๊ณ  ํ๋ค.

์ด ๊ตฌ์กฐ์์
function head ์ function body๊ฐ ์๋๋ฐ ์ด๋ฅผ ๋ค๋ฅธ ๋ง๋ก ์์ฑํ์ธ์.


๋ฌธ์  2 :

function์ ํธ์ถํ๋ค๊ณ  ํ  ๋ ๋ณดํต Call์ด๋ผ๊ณ  ํ๋ค.
์ด ์ธ์๋ ๋์์ด๋ก 2๊ฐ์ง๋ฅผ ๋ ์์ฑํ์ธ์.



๋ฌธ์  3 :

function์์ ์๋ฌด๊ฒ๋ returnํ์ง ์์๊ฒฝ์ฐ return๋๋ ๊ฐ์ ์์ฑํ์ธ์.


```

<details><summary><b>Answer</b></summary>
<p>

```javasript

๋ฌธ์  1 : head == parameter == argument,
body{} == implementation(์ดํ,  ์คํ)


๋ฌธ์  2 : Call/implement/execute a function => function์ ํธ์ถํ๋ค.


๋ฌธ์  3 :
undefined๊ฐ return๋๋ค๊ณ  ๋ณธ๋ค.

```

</p>
</details>
<br>
<br>

### ๐ Functions and Scope

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Functions and Scope


 ```javascript

์์ฝ :

javascript์์ scope๋ local๊ณผ global๋ก ๋๋๋ค.

scope๋ ๋จผ์  ๊ฐ์ scope์ ์๋ ๊ฐ์ ์ฐพ์์ค๊ณ 
์์ผ๋ฉด ๋ค๋ฅธ scope์์ ์ฐพ์์จ๋ค.

์ค์ํ๊ฑด global์์ local์ ์๋ scope๋ ์ฐธ์กฐํ์ง ๋ชปํ์ง๋ง
local์์ global scope๋ ์ฐธ์กฐํ  ์ ์๋ค.

````



<details><summary><b>Answer</b></summary>

  <p>

```javascript


````

 </p>
 </details>
 <br>
 <br>


### ๐ Functions and Arguments

<br>


### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Functions and Arguments


```javascript
์์ฝ :

Function Declaration == Function Definition

someFn(5, 6) == we apply someFn to 5 and 6 == we call someFn with 5 and 6

๋ฌธ์  1 :

function someFn(a, b = 2, c) {
  return a * b * c;
}

someFn(2,3,4);
someFn(2,3);
someFn(2);
someFn(2,4);


์ถ๋ ฅ๊ฐ์ ์์ฑํ์ธ์.


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

### ๐ Function expressions and arrows

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Function expressions and arrows


 ```javascript
์์ฝ :

Block needs no no semicolon.
๋ธ๋ก์ {}์์ฒด๋ก ์ธ๋ฏธ์ฝ๋ก ์ด ์์ด๋ ๋๋ค.

--------------------------------------------------
=๊ธฐํธ๋ฅผ ์ฌ์ด์ ๋๊ณ , ์ผ์ชฝ์ Term/Name/Variable์ ๋ณด์ด์ง๋ง, ==> myVar์ global scope๋ก ์ธ์
=๊ธฐํธ์ ์ค๋ฅธ์ชฝ์ ์ด๋์๋ ์ ๋ณด์ธ๋ค. ==> function myFn(arg)์ scope๊ฐ myVar ์์ชฝ์ ์จ์

let myVar = function myFn(arg) {
  return arg ** 2;
}

--------------------------------------------------
argument๋ก Value๊ฐ ์๋ function์์ฒด๋ฅผ ์ค ์ ์๋ค.


๋ฌธ์  1 :

function log(array) {
 console.log(array[0]);
 console.log(array[1]);
}
log([1, 2, 3]);
log([1, 2, 3, 4, 5, 6]);

์ถ๋ ฅ๊ฐ์ ์์ฑํ์ธ์.
````



<details><summary><b>Answer</b></summary>

  <p>

```javascript
log([1, 2, 3]);   // 1, 2
log([1, 2, 3, 4, 5, 6]);   // 1, 2

````

 </p>
 </details>
 <br>
 <br>

### ๐ First Order Functions

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ First Order Functions


 ```javascript


// ์์ฝ :

// function์ returnํ๋ ๊ฐ์ผ๋ก๋ ์ธ ์ ์๋ค.

function myFn2(arg1) {
  return function myFn1(arg2) {
    return arg2 * 10;
  }
}

let returnedFn1 = myFn2(7);
let returnedFn2 = myFn2(7)(15);

console.log(returnedFn1);
console.log(returnedFn2);

// first oder function์ด๋?
// function์ arg๋ก ๋ฐ๊ฑฐ๋ function์์ฒด๋ฅผ returnํ๋ function



// ๋ฌธ์  1 :

function myFn(f, v){
	return f(f(v));
}
function plusthree(v){
	return v + 3;
}
myFn(plusthree,7);

// ์ถ๋ ฅ๊ฐ์ ์์ฑํ์ธ์.

````



<details><summary><b>Answer</b></summary>

  <p>

```javascript

13

````

 </p>
 </details>
 <br>
 <br>
 
 ### ๐ Callbacks

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Callbacks


```javascript
// ์์ฝ :

// ์ฝ๋ฐฑ์ First Order Funciton์ค์ ํ๊ฐ์ด๋ค.
// CallBack == a First Order Function
// function์ด ๋ค๋ฅธ arg๋ก ์ ๋ฌ๋์ด์ ๋ค๋ฅธ function์์์ ํธ์ถ๋๋ ๊ฒ

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
๋ฌธ์  1 :

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

์์ 3๊ฐ์ง function์ด ์ ์ธ ๋์ด์๋ค.
callback์ ์ด์ฉํด์ askํจ์๋ฅผ ํธ์ถํ  ๋ showOk์ showCancel function๋ ๊ฐ์ด ํธ์ถ ์์ผ๋ณด์ธ์.
*/


/*
๋ฌธ์  2 :

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

์ถ๋ ฅ๊ฐ์ ์์ฑํ์ธ์.
````


<details><summary><b>Answer</b></summary>

<p>

```javascript

๋ฌธ์  1 : 
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

let myFn1 = ask('yes or no?', showOk, showCancel);
console.log(myFn1)();


๋ฌธ์  2 :
2, 1

````

 </p>
 </details>
 <br>
 <br>


### ๐ Function Declaration and Function Expression

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Function Declaration and Function Expression


```javascript
// ์์ฝ :

// Function Declaration
function myFn(arg) {
  return arg + 3;
}

// ----------------------------------------------------------------

// Function Expression == Operation == Operators(์ฐ์ฐ์) + Operands(ํผ์ฐ์ฐ์)

let a = 1;
let b = a + 1;
let c = function myFn(arg) {
  return arg + 3;
}


// ----------------------------------------------------------------
// ์ด๋ป๊ฒ ๋ณด๋ฉด Function Declaration๊ณผ Function Expression์ ๊ฐ์ ๋ณด์ด์ง๋ง ์ฐจ์ด์ ์ด ์๋ค.

// Function Declaration์ ์ฝ๋๋ฅผ ์ฝ์ด์ค๋ ์์์ ์๊ด์์ด ํจ์๊ฐ ์ด๋์ ์ ์ด ๋์ด ์๋ ์ ์ ๋์ด ์๊ธฐ๋งํ๋ฉด ํจ์๋ฅผ ๋ถ๋ฌ ์ฌ ์ ์๋ค.

// ํ์ง๋ง

// Function Expression์ ์ฝ๋๋ฅผ ์ฝ์ด์ค๋ ์์๋ฅผ ์ง์ผ์ผ ํ๋ค.
// ํธ์ถ ๋๋ ์์น๋ณด๋ค ์์ชฝ์ ํจ์๊ฐ ์ ์ ๋์ด ์์ด์ผ ํจ์๋ฅผ ํธ์ถํ  ์ ์๋ค.


/*

๋ฌธ์ 1 :

function sayHi() {
  alert( "Hello" );
}

function bar() {
    return 3;
}

์ ์ฝ๋๋ฅผ function Expression ๋ฐฉ์์ผ๋ก ๋ฐ๊พธ์ธ์.

*/


/*

๋ฌธ์ 2 :

var today = function today() {return new Date()}
today();

์ ์ฝ๋๊ฐ ์๋ํ ์ง ์ํ ์ง ์, ์๋์ค๋ก ๋ตํด์ฃผ์ธ์.


````


<details><summary><b>Answer</b></summary>

<p>

```javascript

๋ฌธ์  1 :
let create = function sayHi() {
    alert("Hello");
}

let hb21 = function bar() {
    	return 3;
}

๋ฌธ์  2 :
์
````

 </p>
 </details>
 <br>
 <br>



### ๐ Arrow Function

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Arrow Function


```javascript

๋ฌธ์  1 :

function plus(a, b) {
  return a + b;
}

์ ์ฝ๋๋ฅผ ๋ ๊ฐ๊ฒฐํ๊ฒ ๋ง๋์ธ์.
````


<details><summary><b>Answer</b></summary>

<p>

```javascript

let career = ((a, b) => a + b);

````

 </p>
 </details>
 <br>
 <br>



### ๐ Object

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Object


```javascript
์์ฝ : 

Primitive types == ๊ธฐ๋ณธ์ ์ธ ํ์(=์์์ ์ธํ์) == Integer,strnig, boolean ..

Structed types == ๊ตฌ์กฐ๋ฅผ ๊ฐ์ง ํ์ == object, array, tuples ...

------------------------------------------------------------------
constructor : ์ ์ค๋ธ์ ํธ๋ฅผ ๋ง๋๋ ๊ฒ
let myObject = new Object();

console.log(myObject);

------------------------------------------------------------------
object๋ key : value ํ์์ผ๋ก ๊ตฌ์ฑ๋๋ค.
key์๋ ""๋ฅผ ๋ถ์ฌ์ค๋ ๋ฌธ๋ฒ์ ์ผ๋ก ํ๋ฆฌ์ง ์๋๋ค.
ํ์ง๋ง ๋ค๋ฅธ ์ฌ๋์ด ๋ณด์์ ๋ ํท๊ฐ๋ฆฌ๋ฏ๋ก camelcase๋ฅผ ์ฐ๋๊ฒ ๋ฌ๋ค.


๋ฐ์๋ objectํธ์ถํ๋ ๋ฐฉ๋ฒ 

let heroes = {
  name: "Superman",
  age: 33,
  "current address": "์ ์ฃผ์ ํ๊ฒฝ๋ฉด ํํฌ๋ฆฌ",
};

console.log(heroes.name);
console.log(heroes.age);
console.log(heroes["current address"]);

*/

/*
๋ฌธ์ 1 :

Primitiveํ์๊ณผ Structed types์ด ์๋๋ฐ Object๋ ์ด๋ ํ์์ ์ํ๋์ง ์ ์ผ์ธ์.
*/

/*
๋ฌธ์ 2 :

Object๋ mutable์ผ์ง unmutable์์ง ์๊ฐํด๋ณด์ธ์.

````


<details><summary><b>Answer</b></summary>

<p>

```javascript
๋ฌธ์  1 : 
Structed types

๋ฌธ์  2 :
 mutable 
````

 </p>
 </details>
 <br>
 <br>



### ๐ Object - adding properties

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Object - adding properties


```javascript
์์ฝ : 

๊ธฐ์กด์ object์ ์๋ก์ด properties๋ฅผ ์ถ๊ฐ ํ  ๋ key์ ""๋ฅผ ๋ถ์ด๋ ๋ฌธ๋ฒ์ ์ด๋ค. ํ์ง๋ง ์ด ๋ฐฉ๋ฒ๋ ํด์๋ ์๋๋ค.
ex)
key์ "current Address" ์ด๋ ๊ฒ ํด์๋ ์๋๋ค. ๋์  CamelCase๋ฅผ ์ฐ์
=> currentAddress

๋์ค์ ๋ฐฐ์ธ ๋ด์ฉ
์ธ๋ถ์์ properties๋ฅผ ์ถ๊ฐํ  ๋๋ [] ๋ฐฉ์์ผ๋ก ํ๋ค.


let heroes = {
  name: "Superman",
  age: 33,
  currentAddress: "์ ์ฃผ์ ํ๊ฒฝ๋ฉด ํํฌ๋ฆฌ",
};

let newKey = "sex"; // don't do that
heroes[newKey] = "male" // don't do that

console.log(heroes.name);
console.log(heroes.age);
console.log(heroes.currentAddress);
console.log(heroes["newKey"]); // don't do that


*/

/*
๋ฌธ์ 1 :

let person = {
  firstName: "SeoYeon",
  age: "25"
}

console.log(person.firstName + " is " + person.age + " years old.");

์ถ๋ ฅ๊ฐ์ ์์ฑํ์ธ์.

````


<details><summary><b>Answer</b></summary>

<p>

```javascript
SeoYeon is 25 years old.

````

 </p>
 </details>
 <br>
 <br>



### ๐ Object constructor function

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Object constructor function


```javascript
์์ฝ : 

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

์ 2๊ฐ์ function์ ๊ฐ์ ์๋ฏธ๋ฅผ ์ง๋๋ค.
๊ทธ๋ฆฌ๊ณ  ์ด 2๊ฐ์ function์ ๊ตฌ์กฐ๋ฅผ ๊ฐ์ง๊ณ  ์๋ ๋ฐ์ดํฐ ํ์์ ๋ง๋ค์ด๋ด๋ function์ด๋ผ๊ณ  ํด์
object constructor function์ด๋ผ๊ณ  ํ๋ค.


*/


/*
๋ฌธ์ 1 :

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

์ ์ฝ๋๋ฅผ ๋ ๊ฐ๊ฒฐํ๊ฒ ์์ฑํด๋ณด์ธ์.

````


<details><summary><b>Answer</b></summary>

<p>

```javascript

function init(type, flavor, levels, price, occasion) {
  return {
    type, 
    flavor, 
    levels, 
    price, 
    occasion, 
  }
}

````

 </p>
 </details>
 <br>
 <br>



### ๐ Object ( for...in )

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Object ( for...in )


```javascript
์์ฝ : 

์ด๋ค Object์ ์๋ key๋ง ๋ฝ์์ ๋ณด๋ ๋ฐฉ๋ฒ

let codes = {
  "49" :"Germany",
  "41" :"Switzerland",
  "44" :"Great Britatin",
  "1" :"USA",
};

//key๋ผ๋ ๋จ์ด๋ ์์๋ก ์ ํ๊ฒ์ผ๋ก ์ด๋ ํ ๋จ์ด๊ฐ ์ค๋๋ผ๋ ์๊ด์๋ค.
for(let key in codes) { 
  console.log(key); // key๊ฐ ์ซ์์ด๋ฉด ์์์์๋ถํฐ ์ถ๋ ฅ
}

*/

/*
๋ฌธ์ 1 : 

var arr = [3, 5, 7];
arr.foo = "hello";

for (var i in arr) {
   console.log(i); 
}

for (var i of arr) {
   console.log(i); 
}

์ถ๋ ฅ ๊ฐ์ ์ ์ผ์ธ์.

````


<details><summary><b>Answer</b></summary>

<p>

```javascript
for (var i in arr) {
   console.log(i); 
}
=> 0, 1, 2, foo

for (var i of arr) {
   console.log(i); 
}
=> 3, 5, 7
````

 </p>
 </details>
 <br>
 <br>



### ๐ Object - copy by reference

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Object - copy by reference


```javascript

์์ฝ : 

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

์ถ๋ ฅ๊ฐ์ 
Batman
Batman
Batman
์ด ๋์ค๋๋ฐ

๊ทธ ์ด์ ๋ Object๋ฅผ ๋ณต์ฌํด์ ์๋ก ๋ง๋ ๊ฒ ์๋ Object์ ๋ฉ๋ชจ๋ฆฌ ์ฃผ์๊ฐ์ ๋ณต์ฌํ๊ธฐ ๋๋ฌธ์ด๋ค.

*/

/*

๋ฌธ์ 1 :

let obj = {
  a: 1,
  b: 2,
};
let copy = obj;

obj.a = 5;
console.log(copy.a);

์ถ๋ ฅ ๊ฐ์ ์ ์ผ์ธ์.

````


<details><summary><b>Answer</b></summary>

<p>

```javascript
5
````

 </p>
 </details>
 <br>
 <br>


