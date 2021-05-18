### 🎁 Array

<br>

#### 진아님 공유문제입니다.

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
// 📌 작성한 답
function solution(arr) {
  let answer = [arr[0]];

  arr.forEach(element => {
    (!(answer[answer.length - 1] == element)) ? answer.push(element) : ''
  });

  return answer
}

배열 result과 arr를 비교하면서 연속되지 않은 값을 result에 push해 주었습니다.

// 📌 프로그래머스 1티어 풀이

function solution(arr)
{
    return arr.filter((val,index) => val != arr[index+1]);
}

//출처 https://programmers.co.kr/learn/courses/30/lessons/12906
```

 </p>
 </details>
 <br>
 <br>

### 🎁 Basic

<br>

#### 진아님 공유문제입니다.

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 문자열 다루기

```javascript
문자열 s의 길이가 4 또는 6이고, 숫자로만 구성되어있는지 확인하는 solution 함수를 작성하세요.
(예: 1234는 true이고, a234는 false를 반환합니다.)

function solution(s){

}

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
function solution(s) {
  return s.length == 4 || s.length == 6 ? !isNaN(s) : false;
}

//출처 https://programmers.co.kr/learn/courses/30/lessons/12918
```

 </p>
 </details>
 <br>
 <br>

### 🎁 If_and_switch

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 'if'를 '?'로 교체하기

```javascript
조건부 연산자 '?'를 이용해 if문이 사용된 아래 코드를 변형해보세요. 동작 결과는 동일해야 합니다.

let result;

let a = 1, b = 5;

if (a + b < 4) {
  result = '미만';
} else {
  result = '이상';
}
```

 <details><summary><b>Answer</b></summary>

   <p>

```javascript
let result;

let a = 1,
  b = 5;

result = a + b < 4 ? "미만" : "이상";
```

  </p>
  </details>
  <br>
  <br>

#### ☁︎ 'if..else'를 '?'로 교체하기

```javascript
조건부 연산자 '?'를 사용해 if..else문이 사용된 아래 코드를 변형해보세요. 동작 결과는 동일해야 합니다.

가독성을 위해 표현식을 여러 줄로 분할해 작성해 보시길 바랍니다.

let message;

let login = prompt('Enter Your position: ');

if (login == '직원') {
  message = '안녕하세요.';
} else if (login == '임원') {
  message = '환영합니다.';
} else if (login == '') {
  message = '로그인이 필요합니다.';
} else {
  message = '';
}
```

 <details><summary><b>Answer</b></summary>

   <p>

```javascript
let message;

let login = prompt("Enter Your position: ");

message =
  login == "직원"
    ? "안녕하세요."
    : login == "임원"
    ? "환영합니다."
    : login == ""
    ? "로그인이 필요합니다."
    : "";

alert(message);
```

  </p>
  </details>
  <br>
  <br>
