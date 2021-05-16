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

isNaN()은 매개변수가 숫자인지 검사하는 함수입니다.
Number()과 parseInt()도 써보았는데, 개인적으로 isNaN()이 제일 코드짜기 쉬웠습니다!

//다른사람 풀이
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
//다른사람 풀이
function solution(x) {
  return ((a + b) * (Math.abs(b - a) + 1)) / 2;
}

//출처 https://programmers.co.kr/learn/courses/30/lessons/12912
```

 </p>
 </details>
 <br>
 <br>

### 🎁 Array

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 같은 숫자는 싫어

```javascript
배열 arr의 각 원소는 숫자 0부터 9까지로 이루어져 있습니다. 이때, 배열 arr에서 연속적으로 나타나는 숫자는 하나만 남기고 전부 제거하려고 합니다. 단, 배열 arr의 원소들의 순서를 유지해야 합니다.
(예 arr = [1, 1, 3, 3, 0, 1, 1] 이면 [1, 3, 0, 1] 을 return 합니다. arr = [4, 4, 4, 3, 3] 이면 [4, 3] 을 return 합니다.)

function solution(arr){

}

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//작성한 답
function solution(arr) {
  var result = [];
  result.push(arr[0]);
  len_result = 0;
  var length = arr.length;

  if (length > 0) {
    for (var i = 1; i < length; i++) {
      if (result[len_result] != arr[i]) {
        len_result += 1;
        result.push(arr[i]);
      }
    }
  }

  return result;
}

배열 result과 arr를 비교하면서 연속되지 않은 값을 result에 push해 주었습니다.

//다른사람 풀이
function solution(arr) {
  return arr.filter((val, index) => val != arr[index + 1]);
}
filter를 쓰면 간단하게 구현할 수 있었습니다..!

function solution(arr) {
  var answer = [arr[0]];

  for (let i = 1; i < arr.length; i++) {
    if (answer[answer.length - 1] !== arr[i]) {
      answer.push(arr[i]);
    }
  }

  return answer;
}

//출처 https://programmers.co.kr/learn/courses/30/lessons/12906
```

### 🎁 Function

<br>

### 난이도 : 🌶🌶

<br>

#### ☁︎ 화살표 함수

```javascript
다음 함수를 화살표 함수로 변경해보세요.

function ask(question, yes, no){
  if(confirm(question)) yes();
  else no();
}

ask(
  "동의하십니까?",
  function(){alert("동의하셨습니다.");},
  function(){alert("취소 버튼을 누르셨습니다.");}
);

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
ask(
  "동의하십니까?",
  ()=>alert("동의하셨습니다.");,
  ()=>alert("취소 버튼을 누르셨습니다."); )


좀 더 간결한 문법으로 표현할 수 있는 화살표 함수에 대해 학습했습니다.
화살표 함수의 구조는 '()'에서 인자를 받고, '=>'우측의 결과를 반환합니다.
map(), setInterval()과 같은 함수에서 많이 사용됩니다.
```

### 🎁 Function

<br>

### 난이도 : 🌶🌶

<br>

#### ☁︎ 화살표 함수2

```javascript
다음 함수를 화살표 함수로 변경해보세요.

function Person() {
  this.age = 0;

  setInterval(function growUp() {
    this.age++;
  }, 1000);
}

var p = new Person();

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
function Person() {
  this.age = 0;

  setInterval(() => {
    this.age++;
  }, 1000);
}
```

### 🎁 Function

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 재귀함수

```javascript
재귀함수로 주어진 n번째 피보나치 수를 계산하는 함수를 구현하세요.

function fibo(n){

}

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
function fibo(n) {
  if (n <= 1) {
    return n;
  }
  return fibo(n - 1) + fibo(n - 2);
}
```
