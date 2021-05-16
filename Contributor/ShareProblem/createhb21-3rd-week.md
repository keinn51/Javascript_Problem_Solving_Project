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

