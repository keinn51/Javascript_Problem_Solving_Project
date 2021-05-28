# dndbekfrl1's Problems

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

### 🎁 Array

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 버블 정렬 구현하기

```javascript
[출처: JS100제 문제 50]
버블정렬은 두 인접한 원소를 검사하여 정렬하는 방법을 말합니다. 시간 복잡도는 느리지만 코드가 단순하기 때문에 자주 사용됩니다. 다음 코드를 작성하세요.

function bubble(arr) {
  let result = arr.slice();

  for (let i = 0; i < result.length - 1; i++) {
    for (/*빈칸을 채워주세요.*/) {
      if (result[j] > result[j + 1]) {
         //빈칸을 채워주세요.
      }
    }
  }
  return result;
}
const items = prompt('입력해주세요.').split(' ').map((n) => {
  return parseInt(n, 10);
});

console.log(bubble(items));

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
function bubble(arr) {
  let result = arr.slice();

  for (let i = 0; i < result.length - 1; i++) {
    for (let j = 0; j < result.length - i; j++) {
      if (result[j] > result[j + 1]) {
        tmp = result[j];
        result[j] = result[j + 1];
        result[j + 1] = tmp;
      }
    }
  }
  return result;
}
const items = prompt("입력해주세요.")
  .split(" ")
  .map((n) => {
    return parseInt(n, 10);
  });

console.log(bubble(items));
```

</p>
</details>

### 🎁 Array

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 최댓값 구하기

```javascript
[출처: JS100제 문제 49]
순서가 없는 10개의 숫자가 공백으로 구분되어 주어진다. 주어진 숫자들 중 최댓값을 반환하라.

입출력

입력 : 10 9 8 7 6 5 4 3 2 1
출력 : 10

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//작성한 답
let array = prompt("10개의 숫자를 입력하세요")
  .split(" ")
  .map((n) => {
    return parseInt(n);
  });
let ans = -1;
for (let i = 0; i < array.length - 1; i++) {
  ans = Math.max(ans, array[i]);
}
console.log(ans);

//답안
let numbers = prompt("10개의 숫자를 입력하세요")
  .split(" ")
  .map((n) => {
    return parseInt(n, 10);
  });

numbers.sort((a, b) => {
  return b - a;
});

console.log(numbers[0]);
```

### 🎁 Array

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 가운데 글자 가져오기

```javascript
[출처: https://programmers.co.kr/learn/courses/30/lessons/12903]
단어 s의 가운데 글자를 반환하는 함수, solution을 만들어 보세요. 단어의 길이가 짝수라면 가운데 두글자를 반환하면 됩니다.

입출력 예:
s	return
"abcde"	"c"
"qwer"	"we"

function solution(s) {
    var answer = '';
    return answer;
}

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//작성한 답
function solution(s) {
  var answer = "";
  var index = 0;
  //홀수
  if (s.length % 2 == 1) {
    index = parseInt(s.length / 2);
    answer = s[index];
  }
  //짝수
  else {
    index = s.length / 2;
    answer = s[index - 1] + s[index];
  }

  return answer;
}

//다른 사람 풀이
function solution(s) {
  const mid = Math.floor(s.length / 2);
  return s.length % 2 === 1 ? s[mid] : s[mid - 1] + s[mid];
}
//Math.floor()은 주어진 숫자와 같거나 작은 정수 중에서 가장 큰 수를 반환한다. 예) Math.floor(5.25) => 5
```

</p>
</details>

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

### 🎁 Basic

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 중복 문자 제거

```javascript
주어진 str의 중복 문자를 제거하세요.

function solution(s) {
  let answer = "";
}

let str = "ksekkset";
console.log(solution(str));
```

<details><summary><b>Answer</b></summary>

<p>

```javascript
function solution(s) {
  let answer = "";
  for (let i = 0; i < s.length; i++) {
    if (s.indexOf(s[i]) == i) answer += s[i];
  }
}

let str = "ksekkset";
console.log(solution(str));
```

</p>
</details>
