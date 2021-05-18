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
