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

````

 </p>
 </details>
 <br>
 <br>

