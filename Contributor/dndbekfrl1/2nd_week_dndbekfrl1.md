# dndbekfrl1's Problems

### 🎁 Basic

<br>

### 난이도 : 🌶

<br>

#### ☁︎ var과 let

```javascript
다음 출력값은 무엇일까요?

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

### 🎁 Basic

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 비교연산자

```javascript
다음 출력값은 무엇일까요?

문자열 비교
console.log('Z'>'A');
console.log('Hello'<'Bye');

다른 형 비교
console.log('2'>1);
```

<details><summary><b>Answer</b></summary>

<p>

```javascript
>true //'Z'가 'Z'보다 크다.
>false //'H'가 'B'보다 크다.
>true // '2'는 숫자 2로 변환 후 비교 된다.

```

 </p>
 </details>
 <br>
 <br>

### 🎁 Basic

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 일치 연산자

```javascript
다음 출력값은 무엇일까요?
console.log(null==undefined);
console.log(null===undefined);
console.log(null==0);
console.log(undefined ==0);

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
>true //null과 undefined는 숫자형으로 변환되어 각각 0, NaN으로 변환
>false
>true
>false //NaN이 피연산자이면 비교 연산자는 항상 false 반환

```

 </p>
 </details>
 <br>
 <br>

### 🎁 Basic

<br>

### 난이도 : 🌶🌶

<br>

#### ☁︎ 1000단위 읽기

```javascript
숫자 1234567를 1,234,567로 출력하는 코드를 작성하세요.
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

또는, num.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
```

 </p>
 </details>
 <br>
 <br>

### 🎁 Basic

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 조건부 연산자 '?'

```javascript
prompt를 통해 age를 입력받고,
18세 이상이면 접근을 허용하는 코드를 작성하세요.
(단, 조건부 연산자 '?'를 사용할 것)

let aceessAllowed;
let age = propmt('나이를 입력해 주세요.','');

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
let aceessAllowed;
let age = propmt("나이를 입력해 주세요.", "");

accessAllowed = age >= 18 ? true : false;
if (accessAllowed) {
  console.log("접근을 허용합니다.");
} else {
  console.log("접근을 거부합니다.");
}
```

 </p>
 </details>
 <br>
 <br>

### 🎁 Array

<br>

### 난이도 : 🌶

<br>

#### ☁︎ set

```javascript
다음 배열에서 중복 요소를 제거하세요.
let arr =['🍎', '🍎', '🍋', '🍌', '🍋', '🍇'];
```

<details><summary><b>Answer</b></summary>

<p>

```javascript
let arr = ["🍎", "🍎", "🍋", "🍌", "🍋", "🍇"];
arr = new Set(arr);
```

 </p>
 </details>
 <br>
 <br>
