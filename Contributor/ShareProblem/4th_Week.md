## Keinn51

### 🎁 If_and_switch

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 'if..else'를 '?'로 교체하기

```javascript
조건부 연산자 '?'를 사용해 if..else문이 사용된 아래 코드를 변형해보세요. 동작 결과는 동일해야 합니다.

가독성을 위해 표현식을 여러 줄로 분할해 작성해 보시길 바랍니다!

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

### 🎁 Array

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 폰켓몬

```javascript
// 문제 설명

당신은 폰켓몬을 잡기 위한 오랜 여행 끝에, 홍 박사님의 연구실에 도착했습니다. 홍 박사님은 당신에게 자신의 연구실에 있는 총 N 마리의 폰켓몬 중에서 N/2마리를 가져가도 좋다고 했습니다.
홍 박사님 연구실의 폰켓몬은 종류에 따라 번호를 붙여 구분합니다. 따라서 같은 종류의 폰켓몬은 같은 번호를 가지고 있습니다. 예를 들어 연구실에 총 4마리의 폰켓몬이 있고, 각 폰켓몬의 종류 번호가 [3번, 1번, 2번, 3번]이라면 이는 3번 폰켓몬 두 마리, 1번 폰켓몬 한 마리, 2번 폰켓몬 한 마리가 있음을 나타냅니다. 이때, 4마리의 폰켓몬 중 2마리를 고르는 방법은 다음과 같이 6가지가 있습니다.

첫 번째(3번), 두 번째(1번) 폰켓몬을 선택
첫 번째(3번), 세 번째(2번) 폰켓몬을 선택
첫 번째(3번), 네 번째(3번) 폰켓몬을 선택
두 번째(1번), 세 번째(2번) 폰켓몬을 선택
두 번째(1번), 네 번째(3번) 폰켓몬을 선택
세 번째(2번), 네 번째(3번) 폰켓몬을 선택

이때, 첫 번째(3번) 폰켓몬과 네 번째(3번) 폰켓몬을 선택하는 방법은 한 종류(3번 폰켓몬 두 마리)의 폰켓몬만 가질 수 있지만, 다른 방법들은 모두 두 종류의 폰켓몬을 가질 수 있습니다. 따라서 위 예시에서 가질 수 있는 폰켓몬 종류 수의 최댓값은 2가 됩니다.
당신은 최대한 다양한 종류의 폰켓몬을 가지길 원하기 때문에, 최대한 많은 종류의 폰켓몬을 포함해서 N/2마리를 선택하려 합니다. N마리 폰켓몬의 종류 번호가 담긴 배열 nums가 매개변수로 주어질 때, N/2마리의 폰켓몬을 선택하는 방법 중, 가장 많은 종류의 폰켓몬을 선택하는 방법을 찾아, 그때의 폰켓몬 종류 번호의 개수를 return 하도록 solution 함수를 완성해주세요.

// 제한사항

nums는 폰켓몬의 종류 번호가 담긴 1차원 배열입니다.
nums의 길이(N)는 1 이상 10,000 이하의 자연수이며, 항상 짝수로 주어집니다.
폰켓몬의 종류 번호는 1 이상 200,000 이하의 자연수로 나타냅니다.
가장 많은 종류의 폰켓몬을 선택하는 방법이 여러 가지인 경우에도, 선택할 수 있는 폰켓몬 종류 개수의 최댓값 하나만 return 하면 됩니다.

// 입출력 예

nums	          result
[3,1,2,3]	      2
[3,3,3,2,2,4]	  3
[3,3,3,2,2,2]	  2

// 입출력 예 설명

입출력 예 #1
문제의 예시와 같습니다.
입출력 예 #2
6마리의 폰켓몬이 있으므로, 3마리의 폰켓몬을 골라야 합니다.
가장 많은 종류의 폰켓몬을 고르기 위해서는 3번 폰켓몬 한 마리, 2번 폰켓몬 한 마리, 4번 폰켓몬 한 마리를 고르면 되며, 따라서 3을 return 합니다.
입출력 예 #3
6마리의 폰켓몬이 있으므로, 3마리의 폰켓몬을 골라야 합니다.
가장 많은 종류의 폰켓몬을 고르기 위해서는 3번 폰켓몬 한 마리와 2번 폰켓몬 두 마리를 고르거나, 혹은 3번 폰켓몬 두 마리와 3번 폰켓몬 한 마리를 고르면 됩니다. 따라서 최대 고를 수 있는 폰켓몬 종류의 수는 2입니다.
```

 <details><summary><b>Answer</b></summary>

   <p>

```javascript
function solution(nums) {
  let answer = new Set(nums);
  return answer.size <= nums.length / 2 ? answer.size : nums.length / 2;
}
```

  </p>
  </details>
  <br>
  <br>

## dndbekfrl1

### 🎁 Basic

<br>

### 난이도 : 🌶

<br>

#### ☁︎ map, filter 그리고 reduce

```javascript
map, filter, reduce를 적절히 사용해
force 유저의 총 점수를 확인해보자!

var personnel = [
  {
    id: 5,
    name: "Luke Skywalker",
    pilotingScore: 98,
    shootingScore: 56,
    isForceUser: true,
  },
  {
    id: 82,
    name: "Sabine Wren",
    pilotingScore: 73,
    shootingScore: 99,
    isForceUser: false,
  },
  {
    id: 22,
    name: "Zeb Orellios",
    pilotingScore: 20,
    shootingScore: 59,
    isForceUser: false,
  },
  {
    id: 15,
    name: "Ezra Bridger",
    pilotingScore: 43,
    shootingScore: 67,
    isForceUser: true,
  },
  {
    id: 11,
    name: "Caleb Dume",
    pilotingScore: 71,
    shootingScore: 85,
    isForceUser: true,
  },
];
```

<details><summary><b>Answer</b></summary>

<p>

```javascript
[참고 아티클: https://medium.com/@saerombang11/%EB%B2%88%EC%97%AD-%EB%8B%B9%EC%8B%A0%EC%9D%98-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8%EB%A5%BC-%EA%B0%84%EC%86%8C%ED%99%94%ED%95%98%EC%84%B8%EC%9A%94-map-reduce-%EA%B7%B8%EB%A6%AC%EA%B3%A0-filter-%EB%A5%BC-%ED%86%B5%ED%95%B4%EC%84%9C-b2ace180d157 ]
[참고 https://tutorialpost.apptilus.com/code/posts/js/js-array-map/]
filter(), map(), reduce()를 활용하면 가독성이 높아진다고 합니다

1. force 유저 filter 로 거르기
let jediPersonnel = personnel.filter((person)=>{return person.isForceUser;});
//Result: {{id: 5, name: "Luke Skywalker", pilotingScore: 98, shootingScore: 56, isForceUser: true},{id: 15, name: "Ezra Bridger", pilotingScore: 43, shootingScore: 67, isForceUser: true},{id: 11, name: "Caleb Dume", pilotingScore: 71, shootingScore: 85, isForceUser: true}}
2. map을 사용해 각 총점 배열 구하기
let jediScores = jediPersonnel.map((jedi)=>{return jedi.pilotingScore+jedi.shootingScore;});
//Result: [154,110,156]
3. 총점을 얻기 위해 reduce 사용 (누적값의 초기값 0으로 설정)
let totalJediScore = jediScores.reduce((acc,score)=>{return acc+score;},0);
//Result: 420

//다음과 같이 짧게 작성할 수 있습니다.
const totalJediScore = personnel
  .filter(person => person.isForceUser)
  .map(jedi => jedi.pilotingScore + jedi.shootingScore)
  .reduce((acc, score) => acc + score, 0);


filter() => 배열의 각 항목 중 콜백함수의 표현식이 true인 항목의 배열을 반환합니다. 이를 통해 특정 조건을 만족하는 새로운 배열을 만들 수 있습니다.
personnel.filter((person)=>{return person.isForceUser;});
에서 isForceUser = true 인 값만 반환이 됐습니다!

map() => 함수가 리턴한 결과값으로 새로운 배열을 만들어 리턴합니다.

reduce() => 배열의 각 요소를 순회하면서 배열의 모든 요소를 합성합니다. 콜백함수의 첫 번째 요소로 누적될 값의 초기값을 지정해줍니다. 보통 배열의 각 요소를 하나의 값으로 줄이는데 사용됩니다.
arr.reduce(function (acc, item, index, array) {}, init);
// acc - 누적값
// item - 각 요소
// index - 인덱스
// array - 배열자신
// init - 누적값의 초깃값

let totalJediScore = jediScores.reduce((acc,score)=>{return acc+score;},0);
에서 초기값을 0으로 설정해 총점을 구했습니다!

```

  </p>
  </details>
  <br>
  <br>

### 🎁 Array

<br>

### 난이도 : 🌶

<br>

#### ☁︎ K번째 수

```javascript
[출처: https://programmers.co.kr/learn/courses/30/lessons/42748]
배열 array의 i번째 숫자부터 j번째 숫자까지 자르고 정렬했을 때, k번째에 있는 수를 구하려 합니다.

예를 들어 array가 [1, 5, 2, 6, 3, 7, 4], i = 2, j = 5, k = 3이라면

array의 2번째부터 5번째까지 자르면 [5, 2, 6, 3]입니다.
1에서 나온 배열을 정렬하면 [2, 3, 5, 6]입니다.
2에서 나온 배열의 3번째 숫자는 5입니다.
배열 array, [i, j, k]를 원소로 가진 2차원 배열 commands가 매개변수로 주어질 때, commands의 모든 원소에 대해 앞서 설명한 연산을 적용했을 때 나온 결과를 배열에 담아 return 하도록 solution 함수를 작성해주세요.

입출력 예
array	[1, 5, 2, 6, 3, 7, 4]
commands [[2, 5, 3], [4, 4, 1], [1, 7, 3]]
return [5, 6, 3]

function solution(array, commands) {
    var answer = [];
    return answer;
}

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//작성한 답
function solution(array, commands) {
  var answer = [];

  for (let m = 0; m < commands.length; m++) {
    let command = commands[m];

    let i = command[0] - 1;
    let j = command[1];
    let k = command[2] - 1;

    let tmp = array.slice(i, j);
    tmp.sort((a, b) => {
      return a - b;
    });
    answer[m] = tmp[k];
  }
  return answer;
}

//다른 사람의 풀이
function solution(array, commands) {
    return commands.map(command => {
        const [sPosition, ePosition, position] = command
        const newArray = array
            .filter((value, fIndex) => fIndex >= sPosition - 1 && fIndex <= ePosition - 1)
            .sort((a,b) => a - b)

        return newArray[position - 1]
    })
}

sort()는 문자열 비교 함수이므로 sort()에 정렬순서를 정의해야 합니다!!
p.s 앞에서 map() filter()를 공부했는데 적용은 아직 어렵네요..

```

  </p>
  </details>
  <br>
  <br>
  
 ### 🎁 If_and_Switch
 <br>

 ### 난이도 : 🌶 🌶
 <br>
 
 #### ☁︎ 조건문과 논리 연산자
 ```javascript
아래 표현식에서 어떤  alert가 실행될까요? 

if( -1||0 ) alert( 'first');
if( -1&&0 ) alert( 'second' );
if(null||-1&&1) alert( 'third' );
 ````
 <details><summary><b>Answer</b></summary>
 <p>
  
 ```javascript
0은 거짓, 다른 숫자는 다 참이다.
-1 || 0     은 true
-1 && 0     은 false
null||true  는 true
따라서 'first', 'third' 실행됨.
 ```

 </p>
 </details>
 <br>
 <br>


  
### 🎁 For_and_While

 <br>

### 난이도 : 🌶🌶🌶

 <br>

#### ☁︎ 프롬프트 창 구현하기

```javascript
사용자가 100보다 큰 숫자를 입력하도록 안내하는 프롬프트 창을 띄워보세요.
사용자가 조건에 맞지 않은 값을 입력한 경우 반복문을 사용해 동일한 프롬프트 창을 띄워줍시다.

사용자가 100을 초과하는 숫자를 입력하거나 취소 버튼을 누른 경우, 
혹은 아무것도 입력하지 않고 확인 버튼을 누른 경우엔
더는 프롬프트 창을 띄워주지 않아도 됩니다.

사용자가 오직 숫자만 입력한다고 가정하고 답안을 작성하도록 해봅시다.
숫자가 아닌 값이 입력되는 예외 상황은 처리하지 않아도 됩니다.

```
<details><summary><b>Answer</b></summary>
 <p>

```javascript
----- 정답 예시 1번 -----

let num = 0;
while( num<=100 ){
    num = prompt( "100보다 큰 숫자를 입력하세요.", '' );
    if( !num ) break;
}

----- 정답 예시 2번 -----

let num;
do{
    num = prompt( "100보다 큰 숫자를 입력하세요.", '' );
}while( num<=100 && num );

-> num이 빈 값이거나 null 일 경우 falsy 이므로 && 연산시 false가 반환되어 반복문 나감.

```

 </p>
 </details>
 <br>
 <br>

