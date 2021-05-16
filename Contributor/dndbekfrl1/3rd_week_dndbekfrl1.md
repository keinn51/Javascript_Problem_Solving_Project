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

//다른사람 풀이
function solution(s) {
  return s.length == 4 || s.length == 6 ? !isNaN(s) : false;
}


isNaN()은 매개변수가 숫자인지 검사하는 함수입니다.
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

### 🎁 Basic

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 일치 연산자

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

//다른사람 풀이
function solution(arr) {
  return arr.filter((val, index) => val != arr[index + 1]);
}

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
