# dndbekfrl1's Problems

### ๐ Basic

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ map, filter ๊ทธ๋ฆฌ๊ณ  reduce

```javascript
map, filter, reduce๋ฅผ ์ ์ ํ ์ฌ์ฉํด
force ์ ์ ์ ์ด ์ ์๋ฅผ ํ์ธํด๋ณด์!

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
[์ฐธ๊ณ  ์ํฐํด: https://medium.com/@saerombang11/%EB%B2%88%EC%97%AD-%EB%8B%B9%EC%8B%A0%EC%9D%98-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8%EB%A5%BC-%EA%B0%84%EC%86%8C%ED%99%94%ED%95%98%EC%84%B8%EC%9A%94-map-reduce-%EA%B7%B8%EB%A6%AC%EA%B3%A0-filter-%EB%A5%BC-%ED%86%B5%ED%95%B4%EC%84%9C-b2ace180d157 ]
[์ฐธ๊ณ  https://tutorialpost.apptilus.com/code/posts/js/js-array-map/]
filter(), map(), reduce()๋ฅผ ํ์ฉํ๋ฉด ๊ฐ๋์ฑ์ด ๋์์ง๋ค๊ณ  ํฉ๋๋ค

1. force ์ ์  filter ๋ก ๊ฑฐ๋ฅด๊ธฐ
let jediPersonnel = personnel.filter((person)=>{return person.isForceUser;});
//Result: {{id: 5, name: "Luke Skywalker", pilotingScore: 98, shootingScore: 56, isForceUser: true},{id: 15, name: "Ezra Bridger", pilotingScore: 43, shootingScore: 67, isForceUser: true},{id: 11, name: "Caleb Dume", pilotingScore: 71, shootingScore: 85, isForceUser: true}}
2. map์ ์ฌ์ฉํด ๊ฐ ์ด์  ๋ฐฐ์ด ๊ตฌํ๊ธฐ
let jediScores = jediPersonnel.map((jedi)=>{return jedi.pilotingScore+jedi.shootingScore;});
//Result: [154,110,156]
3. ์ด์ ์ ์ป๊ธฐ ์ํด reduce ์ฌ์ฉ (๋์ ๊ฐ์ ์ด๊ธฐ๊ฐ 0์ผ๋ก ์ค์ )
let totalJediScore = jediScores.reduce((acc,score)=>{return acc+score;},0);
//Result: 420

//๋ค์๊ณผ ๊ฐ์ด ์งง๊ฒ ์์ฑํ  ์ ์์ต๋๋ค.
const totalJediScore = personnel
  .filter(person => person.isForceUser)
  .map(jedi => jedi.pilotingScore + jedi.shootingScore)
  .reduce((acc, score) => acc + score, 0);


filter() => ๋ฐฐ์ด์ ๊ฐ ํญ๋ชฉ ์ค ์ฝ๋ฐฑํจ์์ ํํ์์ด true์ธ ํญ๋ชฉ์ ๋ฐฐ์ด์ ๋ฐํํฉ๋๋ค. ์ด๋ฅผ ํตํด ํน์  ์กฐ๊ฑด์ ๋ง์กฑํ๋ ์๋ก์ด ๋ฐฐ์ด์ ๋ง๋ค ์ ์์ต๋๋ค.
personnel.filter((person)=>{return person.isForceUser;});
์์ isForceUser = true ์ธ ๊ฐ๋ง ๋ฐํ์ด ๋์ต๋๋ค!

map() => ํจ์๊ฐ ๋ฆฌํดํ ๊ฒฐ๊ณผ๊ฐ์ผ๋ก ์๋ก์ด ๋ฐฐ์ด์ ๋ง๋ค์ด ๋ฆฌํดํฉ๋๋ค.

reduce() => ๋ฐฐ์ด์ ๊ฐ ์์๋ฅผ ์ํํ๋ฉด์ ๋ฐฐ์ด์ ๋ชจ๋  ์์๋ฅผ ํฉ์ฑํฉ๋๋ค. ์ฝ๋ฐฑํจ์์ ์ฒซ ๋ฒ์งธ ์์๋ก ๋์ ๋  ๊ฐ์ ์ด๊ธฐ๊ฐ์ ์ง์ ํด์ค๋๋ค. ๋ณดํต ๋ฐฐ์ด์ ๊ฐ ์์๋ฅผ ํ๋์ ๊ฐ์ผ๋ก ์ค์ด๋๋ฐ ์ฌ์ฉ๋ฉ๋๋ค.
arr.reduce(function (acc, item, index, array) {}, init);
// acc - ๋์ ๊ฐ
// item - ๊ฐ ์์
// index - ์ธ๋ฑ์ค
// array - ๋ฐฐ์ด์์ 
// init - ๋์ ๊ฐ์ ์ด๊น๊ฐ

let totalJediScore = jediScores.reduce((acc,score)=>{return acc+score;},0);
์์ ์ด๊ธฐ๊ฐ์ 0์ผ๋ก ์ค์ ํด ์ด์ ์ ๊ตฌํ์ต๋๋ค!




```

</p>
</details>

### ๐ Array

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ ๋ฒ๋ธ ์ ๋ ฌ ๊ตฌํํ๊ธฐ

```javascript
[์ถ์ฒ: JS100์  ๋ฌธ์  50]
๋ฒ๋ธ์ ๋ ฌ์ ๋ ์ธ์ ํ ์์๋ฅผ ๊ฒ์ฌํ์ฌ ์ ๋ ฌํ๋ ๋ฐฉ๋ฒ์ ๋งํฉ๋๋ค. ์๊ฐ ๋ณต์ก๋๋ ๋๋ฆฌ์ง๋ง ์ฝ๋๊ฐ ๋จ์ํ๊ธฐ ๋๋ฌธ์ ์์ฃผ ์ฌ์ฉ๋ฉ๋๋ค. ๋ค์ ์ฝ๋๋ฅผ ์์ฑํ์ธ์.

function bubble(arr) {
  let result = arr.slice();

  for (let i = 0; i < result.length - 1; i++) {
    for (/*๋น์นธ์ ์ฑ์์ฃผ์ธ์.*/) {
      if (result[j] > result[j + 1]) {
         //๋น์นธ์ ์ฑ์์ฃผ์ธ์.
      }
    }
  }
  return result;
}
const items = prompt('์๋ ฅํด์ฃผ์ธ์.').split(' ').map((n) => {
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
const items = prompt("์๋ ฅํด์ฃผ์ธ์.")
  .split(" ")
  .map((n) => {
    return parseInt(n, 10);
  });

console.log(bubble(items));
```

</p>
</details>

### ๐ Array

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ ์ต๋๊ฐ ๊ตฌํ๊ธฐ

```javascript
[์ถ์ฒ: JS100์  ๋ฌธ์  49]
์์๊ฐ ์๋ 10๊ฐ์ ์ซ์๊ฐ ๊ณต๋ฐฑ์ผ๋ก ๊ตฌ๋ถ๋์ด ์ฃผ์ด์ง๋ค. ์ฃผ์ด์ง ์ซ์๋ค ์ค ์ต๋๊ฐ์ ๋ฐํํ๋ผ.

์์ถ๋ ฅ

์๋ ฅ : 10 9 8 7 6 5 4 3 2 1
์ถ๋ ฅ : 10

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//์์ฑํ ๋ต
let array = prompt("10๊ฐ์ ์ซ์๋ฅผ ์๋ ฅํ์ธ์")
  .split(" ")
  .map((n) => {
    return parseInt(n);
  });
let ans = -1;
for (let i = 0; i < array.length - 1; i++) {
  ans = Math.max(ans, array[i]);
}
console.log(ans);

//๋ต์
let numbers = prompt("10๊ฐ์ ์ซ์๋ฅผ ์๋ ฅํ์ธ์")
  .split(" ")
  .map((n) => {
    return parseInt(n, 10);
  });

numbers.sort((a, b) => {
  return b - a;
});

console.log(numbers[0]);
```

</p>
</details>

### ๐ Array

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ ๊ฐ์ด๋ฐ ๊ธ์ ๊ฐ์ ธ์ค๊ธฐ

```javascript
[์ถ์ฒ: https://programmers.co.kr/learn/courses/30/lessons/12903]
๋จ์ด s์ ๊ฐ์ด๋ฐ ๊ธ์๋ฅผ ๋ฐํํ๋ ํจ์, solution์ ๋ง๋ค์ด ๋ณด์ธ์. ๋จ์ด์ ๊ธธ์ด๊ฐ ์ง์๋ผ๋ฉด ๊ฐ์ด๋ฐ ๋๊ธ์๋ฅผ ๋ฐํํ๋ฉด ๋ฉ๋๋ค.

์์ถ๋ ฅ ์:
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
//์์ฑํ ๋ต
function solution(s) {
  var answer = "";
  var index = 0;
  //ํ์
  if (s.length % 2 == 1) {
    index = parseInt(s.length / 2);
    answer = s[index];
  }
  //์ง์
  else {
    index = s.length / 2;
    answer = s[index - 1] + s[index];
  }

  return answer;
}

//๋ค๋ฅธ ์ฌ๋ ํ์ด
function solution(s) {
  const mid = Math.floor(s.length / 2);
  return s.length % 2 === 1 ? s[mid] : s[mid - 1] + s[mid];
}
//Math.floor()์ ์ฃผ์ด์ง ์ซ์์ ๊ฐ๊ฑฐ๋ ์์ ์ ์ ์ค์์ ๊ฐ์ฅ ํฐ ์๋ฅผ ๋ฐํํ๋ค. ์) Math.floor(5.25) => 5
```

</p>
</details>

### ๐ Array

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ K๋ฒ์งธ ์

```javascript
[์ถ์ฒ: https://programmers.co.kr/learn/courses/30/lessons/42748]
๋ฐฐ์ด array์ i๋ฒ์งธ ์ซ์๋ถํฐ j๋ฒ์งธ ์ซ์๊น์ง ์๋ฅด๊ณ  ์ ๋ ฌํ์ ๋, k๋ฒ์งธ์ ์๋ ์๋ฅผ ๊ตฌํ๋ ค ํฉ๋๋ค.

์๋ฅผ ๋ค์ด array๊ฐ [1, 5, 2, 6, 3, 7, 4], i = 2, j = 5, k = 3์ด๋ผ๋ฉด

array์ 2๋ฒ์งธ๋ถํฐ 5๋ฒ์งธ๊น์ง ์๋ฅด๋ฉด [5, 2, 6, 3]์๋๋ค.
1์์ ๋์จ ๋ฐฐ์ด์ ์ ๋ ฌํ๋ฉด [2, 3, 5, 6]์๋๋ค.
2์์ ๋์จ ๋ฐฐ์ด์ 3๋ฒ์งธ ์ซ์๋ 5์๋๋ค.
๋ฐฐ์ด array, [i, j, k]๋ฅผ ์์๋ก ๊ฐ์ง 2์ฐจ์ ๋ฐฐ์ด commands๊ฐ ๋งค๊ฐ๋ณ์๋ก ์ฃผ์ด์ง ๋, commands์ ๋ชจ๋  ์์์ ๋ํด ์์ ์ค๋ชํ ์ฐ์ฐ์ ์ ์ฉํ์ ๋ ๋์จ ๊ฒฐ๊ณผ๋ฅผ ๋ฐฐ์ด์ ๋ด์ return ํ๋๋ก solution ํจ์๋ฅผ ์์ฑํด์ฃผ์ธ์.

์์ถ๋ ฅ ์
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
//์์ฑํ ๋ต
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

//๋ค๋ฅธ ์ฌ๋์ ํ์ด
function solution(array, commands) {
    return commands.map(command => {
        const [sPosition, ePosition, position] = command
        const newArray = array
            .filter((value, fIndex) => fIndex >= sPosition - 1 && fIndex <= ePosition - 1)
            .sort((a,b) => a - b)

        return newArray[position - 1]
    })
}

sort()๋ ๋ฌธ์์ด ๋น๊ต ํจ์์ด๋ฏ๋ก sort()์ ์ ๋ ฌ์์๋ฅผ ์ ์ํด์ผ ํฉ๋๋ค!!
p.s ์์์ map() filter()๋ฅผ ๊ณต๋ถํ๋๋ฐ ์ ์ฉ์ ์์ง ์ด๋ ต๋ค์..

```

</p>
</details>

### ๐ Basic

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ ์ค๋ณต ๋ฌธ์ ์ ๊ฑฐ

```javascript
์ฃผ์ด์ง str์ ์ค๋ณต ๋ฌธ์๋ฅผ ์ ๊ฑฐํ์ธ์.

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
