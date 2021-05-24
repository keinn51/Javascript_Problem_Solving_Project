# Creathb21's Problems



### 🎁 Object Cloning

<br>

### 난이도 : 🌶

<br>

#### ☁︎  Object Cloning


```javascript

요약 : 

let student1 = {
  name: "Superman",
  study: "JavaScript",
}

let student2 = {};

for (let key in student1) {
  student2[key] = student1[key];
}

student2.name = "Birdman";



console.log(student1.name);
console.log(student2.name);


문제 1 :

요약에 나온대로 코드를 진행하면 student2.name에서 빨간줄이 표시된다.
아직 for 구문이 실행되지 않았기 때문인데 어떻게 코드를 바꾸면 빨간줄 표시를 사라지게 할 수 있을지 생각해 보세요.

````


<details><summary><b>Answer</b></summary>

<p>

```javascript


````

 </p>
 </details>
 <br>
 <br>

### 🎁 Object Deep Cloning


<br>

### 난이도 : 🌶

<br>
 
#### ☁︎  Object Deep Cloning



```javascript

요약 : 

let student1 = {
  name: "Superman",
  study: {
    field: "Javascript",
    year: 3,
  }
}

let student2 = {
  name: "Ironman"
  study: {
    field: ""
  }
};

Object.assign(student2, student1);

student2.name = "Birdman";
student2.study.filed = "Haskell"";



console.log(student1.study);
console.log(student2.study);
console.log(student1.field);


Object를 assign할 떄 오브젝트안에 있는 오브젝트는 완벽히 메모리 주소가 분리되서 복제되지 않는다.
오브젝트 안에 있는 오브젝트까지 복제하는걸 Deep Cloning이라고 한다.
이것은 Library를 이용해서 처리한다.


*/

/*

문제1 :

function copy(mainObj) {
  let objCopy = {}; // objCopy will store a copy of the mainObj
  let key;

  for (key in mainObj) {
    objCopy[key] = mainObj.key; // copies each property to the objCopy object
  }
  return objCopy;
}

const mainObj = {
  a: 2,
  b: 5,
  c: {
    x: 7,
    y: 4,
  },
}

console.log(copy(mainObj));

출력 값을 적으세요.
*/

/*
문제2 :

let obj = {
  a: 1,
  b: 2,
};
let objCopy = Object.assign({}, obj);
console.log(objCopy);

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


### 🎁 Object Object assign

<br>

### 난이도 : 🌶

<br>

#### ☁︎  Object Object assign


```javascript
요약 :

빨간 표시가 있고 코드가 실행되더라도 그것은 잘못된 방식이다.


let student1 = {
  name: "Superman",
  study: "JavaScript",
}

let student2 = {
  name: "Iron"",
  study: "",
};

console.log(student2.name);

Object.assign(student2, student1);

student2.name = "Birdman";


console.log(student1.name);
console.log(student2.name);
console.log(student2.study);

````


<details><summary><b>Answer</b></summary>

<p>

```javascript



````

 </p>
 </details>
 <br>
 <br>


### 🎁 Object method "this"

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Object method "this"


```javascript

요약 :

this는 가급적 쓰지 않아야 한다.
꼭 써야할 때는 정확히 이해하고, 매우 조심해서 사용해야 한다.

Dot notation : 점 앞에 있는 무엇(Object)가 주어, 점 뒤에 있는 무었(function)이 동사.


let superman = {
  name: `Superman`,
  age: 30,
  skill: function() { // 여기서는 this가 무엇인지 모른다. 다만 짐작할 뿐이다.
    console.log(`I am ${this.name}, I can fly!`)
  }
}

let birdman = {
  name: `Birdman`,
  age: 30,
  skill: function() {
    console.log(`I am ${this.name}, I can fly!`)
  }
}


superman.skill(); // 여기서 this가 무엇인지 결정난다.

function learn() {
  console.log(`I am ${this.name}, I study Javascript basic with Team Jupeter.`)
}

learn(); // 이걸 출력하면 this는 previewFrame으로 인식함

superman.learn(); // 바람직 하지 않은 방법, learn이 기존의 superman의 property로 오해할 수 있다.
superman['learn'](); // learn은 외부에서 가져왔으므로 이렇게 써줘야함

birdman['learn']();
*/


/*


문제1 :

var person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};

출력값이 "John Doe"가 되도록 표시하세요.

*/

/*
문제2 :

function myFunction() {
  return this;
}

출력값을 작성하세요.
*/

/*

문제3 :

"use strict";
function myFunction() {
  return this;
}

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


### 🎁 주어(Object)와 동사(Function)의 어울림
<br>

### 난이도 : 🌶

<br>

#### ☁︎ 주어(Object)와 동사(Function)의 어울림


```javascript
요약 :

앞 강의에서 learn function은 주어 + 동사처럼 잘 어울리지 않았다.
그래서 그 결과로 previewFrame이 출력되었는데 이것을 어울리게 만들어 주어야 한다.


let superman = {
  name: `Superman`,
  age: 30,
  skill: function() { 
    console.log(`I am ${this.name}, I can fly!`)
  }
}

let birdman = {
  name: `Birdman`,
  age: 30,
  skill: function() {
    console.log(`I am ${this.name}, I can fly!`)
  }
}

function study() {
  console.log(`I am ${this.name}, I study Javascript basic with Team Jupeter.`)
}



superman['learn'] = study; // 어울리게 해주기
superman['learn']();

birdman['learn'] = study; // 어울리게 해주기
birdman['learn']();


````


<details><summary><b>Answer</b></summary>

<p>

```javascript


````

 </p>
 </details>
 <br>
 <br>


### 🎁 Constructor operator - new

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Constructor operator - new


```javascript
요약 :

// constructor 방식
function Hero(name, age = 30) {
  this.name = name;
  this.age = age;
  this.skill = function() {
    return `I always win`
  }
}

let superman = new Hero(`Superman`, 25);
let wolverine = new Hero(`Wolverine`);
let wolverine = new Hero(`atman`);
let wolverine = new Hero(`xman`, 50);
let wolverine = new Hero(`Dr. starnge`, 50);

console.log(superman.age);
console.log(wolverine.age);
console.log(wolverine.skill());

// 프로그래머들간의 약속이, new 라는것을 Object를 만들 때는 대문자를 써준다.

// Object literal 방식
let Birdman = {
  name: `Birdman`,
  age: 55,
  address: `Seoguipo Jungmun`,
  skill: function() {
    return `I can fly`;
  }
}

console.log(Birdman.name);
console.log(Birdman.age);
console.log(Birdman.skill());

````


<details><summary><b>Answer</b></summary>

<p>

```javascript


````

 </p>
 </details>
 <br>
 <br>


### 🎁 Array Destructuring 기초

<br>

### 난이도 : 🌶

<br>

#### ☁︎  Array Destructuring 기초


```javascript


````


<details><summary><b>Answer</b></summary>

<p>

```javascript

요약 :

한번에 할당하는 것

let heros = [`Superman`, `Xman`];

let [hero1, hero2] = heroes;

console.log(hero1);
console.log(hero2);

*/

/*
문제1 :

var x = 1, y = 2;
[x, y] = [y, x];
console.log(x, y);

출력 값을 작성하세요.
*/

/*
문제2 :

var [x, , z] = [1, 2, 3];
console.log(x, z);

출력 값을 작성하세요.
````

 </p>
 </details>
 <br>
 <br>


### 🎁 Array Destructuring 응용

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Array Destructuring 응용


```javascript
요약 :

let heros = [`Superman`, `Xman`];

let hero1 = heroes[0],
    hero2 = heroes[1];
console.log(hero1); // `Superman`
console.log(hero2); // `Xman`

------------------------------------------

let [ ,hero2] = heroes;
console.log(hero2); // `Xman`

// string: array of characters(문자들의 배열)
let [a, b, c] = "abc";
// let [a, b, c] = [`a`,`b`,`c`]; 위와 똑같은 의미이다.
console.log(a);
console.log(b);
console.log(c);

````


<details><summary><b>Answer</b></summary>

<p>

```javascript


````

 </p>
 </details>
 <br>
 <br>


### 🎁 Default Values

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Default Values


```javascript


````


<details><summary><b>Answer</b></summary>

<p>

```javascript
요약 :

... :배열 중 나머지 것들을 보여주는 것

let heroes = [`Superman`, `Xman`, `Birdman`, `Catgirl`, `Wondergirl`];

let [hero1, hero2, ...otherHeroes] = heroes;

console.log(hero1);
console.log(hero2);
console.log(otherHeroes);
console.log(otherHeroes[0]);
console.log(otherHeroes[2]);

---------------------------------------------------------

let [hero1, hero2, hero3, hero4, hero5, hero6 = `Jupeter`] = heroes; // 여기서 (= Jupeter)는 default argument(=value)라고 한다.
// default value에는 value뿐만 아니라 function도 들어갈 수 있다.

console.log(hero6);



*/

/*

문제1 :

function test(num = 1) {
  console.log(typeof num);
}

test();          
test(undefined); 

test('');        
test(null);

출력 값을 작성하세요.

````

 </p>
 </details>
 <br>
 <br>


