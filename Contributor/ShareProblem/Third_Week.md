# 3rd Week Problem Sharing

## Keinn51

### 🎁 Array

<br>

### 난이도 : 🌶🌶

<br>

#### ☁︎ 마라톤 미완주 선수 찾기

```javascript
꼭 사이트에 들어가셔서 먼저 풀어보시고 코드 채점 받아보세요!

https://programmers.co.kr/learn/courses/30/parts/12077"

수많은 마라톤 선수들이 마라톤에 참여하였습니다. 단 한 명의 선수를 제외하고는 모든 선수가 마라톤을 완주하였습니다.

마라톤에 참여한 선수들의 이름이 담긴 배열 participant와 완주한 선수들의 이름이 담긴 배열 completion이 주어질 때,
완주하지 못한 선수의 이름을 return 하도록 solution 함수를 작성해주세요.

// 제한사항

마라톤 경기에 참여한 선수의 수는 1명 이상 100,000명 이하입니다.
completion의 길이는 participant의 길이보다 1 작습니다.
참가자의 이름은 1개 이상 20개 이하의 알파벳 소문자로 이루어져 있습니다.
참가자 중에는 동명이인이 있을 수 있습니다.

// 입출력 예

<1>
participant: ["leo", "kiki", "eden"] completion : ["eden", "kiki"] return : "leo"

<2>
participant: ["marina", "josipa", "nikola", "vinko", "filipa"] completion : ["josipa", "filipa", "marina", "nikola"] return : "vinko"

<3>
participant: ["mislav", "stanko", "mislav", "ana"] completion : ["stanko", "ana", "mislav"] return : "mislav"

// 입출력 예 설명

예제 #1
"leo"는 참여자 명단에는 있지만, 완주자 명단에는 없기 때문에 완주하지 못했습니다.

예제 #2
"vinko"는 참여자 명단에는 있지만, 완주자 명단에는 없기 때문에 완주하지 못했습니다.

예제 #3
"mislav"는 참여자 명단에는 두 명이 있지만, 완주자 명단에는 한 명밖에 없기 때문에 한명은 완주하지 못했습니다.
```

<details><summary><b>Answer</b></summary>
  <p>

##### 📌 array의 method인 filter나 find를 사용, 답은 맞지만 비효율적인 코드.

```javascript
function solution(participant, completion) {
  var answer = "";

  for (let i = 0; i < participant.length; i++) {
    if (
      // 동명이인이 없는 경우
      !(
        typeof completion.find((element) => element == participant[i]) ==
        "string"
      )
    ) {
      answer = participant[i];
      return answer;
    }

    if (
      // 동명이인의 경우
      participant.filter((element) => element == participant[i]).length == 2
    ) {
      answer = participant[i];
      return answer;
    }
  }
}
```

그러나 위의 식은 반복문을 세 번이나 쓰기 때문에 비효율적인 코딩입니다.  
반복문을 최대한 줄여 시간 효율적인 코드를 구성해야 하므로 다른 방법을 생각해봅니다.

<br>

##### 📌 sort를 사용하는 방법

```javascript
function solution(participant, completion) {
  var answer;

  participant.sort();
  completion.sort();

  for (let i = 0; i < participant.length; i++) {
    if (participant[i] != completion[i]) {
      answer = participant[i];
      return answer;
    }
  }
}
```

반복문을 한 번만 사용해 시간을 절약할 수 있습니다.

<br>

##### 📌 프로그래머스 1티어 풀이

```javascript
let solution = (participant, completion) =>
  participant.find(
    (name) => !completion[name]--,
    completion.map((name) => (completion[name] = (completion[name] | 0) + 1))
  );

// map : 배열의 각 요소에 함수를 적용하고, 그 결과를 모아 배열로 반환.
// find : 조건에 맞는 첫 번째 요소를 반환.
```

array도 object이기 때문에, key-value로 이루어진 쌍을 받을 수 있습니다.  
(completion[name] | 0) + 1 에서 name이라는 key를 가진 요소가 completion에 있다면 그 value에 1을 더해줍니다.

value값이 없었다면 0 + 1 을 통해 value값이 1이 됩니다.
그 결과의 예를 들면 ['cake', 'ball', 'sauce', 'cake', cake: 2, ball: 1, sauce: 1] 이런 식입니다.

<br>

map이 끝났다면 find로 이어지는데, completion의 요소 중 false가 되는 값을 찾으면 그 값에 !을 붙여 true로 만들어줍니다.  
그렇다면 completion요소 중에서 false가 나오는 값이 최종 답이 될 것입니다.  
우리는 평소 false로 칭해지는 값들은 (false, 0, -0, NaN, null, undefined, '')라고 알고 있습니다.

find(name => 여기에서 부르는 name은 participant 요소들의 name 입니다.

여기서부터는 예를 들어서 설명해봅니다.

<br>

> 동명이인이 없는 경우

participant : ['cake', 'ball', 'sauce', 'carrot']  
completion : ['cake', 'ball', 'sauce']  
인 경우

- participant의 name으로 completion의 key값을 부르는 것인데, carrot은 participant에만 있고 completion에는 없는 값이라서 undefined가 반환됩니다.

> 동명이인이 있는 경우

participant : ['cake', 'ball', 'sauce', 'cake']  
completion : ['cake', 'ball', 'sauce']  
인 경우

- cake의 value가 이전에 이미 1-- 을 통해 0이 되었으므로, cake을 다시 불러줬을 때 그 값은 0이어서 false가 됩니다.

 </p>
 </details>
 <br>
 <br>

#### ☁︎ 배열의 정렬

```javascript
부분에 배열 내장함수를 이용하여 코드를 입력하고 다음과 같이 출력되게 하세요.

// 문제 설명

배열 array의 i번째 숫자부터 j번째 숫자까지 자르고 정렬했을 때, k번째에 있는 수를 구하려 합니다.

예를 들어 array가 [1, 5, 2, 6, 3, 7, 4], i = 2, j = 5, k = 3이라면
array의 2번째부터 5번째까지 자르면 [5, 2, 6, 3]입니다.
1에서 나온 배열을 정렬하면 [2, 3, 5, 6]입니다.
2에서 나온 배열의 3번째 숫자는 5입니다.

배열 array, [i, j, k]를 원소로 가진 2차원 배열 commands가 매개변수로 주어질 때,
commands의 모든 원소에 대해 앞서 설명한 연산을 적용했을 때 나온 결과를 배열에 담아 return 하도록 solution 함수를 작성해주세요.

// 제한사항

array의 길이는 1 이상 100 이하입니다.
array의 각 원소는 1 이상 100 이하입니다.
commands의 길이는 1 이상 50 이하입니다.
commands의 각 원소는 길이가 3입니다.

// 입출력 예

array: [1, 5, 2, 6, 3, 7, 4] commands: [[2, 5, 3], [4, 4, 1], [1, 7, 3]] return:  [5, 6, 3]

// 입출력 예 설명

[1, 5, 2, 6, 3, 7, 4]를 2번째부터 5번째까지 자른 후 정렬합니다. [2, 3, 5, 6]의 세 번째 숫자는 5입니다.

[1, 5, 2, 6, 3, 7, 4]를 4번째부터 4번째까지 자른 후 정렬합니다. [6]의 첫 번째 숫자는 6입니다.

[1, 5, 2, 6, 3, 7, 4]를 1번째부터 7번째까지 자릅니다. [1, 2, 3, 4, 5, 6, 7]의 세 번째 숫자는 3입니다.
```

 <details><summary><b>Answer</b></summary>

   <p>

##### 📌 가장 간결한 풀이

```javascript
function solution(array, commands) {
  var answer = [];
  for (let a of commands) {
    answer.push(array.slice(a[0] - 1, a[1]).sort((a, b) => a - b)[a[2] - 1]);
  }
  return answer;
}
```

array를 slice로 베껴 sort로 정렬시킵니다.  
숫자 관련 sort를 핧 시에는 무조건 sort안에 (a, b) => a - b 를 넣어주는 것이 좋습니다.

넣어주지 않는다면 유니코드 해석 순서상 80이 9보다 먼저 오는 특이한 상황이 발생합니다.  
참고 : <a href="https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Array/sort">MDN</a>

<br>

##### 📌 새로운 개념 풀이

```javascript
function solution(array, commands) {
  return commands.map((command) => {
    const [sPosition, ePosition, position] = command;
    const newArray = array
      .filter(
        (value, fIndex) => fIndex >= sPosition - 1 && fIndex <= ePosition - 1
      )
      .sort((a, b) => a - b);

    return newArray[position - 1];
  });
}
```

제가 푼 건 아니지만 신기학게 풀어서 가져와 봤습니다.  
const [sPosition, ePosition, position] = command 어떻게 이런 생각을...  
함수에서 filter요소를 다루는 것도 색달랐습니다~

  </p>
  </details>
  <br>
  <br>

# dndbekfrl1's Problems

### 🎁 Basic

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

 </p>
 </details>
 <br>
 <br>

# SoozingKIM's Problems


### 🎁 Basic

 <br>

### 난이도 : 🌶

 <br>

#### ☁︎ const 상수 (대문자상수)

```javascript
아래 코드를 평가해 보시기 바랍니다.

const birthday = '18.04.1982';
const age = someCode(birthday);

위 코드의 상수 birthday는 태어난 날짜 정보를 담고 있습니다.
age라는 상수는 나이에 관한 값을 담고 있는데 birthday를 조작하여 그 값을 도출합니다.
(생일을 이용하여 나이를 도출하는 코드는 간결성을 위해 여기선 언급하지 않겠습니다. 이 문제에서 해당 코드가 중요한 역할을 하지 않기도 합니다)
이런 상황에서 birthday를 대문자 상수로 바꾸는 것이 적절할까요?
age 역시 대문자 상수로 바꾸는 것이 괜찮은 선택일까요?
```

 <details><summary><b>Answer</b></summary>
 <p>
  
 ```javascript
 BIRTHDAY는 괜찮지만, age는 소문자가 좋다.
 태어난 날짜는 변하지 않지만 나이는 매년 변하기 때문!
 ```
 </p>
 </details>
 <br>
 <br>

### 🎁 Basic

 <br>

### 난이도 : 🌶🌶

 <br>

#### ☁︎ 연산자

```javascript
아래 표현식의 결과를 예측해 보세요.
1)  "" + 1 + 0
2)  "" - 1 + 0
3) true + false
4)  6 / "3"
5)  "2" * "3"
6)  4 + 5 + "px"
7)  "$" + 4 + 5
8)  "4" - 2
9)  "4px" - 2
10) 7 / 0
11) "  -9  " + 5
12) "  -9  " - 5
13) null + 1
14) undefined + 1
15) " \t \n" - 2
```

 <details><summary><b>Answer</b></summary>
 <p>

```javascript
1)  10      ""은 빈 문자열로 취급되고, 문자열 + 숫자가 되면 숫자는 문자 취급을 받는다.
2)  -1      ""은 문자열인데 숫자 0으로 변황된다.
3)  1       참:1 / 거짓:0
4)  2       +를 제외한 산술 연산자는 피연산자가 숫자형이 아닌경우 숫자형으로 바꿈.
5)  6       +를 제외한 산술 연산자는 피연산자가 숫자형이 아닌경우 숫자형으로 바꿈.
6)  9px     문자열 더하기
7)  $45     문자열 더하기
8)  2       +를 제외한 산술 연산자는 피연산자가 숫자형이 아닌경우 숫자형으로 바꿈.
9)  NaN     "4px"을 숫자로 변환할 수 없기 때문에 NaN.
10) Infinty 산술 연산
11)  -9 5   문자열 더하기
12) -14     문자열이 숫자형으로 변하면 앞뒤 공백이 삭제된다.
13) 1       null은 숫자형 변환시 0.
14) NaN     undefined는 숫자형 변환시 NaN.
15) -2      문자열이 숫자형으로 변하면 앞뒤 공백이 삭제되는데, 공백만드는 문자열이 삭제되어 ""로 인식되고 이것이 0으로 인식된다.
```

 </p>
 </details>
 <br>
 <br>

