# dndbekfrl1's Problems

### ๐ Basic

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ var๊ณผ let

```javascript
๋ค์ ์ถ๋ ฅ๊ฐ์ ๋ฌด์์ผ๊น์?

let x = 3;
var y = 5;

if (x === 3) {
  let x = 2;
  var y =3;

  console.log(x);
}

console.log(x);
console.log(y);
```

<details><summary><b>Answer</b></summary>

<p>

```javascript
>2
>3
>3
```

 </p>
 </details>
 <br>
 <br>

### ๐ Basic

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ ๋น๊ต์ฐ์ฐ์

```javascript
๋ค์ ์ถ๋ ฅ๊ฐ์ ๋ฌด์์ผ๊น์?

๋ฌธ์์ด ๋น๊ต
console.log('Z'>'A');
console.log('Hello'<'Bye');

๋ค๋ฅธ ํ ๋น๊ต
console.log('2'>1);
```

<details><summary><b>Answer</b></summary>

<p>

```javascript
>true //'Z'๊ฐ 'Z'๋ณด๋ค ํฌ๋ค.
>false //'H'๊ฐ 'B'๋ณด๋ค ํฌ๋ค.
>true // '2'๋ ์ซ์ 2๋ก ๋ณํ ํ ๋น๊ต ๋๋ค.

```

 </p>
 </details>
 <br>
 <br>

### ๐ Basic

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ ์ผ์น ์ฐ์ฐ์

```javascript
๋ค์ ์ถ๋ ฅ๊ฐ์ ๋ฌด์์ผ๊น์?
console.log(null==undefined);
console.log(null===undefined);
console.log(null==0);
console.log(undefined ==0);

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
>true //null๊ณผ undefined๋ ์ซ์ํ์ผ๋ก ๋ณํ๋์ด ๊ฐ๊ฐ 0, NaN์ผ๋ก ๋ณํ
>false
>true
>false //NaN์ด ํผ์ฐ์ฐ์์ด๋ฉด ๋น๊ต ์ฐ์ฐ์๋ ํญ์ false ๋ฐํ

```

 </p>
 </details>
 <br>
 <br>

### ๐ Basic

<br>

### ๋์ด๋ : ๐ถ๐ถ

<br>

#### โ๏ธ 1000๋จ์ ์ฝ๊ธฐ

```javascript
์ซ์ 1234567๋ฅผ 1,234,567๋ก ์ถ๋ ฅํ๋ ์ฝ๋๋ฅผ ์์ฑํ์ธ์.
```

<details><summary><b>Answer</b></summary>

<p>

```javascript
var num = 1234567;
num = 1234567 + "";

var point = num.length % 3;
var len = num.length;
var res = num.subString(0, point);

while (point < len) {
  if (res != "") str += ",";
  str += num.subString(point, point + 3);
  point += 3;
}
console.log(res);

๋๋, num.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
```

 </p>
 </details>
 <br>
 <br>

### ๐ Basic

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ ์กฐ๊ฑด๋ถ ์ฐ์ฐ์ '?'

```javascript
prompt๋ฅผ ํตํด age๋ฅผ ์๋ ฅ๋ฐ๊ณ ,
18์ธ ์ด์์ด๋ฉด ์ ๊ทผ์ ํ์ฉํ๋ ์ฝ๋๋ฅผ ์์ฑํ์ธ์.
(๋จ, ์กฐ๊ฑด๋ถ ์ฐ์ฐ์ '?'๋ฅผ ์ฌ์ฉํ  ๊ฒ)

let aceessAllowed;
let age = propmt('๋์ด๋ฅผ ์๋ ฅํด ์ฃผ์ธ์.','');

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
let aceessAllowed;
let age = propmt("๋์ด๋ฅผ ์๋ ฅํด ์ฃผ์ธ์.", "");

accessAllowed = age >= 18 ? true : false;
if (accessAllowed) {
  console.log("์ ๊ทผ์ ํ์ฉํฉ๋๋ค.");
} else {
  console.log("์ ๊ทผ์ ๊ฑฐ๋ถํฉ๋๋ค.");
}
```

 </p>
 </details>
 <br>
 <br>

### ๐ Array

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ set

```javascript
๋ค์ ๋ฐฐ์ด์์ ์ค๋ณต ์์๋ฅผ ์ ๊ฑฐํ์ธ์.
let arr =['๐', '๐', '๐', '๐', '๐', '๐'];
```

<details><summary><b>Answer</b></summary>

<p>

```javascript
let arr = ["๐", "๐", "๐", "๐", "๐", "๐"];
arr = new Set(arr);
```

 </p>
 </details>
 <br>
 <br>
