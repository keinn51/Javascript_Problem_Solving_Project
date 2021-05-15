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
