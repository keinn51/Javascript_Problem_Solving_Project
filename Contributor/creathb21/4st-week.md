# Creathb21's Problems



### ๐ Object Cloning

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ  Object Cloning


```javascript

์์ฝ : 

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


๋ฌธ์  1 :

์์ฝ์ ๋์จ๋๋ก ์ฝ๋๋ฅผ ์งํํ๋ฉด student2.name์์ ๋นจ๊ฐ์ค์ด ํ์๋๋ค.
์์ง for ๊ตฌ๋ฌธ์ด ์คํ๋์ง ์์๊ธฐ ๋๋ฌธ์ธ๋ฐ ์ด๋ป๊ฒ ์ฝ๋๋ฅผ ๋ฐ๊พธ๋ฉด ๋นจ๊ฐ์ค ํ์๋ฅผ ์ฌ๋ผ์ง๊ฒ ํ  ์ ์์์ง ์๊ฐํด ๋ณด์ธ์.

````


<details><summary><b>Answer</b></summary>

<p>

```javascript
let student1 = {
        name: "Superman",
        study: "Javascript"
      }

      let student2 = {};

      for (let key in student1) {
        student2[key] = student1[key];
      }

      console.log(student2); // {name: "Superman", study: "Javascript"}

      student2.name = "Birdman";

      console.log(student1.name);   // Superman
      console.log(student2.name);   // Birdman

````

 </p>
 </details>
 <br>
 <br>

### ๐ Object Deep Cloning


<br>

### ๋์ด๋ : ๐ถ

<br>
 
#### โ๏ธ  Object Deep Cloning



```javascript

์์ฝ : 

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


Object๋ฅผ assignํ  ๋ ์ค๋ธ์ ํธ์์ ์๋ ์ค๋ธ์ ํธ๋ ์๋ฒฝํ ๋ฉ๋ชจ๋ฆฌ ์ฃผ์๊ฐ ๋ถ๋ฆฌ๋์ ๋ณต์ ๋์ง ์๋๋ค.
์ค๋ธ์ ํธ ์์ ์๋ ์ค๋ธ์ ํธ๊น์ง ๋ณต์ ํ๋๊ฑธ Deep Cloning์ด๋ผ๊ณ  ํ๋ค.
์ด๊ฒ์ Library๋ฅผ ์ด์ฉํด์ ์ฒ๋ฆฌํ๋ค.


*/

/*

๋ฌธ์ 1 :

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

์ถ๋ ฅ ๊ฐ์ ์ ์ผ์ธ์.
*/

/*
๋ฌธ์ 2 :

let obj = {
  a: 1,
  b: 2,
};
let objCopy = Object.assign({}, obj);
console.log(objCopy);

์ถ๋ ฅ ๊ฐ์ ์ ์ผ์ธ์.

````


<details><summary><b>Answer</b></summary>

<p>

```javascript

๋ฌธ์  1 : {a: undefined, b: undefined, c: undefined}

๋ฌธ์  2 : {a: 1, b: 2}
````

 </p>
 </details>
 <br>
 <br>


### ๐ Object Object assign

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ  Object Object assign


```javascript
์์ฝ :

๋นจ๊ฐ ํ์๊ฐ ์๊ณ  ์ฝ๋๊ฐ ์คํ๋๋๋ผ๋ ๊ทธ๊ฒ์ ์๋ชป๋ ๋ฐฉ์์ด๋ค.


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


### ๐ Object method "this"

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Object method "this"


```javascript

์์ฝ :

this๋ ๊ฐ๊ธ์  ์ฐ์ง ์์์ผ ํ๋ค.
๊ผญ ์จ์ผํ  ๋๋ ์ ํํ ์ดํดํ๊ณ , ๋งค์ฐ ์กฐ์ฌํด์ ์ฌ์ฉํด์ผ ํ๋ค.

Dot notation : ์  ์์ ์๋ ๋ฌด์(Object)๊ฐ ์ฃผ์ด, ์  ๋ค์ ์๋ ๋ฌด์(function)์ด ๋์ฌ.


let superman = {
  name: `Superman`,
  age: 30,
  skill: function() { // ์ฌ๊ธฐ์๋ this๊ฐ ๋ฌด์์ธ์ง ๋ชจ๋ฅธ๋ค. ๋ค๋ง ์ง์ํ  ๋ฟ์ด๋ค.
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


superman.skill(); // ์ฌ๊ธฐ์ this๊ฐ ๋ฌด์์ธ์ง ๊ฒฐ์ ๋๋ค.

function learn() {
  console.log(`I am ${this.name}, I study Javascript basic with Team Jupeter.`)
}

learn(); // ์ด๊ฑธ ์ถ๋ ฅํ๋ฉด this๋ previewFrame์ผ๋ก ์ธ์ํจ

superman.learn(); // ๋ฐ๋์ง ํ์ง ์์ ๋ฐฉ๋ฒ, learn์ด ๊ธฐ์กด์ superman์ property๋ก ์คํดํ  ์ ์๋ค.
superman['learn'](); // learn์ ์ธ๋ถ์์ ๊ฐ์ ธ์์ผ๋ฏ๋ก ์ด๋ ๊ฒ ์จ์ค์ผํจ

birdman['learn']();
*/


/*


๋ฌธ์ 1 :

var person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};

์ถ๋ ฅ๊ฐ์ด "John Doe"๊ฐ ๋๋๋ก ํ์ํ์ธ์.

*/

/*
๋ฌธ์ 2 :

function myFunction() {
  return this;
}

์ถ๋ ฅ๊ฐ์ ์์ฑํ์ธ์.
*/

/*

๋ฌธ์ 3 :

"use strict";
function myFunction() {
  return this;
}

์ถ๋ ฅ๊ฐ์ ์์ฑํ์ธ์.
````


<details><summary><b>Answer</b></summary>

<p>

```javascript
๋ฌธ์  1 : person.fullName();

๋ฌธ์  2 : undefined
         
๋ฌธ์  3 : undefined


````

 </p>
 </details>
 <br>
 <br>


### ๐ ์ฃผ์ด(Object)์ ๋์ฌ(Function)์ ์ด์ธ๋ฆผ
<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ ์ฃผ์ด(Object)์ ๋์ฌ(Function)์ ์ด์ธ๋ฆผ


```javascript
์์ฝ :

์ ๊ฐ์์์ learn function์ ์ฃผ์ด + ๋์ฌ์ฒ๋ผ ์ ์ด์ธ๋ฆฌ์ง ์์๋ค.
๊ทธ๋์ ๊ทธ ๊ฒฐ๊ณผ๋ก previewFrame์ด ์ถ๋ ฅ๋์๋๋ฐ ์ด๊ฒ์ ์ด์ธ๋ฆฌ๊ฒ ๋ง๋ค์ด ์ฃผ์ด์ผ ํ๋ค.


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



superman['learn'] = study; // ์ด์ธ๋ฆฌ๊ฒ ํด์ฃผ๊ธฐ
superman['learn']();

birdman['learn'] = study; // ์ด์ธ๋ฆฌ๊ฒ ํด์ฃผ๊ธฐ
birdman['learn']();


````


<details><summary><b>Answer</b></summary>

<p>

```javascript

superman['learn'](); // I am Superman, I study Javascript basic with Team Jupeter.
birdman['learn'](); // I am Birdman, I study Javascript basic with Team Jupeter.

````

 </p>
 </details>
 <br>
 <br>


### ๐ Constructor operator - new

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Constructor operator - new


```javascript
์์ฝ :

// constructor ๋ฐฉ์
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

// ํ๋ก๊ทธ๋๋จธ๋ค๊ฐ์ ์ฝ์์ด, new ๋ผ๋๊ฒ์ Object๋ฅผ ๋ง๋ค ๋๋ ๋๋ฌธ์๋ฅผ ์จ์ค๋ค.

// Object literal ๋ฐฉ์
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

console.log(superman.age);   // 25 
console.log(wolverine.age);   // 50
console.log(wolverine.skill());   // I always win


````

 </p>
 </details>
 <br>
 <br>


### ๐ Array Destructuring ๊ธฐ์ด

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ  Array Destructuring ๊ธฐ์ด


```javascript
์์ฝ :

ํ๋ฒ์ ํ ๋นํ๋ ๊ฒ

let heros = [`Superman`, `Xman`];

let [hero1, hero2] = heroes;

console.log(hero1);
console.log(hero2);

*/

/*
๋ฌธ์ 1 :

var x = 1, y = 2;
[x, y] = [y, x];
console.log(x, y);

์ถ๋ ฅ ๊ฐ์ ์์ฑํ์ธ์.
*/

/*
๋ฌธ์ 2 :

var [x, , z] = [1, 2, 3];
console.log(x, z);

์ถ๋ ฅ ๊ฐ์ ์์ฑํ์ธ์.



````


<details><summary><b>Answer</b></summary>

<p>

```javascript

๋ฌธ์  1 : console.log(x, y);   // 2, 1

๋ฌธ์  2 : console.log(x, z);  // 1, 3

````

 </p>
 </details>
 <br>
 <br>


### ๐ Array Destructuring ์์ฉ

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Array Destructuring ์์ฉ


```javascript
์์ฝ :

let heros = [`Superman`, `Xman`];

let hero1 = heroes[0],
    hero2 = heroes[1];
console.log(hero1); // `Superman`
console.log(hero2); // `Xman`

------------------------------------------

let [ ,hero2] = heroes;
console.log(hero2); // `Xman`

// string: array of characters(๋ฌธ์๋ค์ ๋ฐฐ์ด)
let [a, b, c] = "abc";
// let [a, b, c] = [`a`,`b`,`c`]; ์์ ๋๊ฐ์ ์๋ฏธ์ด๋ค.
console.log(a);
console.log(b);
console.log(c);

````


<details><summary><b>Answer</b></summary>

<p>

```javascript

console.log(a);  // a
console.log(b);   // b
console.log(c);   // c

````

 </p>
 </details>
 <br>
 <br>


### ๐ Default Values

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Default Values


```javascript

์์ฝ :

... :๋ฐฐ์ด ์ค ๋๋จธ์ง ๊ฒ๋ค์ ๋ณด์ฌ์ฃผ๋ ๊ฒ

let heroes = [`Superman`, `Xman`, `Birdman`, `Catgirl`, `Wondergirl`];

let [hero1, hero2, ...otherHeroes] = heroes;

console.log(hero1);
console.log(hero2);
console.log(otherHeroes);
console.log(otherHeroes[0]);
console.log(otherHeroes[2]);

---------------------------------------------------------

let [hero1, hero2, hero3, hero4, hero5, hero6 = `Jupeter`] = heroes; // ์ฌ๊ธฐ์ (= Jupeter)๋ default argument(=value)๋ผ๊ณ  ํ๋ค.
// default value์๋ value๋ฟ๋ง ์๋๋ผ function๋ ๋ค์ด๊ฐ ์ ์๋ค.

console.log(hero6);



*/

/*

๋ฌธ์ 1 :

function test(num = 1) {
  console.log(typeof num);
}

test();          
test(undefined); 

test('');        
test(null);

์ถ๋ ฅ ๊ฐ์ ์์ฑํ์ธ์.

````


<details><summary><b>Answer</b></summary>

<p>

```javascript

test();  // number
test(undefined);  // number
test('');        // string
test(null);      // number

````

 </p>
 </details>
 <br>
 <br>


