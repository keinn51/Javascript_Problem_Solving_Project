# Creathb21's Problems



### ๐ Evaluation, Expression, Statement

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Evaluation, Expression, Statement


```Javascript ์ฝ๋ ๋ค์๋ ์ข์ข ; ์๋ฐ์ (semi-colon)์ ๋ณผ ์ ์๋๋ฐ, ์ด๊ฒ์ Statement๋ค์ ๊ตฌ๋ถ์ง๊ณ  ์์์ ์ผ๋ก ์ด Statement๊ฐ ๋๋ฌ๋ค๋ผ๋ ๋ป์ผ๋ก ์ฌ์ฉ๋ฉ๋๋ค. 

๋ฌธ์  1 : ๋ค์์ ๋ฌธ์ ๋ค์ ์๋ง์ ์ ๋ต๊ณผ ๋งค์นญํ์ธ์.
1. ํ๋ก๊ทธ๋๋ฐ์์ ์ฝ๋๋ ๋ฌด์์ธ๊ฐ์? 
2. ํ๋ก๊ทธ๋๋ฐ์์ Statement์ด๋ ๋ฌด์์ธ๊ฐ์? 
3. ํ๋ก๊ทธ๋๋ฐ์์ Expression์ด๋ ๋ฌด์์ธ๊ฐ์? 
4. ํ๋ก๊ทธ๋๋ฐ์์ Evaluation์ด๋ ๋ฌด์์ธ๊ฐ์? 

a. ์ปดํจํฐ์๊ฒ ์ด๋ ํ ๊ฐ์ ๊ฐ์ ธ์ค๋ผ๋ ๋ช๋ น
b. ์ปดํจํฐ๊ฐ ์ฝ์ ์ ์๋ ์ธ์ด
c. ์ปดํจํฐ๊ฐ ์ฝ๋๋ฅผ ์ฝ๊ณ  ๊ณ์ฐ์ํด์ ๋ด๋ ๊ฒฐ๊ณผ๊ฐ
d. ์ปดํจํฐ์๊ฒ ๋ฌด์์ ํ๋ผ๊ณ  ๋ด๋ฆฌ๋ ๋ช๋ น


๋ฌธ์  2 : 
let math = 2 + 3;
console.log(math);

๋ค์์ 5๋ฅผ ์ถ๋ ฅํ๋ ๊ฐ๋จํ ์ฝ๋์๋๋ค. ์ฌ๊ธฐ์ ์ด๋ค๊ฒ์ด Statement, Expression ๊ทธ๋ฆฌ๊ณ  Evaluation์ธ์ง ์๊ฐํด๋ณด์ธ์.



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


### ๐ variables

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ  variables

```javascript

vary(๋ณํ๋ค) + able(ํ  ์ ์๋ค) 

๋ณ์๋ "์ด๋ค ๊ด๊ณ๋ ๋ฒ์ ์์์ ์ฌ๋ฌ ๊ฐ์ง ๊ฐ์ผ๋ก ๋ณํ  ์ ์๋ ์"๋ฅผ ๋งํฉ๋๋ค.

Javascript๋ด์์ ๋ณ์๋ฅผ ์์ฑํ ๋ ค๋ฉด, ๋จผ์  ๋ณ์๋ฅผ ์ ์ธ(declaration)ํด์ค์ผํฉ๋๋ค.
let food;

์ด food๋ผ๋ ๋ณ์๋ฅผ ํ์ผ๋ด์ ์ ์ธํจ์ผ๋ก์จ, ์ด food ๋ณ์๋ ํ์ผ๋ด์ ์กด์ฌํ๊ฒ๋ฉ๋๋ค. ์ฐ๋ฆฌ๋ ์ด food๋ผ๋ ๋ณ์๋ฅผ ์ฌ์ฉ ํ  ์ ์๊ณ , ๊ฐ์ ํ ๋นํ  ์ ์์ต๋๋ค.

๋ณ์์ ๊ฐ์ ๋ด์๋ ์ฐ๋ฆฌ๋ ์ด๊ฒ์ ์ด๊ธฐํ(Initialization)๋ผ๊ณ  ๋ถ๋ฆ๋๋ค.
let food = "pizza";

๋ ์ฌ์ด ์์ ๋ฅผ ๋ค์๋ฉด, 
let box = "something" ์ ๊ฐ์ ๋ด๋ ์์๋ฅผ ํ์ผ๋ด์ ์กด์ฌํ๋ค๊ณ  ์ ์ธํ๊ณ , ์์์์ ์ฐ๋ฆฌ๊ฐ ์ํ๋ ๊ฐ(something)์ผ๋ก ์ด๊ธฐํํฉ๋๋ค.
๋ณ์์ ๊ฐ์ ๊ฒ์ํด์ ์ฌํ ๋น ํ  ์ ์์ต๋๋ค.
box = "toy";
box = "food";

๋ณ์์ ํ ๋น๋๋ ๊ฐ์ด ๋ฌธ์์ผ ๊ฒฝ์ฐ  " "๋ ' '๋ก ๋ฌถ์ด์ค์ผํฉ๋๋ค.

Javascript๋ด์์ ๋ณ์๋ฅผ ์ ์ธํ ๋ ์ฌ์ฉ๋๋ ํค์๋๋ let, var, const๋ฑ ์ด ์๊ณ , ๊ฐ๊ฐ์ ๋ค๋ฅธ ์ฉ๋๋ฅผ ๊ฐ์ง๊ณ ์์ต๋๋ค. 


๋ฌธ์  1 : let ํค์๋๋ฅผ ์ฌ์ฉํด juice๋ผ๋ ๋ณ์๋ฅผ ์ ์ธํ๊ณ , juice ๋ณ์์ apple juice๋ผ๋ ๊ฐ์ ํ ๋นํ์ธ์. ๊ทธ๋ฆฌ๊ณ  console.log()๋ฅผ ์ด์ฉํด juice๋ณ์๋ฅผ ์ถ๋ ฅํ์ธ์.

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

### ๐ let and const

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ variables


 ```javascript

๋ฌธ์  1 : ์ง๊ธ๊น์ง ๋ฐฐ์ด ์ ์ธ๊ณผ ์ด๊ธฐํ ๊ฐ๋์ํตํด, iceCream์ด๋ผ๋ ์ฃผ์ด์ง ๋ณ์์ ๊ฐ์ ์ถ๋ ฅํด๋ณด์ธ์. ์ถ๋ ฅ๋๋ ๊ฐ์ 
choco
vanilla
์ด์ฌ์ผ ํฉ๋๋ค

๋ฌธ์  2 : const ํค์๋๋ฅผ ์ด์ฉํด ๋ณ์๋ฅผ ์ ์ธ ๋ฐ ์ด๊ธฐํํด๋ณด์ธ์.


// ๋ฌธ์  1
let iceCream; // ์ ์ธ(Declaration)
// iceCream = " " // ์ด๊ธฐํ(Initialization)
// console.log() // ์ถ๋ ฅ


// ๋ฌธ์  2

````



<details><summary><b>Answer</b></summary>

  <p>

```javascript
๋ฌธ์ 1 
let iceCream;
iceCream = "choco vanila"
console.log(iceCream);

๋ฌธ์ 2
const candy = red;

````

 </p>
 </details>
 <br>
 <br>


### ๐ Datatypes

<br>


### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Data type


```javascript

์๋ฐ์คํฌ๋ฆฝํธ์์ ์ฌ์ฉ๋๋ ๋ฐ์ดํฐ ์ ํ(Data type)์ ์ฌ๋ฌ๊ฐ์ง๊ฐ ์์ต๋๋ค.


๋ค์์ ๋ํ์ ์ผ๋ก ์ฌ์ฉ๋๋ ๋ฐ์ดํฐ ์ ํ๋ค ์๋๋ค.
string = ๋ฌธ์์ด
number = ์ซ์
boolean = ์ฐธ ํน์ ๊ฑฐ์ง(true or false)์ ๊ฐ์ง ๋ฐ์ดํฐ๋ฅผ returnํฉ๋๋ค
undefined = ๋ณ์๊ฐ ์ ์ธ๋ง๋๊ณ  ์์ง ๊ฐ์ด ํ ๋น(์ด๊ธฐํ)๋์ง ์์์๋๋ฅผ ์๊ธฐํฉ๋๋ค.
null = 0๊ณผ ๊ฐ์

์์ง ๋ฐฐ์ฐ์ง์๋ ๋ฐ์ดํฐ ์ ํ๋ค
object
symbol(ES6์์ ์ถ๊ฐ๋จ)

๋ฌธ์  1 : ํ์ฌ ์๋์ ๋ณ์๋ค์ ์ ์ธ(declaration)๋ง ๋์ด์๋ ์ํ์๋๋ค. ์๋์ ๋ณ์๋ค์ ์ด๋ฆ์ ๊ฐ๊ฐ์ ๋ง๋ ๋ฐ์ดํฐ ์ ํ(data type)์ ํ ๋นํ์ธ์.

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

### ๐ Type Conversion

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Type Conversion


 ```javascript
Type Conversion
Type = ์ ํ
Conversion = ๋ณํํ๋ค 
String = ๋ฌธ์์ด
Number = ์ซ์

Type Conversion์ ๋ฐ์ดํฐ์ ์ ํ์ ๋ณํํ๋ค๋ ๋ป ์๋๋ค.
Javascript์์ ์ฌ์ฉํ  ์ ์๋ ์ฌ๋ฌ ๋ฐ์ดํฐ ์ ํ๋ค, ์ซ์, ๋ฌธ์์ด, Boolean ๋ฑ์ ๋ค๋ฅธ ๋ฐ์ดํฐ ์ ํ์ผ๋ก ๋ฐ๊ฟ ์ ์์ต๋๋ค.
์ซ์ -> ๋ฌธ์์ด
๋ฌธ์์ด - > ์ซ์...

let value = 13; 
console.log(typeof value);
a๋ผ๋ ๋ณ์๋ 13์ด๋ผ๋ ์ซ์ ๋ฐ์ดํฐ ์ ํ์ธ ๊ฐ์ ๊ฐ์ง๊ณ  ์์ต๋๋ค. 
์ด ๋ณ์๊ฐ ๊ฐ์ง ๋ฐ์ดํฐ ์ ํ์ ๋ณด๋ ค๋ฉด typeof ๋ณ์์ด๋ฆ ์ ์๋ ฅํ๋ฉด๋ฉ๋๋ค
๊ฒฐ๊ณผ๊ฐ์ผ๋ก number ๊ฐ ์ถ๋ ฅ๋ฉ๋๋ค.

์ฐ๋ฆฌ๋ ์ด 13์ด๋ผ๋ ์ซ์๋ฅผ String()ํจ์๋ฅผ ์ด์ฉํด ๋ฌธ์์ด๋ก ๋ณํ์ํฌ ์ ์์ต๋๋ค.
value = String(value) // ๋ฐ์ดํฐ ์ ํ์ String()ํจ์๋ฅผ ์ด์ฉํด String๋ก ๋ณ๊ฒฝ
console.log(typeof value); // 13์ด ์ซ์๊ฐ์๋ ๋ฌธ์์ด๋ก ์ถ๋ ฅ๋จ

๋ฐ๋๋ก ๋ฌธ์์ด ๋ฐ์ดํฐ ์ ํ์๊ฐ์ง ๊ฐ์ ์ซ์๋ก ๋ณํ์ํฌ ์ ์์ต๋๋ค.
let str = "123";
str = (typeof str) // String ์ถ๋ ฅ

let num = Number(str); // ๋ฐ์ดํฐ ์ ํ์ Number()ํจ์๋ฅผ ์ด์ฉํด Number๋ก ๋ณ๊ฒฝ
console.log(typeof num); // Number ์ถ๋ ฅ



๋ฌธ์์ด ๋ฐ์ดํฐ ์ ํ์ธ "I am"๊ณผ ์ซ์ ๋ฐ์ดํฐ ์ ํ์ธ 13์ ๋ํ๋ฉด ์ด๋ป๊ฒ๋ ๊น์?
console.log("I am" + 12)
I am12 ๊ฐ ์ถ๋ ฅ์ด ๋ฉ๋๋ค.

์ ๊ฐ์์ Variable์์ ๋ฌธ์์ด(string)์ ์ฌ์ฉํ ๋ ค๋ฉด ๋ฌธ์์ด์ " "๋ ' '๋ก ๋ฌถ์ด์ค์ผํ๋ค๊ณ  ํ์์ต๋๋ค, ๊ทธ ๋ง์ 2๋ ์ซ์์ง๋ง, "2"๋ ๋ฌธ์์ด์ด ๋๋ค๋ ๋ป์๋๋ค.

์ด๋ฒ์๋ a๋ผ๋ ๋ณ์๋ฅผ 5 + "6"๋ก ์ด๊ธฐํํ์ฌ, ์ถ๋ ฅํ๋ฉด ์ด๋ป๊ฒ๋ ๊น์?
let a = 5 + "6";
console.log(a);
56์ด ์ถ๋ ฅ์ด๋ฉ๋๋ค.





๋ฌธ์  1 :
let c = 13;
13์ด๋ผ๋ ์ซ์ ๋ฐ์ดํฐ ์ ํ์ ๊ฐ์ง๊ณ  ์๋ ๋ณ์ C๊ฐ ์์ต๋๋ค.
์ด ์ซ์ 13์ ๋ฌธ์์ด๋ก ๋ณํํด๋ณด์ธ์.


๋ฌธ์  2 :
let something = "1000";
"1000" ์ด๋ผ๋ ๋ฌธ์์ด ๋ฐ์ดํฐ ์ ํ์ ๊ฐ์ง๊ณ  ์๋ ๋ณ์ something๊ฐ ์์ต๋๋ค.
์ด ๋ฌธ์์ด์ ์ซ์๋ก ๋ณํํด๋ณด์ธ์.

๋ฌธ์  3 :
let b = '12' + '21';
b๋ฅผ ์ถ๋ ฅํ๋ฉด ๋ญ๊ฐ ๋์ฌ๊น์?

๋ฌธ์  4 :
let d = "I am" + " "  + 12;
d๋ฅผ ์ถ๋ ฅํ๋ฉด ๋ญ๊ฐ ๋์ฌ๊น์?

````



<details><summary><b>Answer</b></summary>

  <p>

```javascript
๋ฌธ์ 1 :
let c = 13;
c = String(c)
console.log(typeof c);  // string 

๋ฌธ์ 2 : 
let something = "1000";
something = Number(something)
console.log(typeof something);   / number

๋ฌธ์ 3 : 
let b = '12' + '21'; 
console.log(b);    // 1221

๋ฌธ์  4 :
let d = "I am" + " "  + 12;
console.log(d);    // I am 12
````

 </p>
 </details>
 <br>
 <br>

### ๐ Operators

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Operators


 ```javascript


์๋ฐ์คํฌ๋ฆฝํธ์์๋ ๋ค์ํ ์ฐ์ฐ์(Operators)๊ฐ ์ฌ์ฉ๋๊ณ  ์์ต๋๋ค.
๋ผ๋ฆฌ ์ฐ์ฐ์, ๋น๊ต ์ฐ์ฐ์, ๋์ ์ฐ์ฐ์, ๋ถ ์ฐ์ฐ์..



Operators : ์ฐ์ฐ์๋ ๋ณ์๋ ๊ฐ์ ์ฐ์ฐ์ ์ํด ์ฌ์ฉ๋๋ ๋ถํธ๋ฅผ ์นญํฉ๋๋ค.
์์ : 2 + 3 ์์ 2์ 3์ ์ฐ์ฐ์์ํด + ์ฐ์ฐ์๊ฐ ์ฌ์ฉ๋ฉ๋๋ค.

Operands : ํผ์ฐ์ฐ์๋ ์ฐ์ฐ์ ํ์ํ ๊ฐ์ ๋ปํฉ๋๋ค.
์์ : 3 + 5 ์์ + ์ฐ์ฐ์๋ฅผ ์ด์ฉํด ํผ์ฐ์ฐ์์ธ 3๊ณผ 5๋ฅผ ๋ํ์ต๋๋ค.

Unary Operator : ์ฐ์ฐ์๊ฐ 1๊ฐ์ ํผ์ฐ์ฐ์๋ฅผ ๊ฐ์ง๊ณ ์์ผ๋ฉด ์ฐ๋ฆฌ๋ ์ด ์ฐ์ฐ์๋ฅผ Binary Operator๋ผ๊ณ  ๋ถ๋ฆ๋๋ค.
์์ : -1 , ๋นผ๊ธฐ ์ฐ์ฐ์๋ ํผ์ฐ์ฐ์์ธ 1์ ๊ฐ์ง๊ณ  ์์.

Binary Operator : ์ฐ์ฐ์๊ฐ 2๊ฐ์ ํผ์ฐ์ฐ์๋ฅผ ๊ฐ์ง๊ณ ์์ผ๋ฉด ์ฐ๋ฆฌ๋ ์ด ์ฐ์ฐ์๋ฅผ Binary Operator๋ผ๊ณ  ๋ถ๋ฆ๋๋ค.
์์ : 1 + 2 , ๋ํ๊ธฐ ์ฐ์ฐ์๋ ํผ์ฐ์ฐ์์ธ 1๊ณผ 2๋ฅผ ๊ฐ์ง๊ณ  ์์.

Ternary Operator : ์ฐ์ฐ์๊ฐ 3๊ฐ์ ํผ์ฐ์ฐ์๋ฅผ ๊ฐ์ง๊ณ ์์ผ๋ฉด ์ฐ๋ฆฌ๋ ์ด ์ฐ์ฐ์๋ฅผ Ternary Operator๋ผ๊ณ  ๋ถ๋ฆ๋๋ค

์ฐ์  ์์(Priority of Operators) : ํ Expression์ค์ ์ฌ๋ฌ๊ฐ์ ์ฐ์ฐ์๊ฐ ์กด์ฌํ๋ค๋ฉด, ์ด๋๊ฒ์ ๋จผ์  ๊ณ์ฐํด์ผํ ์ง ์๊ฐํด์ผํฉ๋๋ค. ์ด๊ฒ์ ์ฐ๋ฆฌ๋ ์ฐ์ฐ์์ ์ฐ์  ์์๋ผ๊ณ  ํฉ๋๋ค.

````



<details><summary><b>Answer</b></summary>

  <p>

```javascript

````

 </p>
 </details>
 <br>
 <br>
 
 
 ### ๐ Operators Increment Decrement

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ Operators Increment Decrement


 ```javascript
Increment Opertoar : ์ฆ๊ฐ ์ฐ์ฐ์
์์ : a++, ++a, b--, --b 

Remainder : ๋๋จธ์ง
์์ : 100 & 40 = 2 ... 20 ๋๋จธ์ง

Exponentiation : ๊ฑฐ๋ญ์ ๊ณฐ
์์ : 2 ** 3 = 8

๋ฌธ์  1 : 
let a = 5;
let counterA = ++a * 2;
console.log(counterA);
๋ค์์ Increment Operator๊ฐ ๋ณ์ ์ ์ ์์ ๋์ ์ํฉ์๋๋ค. ์ถ๋ ฅ๋  ๊ฐ์ ์์ฑํ์ธ์

๋ฌธ์  2 :
let b = 25;
let counterB = b-- * 2;
console.log(counterB);
๋ค์์ Increment Operator๊ฐ ๋ณ์ ๋ค์ ์์ ๋์ ์ํฉ์๋๋ค. ์ถ๋ ฅ๋  ๊ฐ์ ์์ฑํ์ธ์

๋ฌธ์  2 : 
let c = 25
let counterC = c % 4;
console.log(counterC);
๋ค์์ Remainder(๋๋จธ์ง) & ๋ฅผ ์ถ๋ ฅํ๋ ์ฝ๋์๋๋ค. ์ถ๋ ฅ๋  ๊ฐ์ ์์ฑํ์ธ์ 

๋ฌธ์  3 : 
let d = 5;
let counterD = d ** 2;
console.log(counterD);
๋ค์์ Exponentiation ** (๊ฑฐ๋ญ์ ๊ณฑ)์ ์ฌ์ฉํ๋ ์ฝ๋์๋๋ค. ์ถ๋ ฅ๋  ๊ฐ์ ์์ฑํ์ธ์.

````



<details><summary><b>Answer</b></summary>

  <p>

```javascript
๋ฌธ์  1 : 12
๋ฌธ์  2 : 1
๋ฌธ์  3 : 25
````

 </p>
 </details>
 <br>
 <br>

 ### ๐  Operators Modify in place

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ  Operators Modify in place


 ```javascript

๋ฌธ์  1 : 
=, +, -, *, / 
Operator ๋ค์ ์ฐ์ ์์ ๋ณ๋ก ๋์ด ํ์ธ์.


๋ฌธ์  2 :
a = a + 3; === a += 3; 

์ ์๊ณผ ๊ฐ์ด ์๋ ์๋ค์ ์ค์ฌ๋ณด์ธ์.
a = a * 4;
b = b / 3;
c = c - 2;



๋ฌธ์  3 : 
let d = 7;
d *= 8 + 9;
console.log(d);
์ถ๋ ฅ๋  ๊ฐ์ ์์ฑํ์ธ์ 

````



<details><summary><b>Answer</b></summary>

  <p>

```javascript
๋ฌธ์  1 : * -> / -> + -> - -> = 
๋ฌธ์  2 : a *= 4;, b /= 3;, c -= 2;
๋ฌธ์  3 : 119 

````

 </p>
 </details>
 <br>
 <br>

 ### ๐  Operators Assignment

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ  Operators Assignment


 ```javascript
๋ฌธ์  1 : 

let z = 3 + 4 * 5;
console.log(z);

์ถ๋ ฅ๋  ๊ฐ์ ์์ฑํ์ธ์


๋ฌธ์  2 : 

let a, b, c = 10
console.log(a);
console.log(b);
console.log(c);
์ถ๋ ฅ๋  ๊ฐ์ ์์ฑํ์ธ์


๋ฌธ์  3 :

let d, e, f;

d = e = f = 10;

console.log(d);
console.log(e);
console.log(4 + ( f = e - 3));

์ถ๋ ฅ๋  ๊ฐ์ ์์ฑํ์ธ์ 


````



<details><summary><b>Answer</b></summary>

  <p>

```javascript
๋ฌธ์  1 : 23
๋ฌธ์  2 : 
console.log(a);   // undefined  
console.log(b);   // undefined
console.log(c);   // 10 
๋ฌธ์  3 :
console.log(d); // 10 
console.log(e); // 10
console.log(4 + ( f = e - 3));  // 11


````

 </p>
 </details>
 <br>
 <br>


### ๐  Operators Assignment

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ  Operators Assignment


 ```javascript
๋ฌธ์  1 : 

A. console.log('a' > 2)
B. console.log('2' > 1)
C. console.log('A' > 'a')
D. console.log(0 == false)
E. console.log(1 > 2
F. console.log(true == 1)
G. console.log(0 == 'a')
H. console.log('abc' > 'acb')

๊ฒฐ๊ณผ๋ ๋์ค์ง๋ง ์ง์ํด์ผํ  ์๊ณผ ์๋์์ ๋ถ๋ฅํ๊ณ  ํ๋ฉด์ ์ถ๋ ฅํ๋ ๊ฐ์ ์ ์ผ์ธ์.

````



<details><summary><b>Answer</b></summary>

  <p>

```javascript

A. console.log('a' > 2)   //   ์ง์ํด์ผ,   false
B. console.log('2' > 1)   //   ์ง์ํด์ผ,   true
C. console.log('A' > 'a')  //   ์ง์ํด์ผ,   false (์๋ฌธ์๊ฐ ํญ์ ๋๋ฌธ์๋ณด๋ค ์ฐ์ ์์์)
D. console.log(0 == false)  //   true 
E. console.log(1 > 2)   //   false
F. console.log(true == 1)  //  true 
G. console.log(0 == 'a')   //   false,   string์ false๊ฐ ์๋
H. console.log('abc' > 'acb')  //   false


````

 </p>
 </details>
 <br>
 <br>
 
 
 ### ๐ Interaction, Conditional operators "if"

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ  Interaction, Conditional operators "if"


 ```javascript
 
 ๋ฌธ์  1 : 

์ค๋ฅธ์ชฝ์ ๋ํ๋ ๊ทธ๋ฆผ์ฒ๋ผ
Harry Potter๋ผ๊ณ  ์๋ ฅํ์ ์ 
"ํด๋ฆฌํฌํฐ๋ ํ์ํฉ๋๋ค"
์๋์
"ํด๋ฆฌํฌํฐ๊ฐ ์๋๋๋ค"
๋ผ๊ณ  ์ถ๋ ฅ๋  ์ ์๋๋ก ์ฝ๋๋ฅผ ์ง๋ณด์ธ์.
````
![์บก์ฒ](https://user-images.githubusercontent.com/80245801/116802754-61b64280-ab50-11eb-876a-6e85e6759336.PNG)


<details><summary><b>Answer</b></summary>

  <p>

```javascript

let name = prompt('Please enter your name', 'Harry Potter');
if (name === 'Harry Potter') {
alert("ํด๋ฆฌํฌํฐ๋ ํ์ํฉ๋๋ค"); 
} else {
alert("ํด๋ฆฌํฌํฐ๊ฐ ์๋๋๋ค");
}; 

````

 </p>
 </details>
 <br>
 <br>

### ๐ Conditional operators "?"

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ  Conditional operators "?"


 ```javascript
 
 ๋ฌธ์  1 : 

let i = 1, j = 2;

let whoisbig = ( i > j )? i : j

console.log(whoisbig);

์ถ๋ ฅ๊ฐ์ ์ ์ผ์ธ์.

````



<details><summary><b>Answer</b></summary>

  <p>

```javascript

Answer : 2

````

 </p>
 </details>
 <br>
 <br>
 
 ### ๐ Logical operators

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ  Logical operators


 ```javascript
 
 0, null, undefined == false 
 1, 2, .... == true.
 
 &&๋ก ์ฐ๊ฒฐ๋๋ฉด, ์ต์ด์ False๊ฐ์ returnํ๊ฑฐ๋, ํน์ false๊ฐ ์์ผ๋ฉด ์ ์ผ ๋ง์ง๋ง ๊ฐ return.
 
 ||์ ์ต์ด์ true๊ฐ์ returnํ๊ฑฐ๋, ์์ผ๋ฉด, ์ ์ผ ๋ง์ง๋ง false๊ฐ์ return.
 
 &&์ Priority๊ฐ ||๋ณด๋ค ๋๋ค. ๋ฐ๋ผ์ and ๋ถํฐ ๋จผ์  ํ๊ณ  ๊ทธ ๋ค์์ or์ ํ๊ฒ ๋๋ค.
 
 ๋ฌธ์  1 : 

console.log(1 || 2 && 3);
console.log(1 || 0 && 3 || 0);
console.log(undefined || 2 && 3 || null);
console.log(3 || 2 && 0);
console.log(undefined || 2 && 3 && null);

์ถ๋ ฅ๊ฐ์ ์ ์ผ์ธ์.


````



<details><summary><b>Answer</b></summary>

  <p>

```javascript
console.log(1 || 2 && 3);     //    1
console.log(1 || 0 && 3 || 0);     //    1
console.log(undefined || 2 && 3 || null);    //    3
console.log(3 || 2 && 0);    //    3
console.log(undefined || 2 && 3 && null);    //     null 


````

 </p>
 </details>
 <br>
 <br>


### ๐  Loops while and for

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ  Loops while and for


 ```javascript
 
 while (boolean expression == true or false => true์ผ ๊ฒฝ์ฐ ์คํ, false์ผ ๊ฒฝ์ฐ ์คํx) {
      }
      Boolean Expression => true๋ฅผ ์ธ ๋ ์ฃผ์ํด์ผ(๋์์ด, ๋ฌดํํ ๋ฐ๋ณต๋์ computer down.). true ๊ฐ์ด ์ฃผ์ด์ง ์ ์๋ ์กฐ๊ฑด์์ ์ฃผ์ด์ ๊ทธ ์กฐ๊ฑด์์ ๋ง์กฑํ  ๋ ๊น์ง๋ง ๋์๊ฐ๋๋ก ํด์ผํจ.
      while (true) {
        console.log(1)
      }
      while (false) {
        console.log(1)
      }
      
     
for loop => for ๋ฌธ์ฅ๊ณผ while ๋ฌธ์ฅ์ ๊ธฐ๋ณธ์ ์ผ๋ก ๋์ผํ ๊ฒ์ด๋ค. ๋ฌธ์ฅ ๊ตฌ์กฐ๋ง ๋ค๋ฅธ ๊ฒ.
      
 
๋ฌธ์  1 : 

a formula which return true or false๋?

๋ฌธ์  2 : 

0๋ถํด 100๊น์ง 1์ฉ ์ฆ๊ฐํ๋ ์ฝ๋๋ฅผ while์ ์จ์ ์์ฑํ์ธ์.

๋ฌธ์  3 :

100๋ถํฐ 1๊น์ง 1์ฉ ๊ฐ์ํ๋ ์ฝ๋๋ฅผ for์ ์จ์ ์์ฑํ์ธ์.

````



<details><summary><b>Answer</b></summary>

  <p>

```javascript

๋ฌธ์  1 :
Boolean Expression

๋ฌธ์  2 :

let i = 1;
while (i =< 100) {
console.log(i);
i++;
}

๋ฌธ์  3 :

for (let i = 100; i >= 1; i--) {
   console.log(i); 
}

````

 </p>
 </details>
 <br>
 <br>


### ๐  continue and break

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ  continue and break

 ```javascript
 

๋ฌธ์  1 : 

for (let i = 0; i < 10; i ++) {
  if(i % 2) continue;
  console.log(i);
}

์ถ๋ ฅ๊ฐ์ ์์ฑํ์ธ์.

๋ฌธ์  2 : 

for (let i = 0; i < 10; i++) {
  if (i % 2 == 0) break;
  console.log(i);
}

console.log("I am kicked out!!");

์ถ๋ ฅ๊ฐ์ ์์ฑํ์ธ์.


๋ฌธ์  3 :

for (let i = 0; i < 10; i++) {
  if (i % 2) break;
  console.log(i);
}

console.log("I am kicked out again!!");

์ถ๋ ฅ๊ฐ์ ์์ฑํ์ธ์.

 


````



<details><summary><b>Answer</b></summary>

  <p>

```javascript

๋ฌธ์  1 :  0, 2, 4, 6, 8


๋ฌธ์  2 :  I am kicked out!!


๋ฌธ์  3 : 0, I am kicked out again!!


````

 </p>
 </details>
 <br>
 <br>


๋ฌธ์  ์ถ์ฒ : https://docs.google.com/spreadsheets/d/1YNPM8tD0EcR0RwBnRyWL0DsgVXfax4QvDeoYsRS1ILA/edit#gid=141000431


