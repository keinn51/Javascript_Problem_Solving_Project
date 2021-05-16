# dndbekfrl1's Problems

### 🎁 Basic

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 문자열 다루기

```javascript
문자열 s의 길이가 4 또는 6이고, 숫자로만 구성되어있는지 확인하는 solution 함수를 작성하세요.
(예: 1234는 True이고, a234는 False를 반환합니다.)

function solution(s){

}

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//작성한 답
function solution(s) {
  var result = false;
  var length = s.length;
  if (length == 4 || length == 6) {
    result = true;
    var tmp = s.split("");
    tmp.forEach((item) => {
      if (isNaN(item)) {
        result = false;
      }
    });
  }
  return result;
}

//best 답
function solution(s) {
  return s.length == 4 || s.length == 6 ? !isNaN(s) : false;
}

//출처 https://programmers.co.kr/learn/courses/30/lessons/12918
```

 </p>
 </details>
 <br>
 <br>

### 🎁 Basic

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 두 정수 사이의 합

```javascript
두 정수 a, b 사이에 속한 모든 정수의 합을 리턴하는 solution을 작성하세요.
function solution(a,b){

}
```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//작성한 답
function solution(a, b) {
  var result = 0;
  var start = 0;
  var finish = 0;
  if (a > b) {
    start = b;
    finish = a;
  } else {
    start = a;
    finish = b;
  }

  for (var i = start; i <= finish; i++) {
    result += i;
  }
  return result;
}
//best 답
function solution(x) {
  return ((a + b) * (Math.abs(b - a) + 1)) / 2;
}

//출처 https://programmers.co.kr/learn/courses/30/lessons/12912
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
