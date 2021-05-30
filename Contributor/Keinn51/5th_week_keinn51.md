### 🎁 Array

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 내적

```javascript
// 문제 설명

길이가 같은 두 1차원 정수 배열 a, b가 매개변수로 주어집니다. a와 b의 내적을 return 하도록 solution 함수를 완성해주세요.
이때, a와 b의 내적은 a[0]*b[0] + a[1]*b[1] + ... + a[n-1]*b[n-1] 입니다. (n은 a, b의 길이)

// 제한사항

a, b의 길이는 1 이상 1,000 이하입니다.
a, b의 모든 수는 -1,000 이상 1,000 이하입니다.

// 입출력 예

a	         b	        result
[1,2,3,4]	[-3,-1,0,2]	3
[-1,0,1]	[1,0,-1]	  -2

// 입출력 예 설명

입출력 예 #1

a와 b의 내적은 1*(-3) + 2*(-1) + 3*0 + 4*2 = 3 입니다.

입출력 예 #2

a와 b의 내적은 (-1)*1 + 0*0 + 1*(-1) = -2 입니다.
```

 <details><summary><b>Answer</b></summary>

   <p>

```javascript
function solution(a, b) {
  return a.reduce((sum, _, i) => (sum += a[i] * b[i]), 0);
}
```

  </p>
  </details>
  <br>
  <br>
  

#### ☁︎ K번째수

진아님 공유문제입니다.

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
function solution(array, commands) {
  return commands.map(
    (a, i) => array.slice(a[0] - 1, a[1]).sort((a, b) => a - b)[a[2] - 1]
  );
}
```

  </p>
  </details>
  <br>
  <br>

#### ☁︎ map, filter 그리고 reduce

진아님 공유문제입니다.

```javascript
/*map, filter, reduce를 적절히 사용해
force 유저의 총 점수를 확인해보자!*/

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
function solution(personnel) {
  return personnel
    .filter((a) => a.isForceUser == true)
    .reduce((sum, curr) => (sum += curr.pilotingScore + curr.shootingScore), 0);
}
```

  </p>
  </details>
  <br>
  <br>

#### ☁︎ 로꾸꺼

kuk329님 공유문제입니다.

##### 문장이 입력되면 거꾸로 출력하는 프로그램을 만들어 봅시다.

```javascript
입출력;

입력: 거꾸로;
출력: 로꾸거;
```

 <details><summary><b>Answer</b></summary>

   <p>

```javascript
str로 받는 문제도 왠만하면 array로 바꾸어서 array의 mehtod를 쓰는게 좋은 방법인듯!

function solution(str) {
  return str.split('').reverse().join('')
}
```

  </p>
  </details>
  <br>
  <br>

<br>

### 난이도 : 🌶🌶

<br>

#### ☁︎ 역행열

```javascript
다음 출력값이 되도록 transpose함수를 만들어보세요.

let A = transpose([
  [0, 0, 0, 0, 0],
  [0, 0, 1, 0, 3],
  [0, 2, 5, 0, 1],
  [4, 2, 4, 4, 2],
  [3, 5, 1, 3, 1],
]);
console.log(A);

/*  출력값 :
[[0, 0, 0, 4, 3],
[0, 0, 2, 2, 5],
[0, 1, 5, 4, 1],
[0, 0, 0, 4, 3],
[0, 3, 1, 2, 1]]
*/
```

 <details><summary><b>Answer</b></summary>

   <p>

```javascript
const transpose = (matrix) =>
  matrix.reduce(
    (result, row) => row.map((_, i) => [...(result[i] || []),(row[i])]),
    []
  );

transpose가 너무 이해가 안 되어서 천천히 공부하면서 탐구해 본 결과입니다.
먼저 이 것을 이해하기 위해서는 이 문제에서의 reduce와 map, …문법의 기능을 확실하게 이해해야 합니다.
(1) map : 대상의 되는 배열의 ‘각 요소’를 화살표 함수의 ‘반환값으로 대체’한다.
(2) reduce : 현재 reduce에서 돌아가고 있는 인덱스의 ‘이전 반환값’을 result에 저장한다.
(3) 화살표함수 : A=>B는 B를 ‘반환’한다는 말이다.
(4) … : …에 뒤따라오는 것이 ‘배열이라면 요소만 추출’해주고, ‘빈배열이라면 삭제’한다.

이게 무슨 말인지 설명하기 위해 예를 들어볼게요.  [1,2].map(x => x * 2); 의 반환값은 [2,4]가 됩니다.이는 1,2 각각의 자리를, x*2의 결과인 2와 4가 대체했다고 볼 수 있는 것이죠.

또 reduce를 살펴보자면, [1, 2, 3].reduce((sum, curr) => sum + curr, 0); 은 0+1+2+3의 결과를 반환해줍니다. sum은 초기값인 0입니다. reduce에서 curr =1일 때, sum에는 이전 반환값인 0이 저장되어 있는 상태입니다. 그러므로 이 때 sum+curr의 결과값으로 0+1 = 1이 반환되며 , 이는 ‘다음 인덱스’의 sum이 되는 겁니다. 이 말은 curr=2일 때 이전 인덱스에서의 반환값인 화살표 함수의 반환값(sum + curr)인 0+1이 불려와 sum에 저장되어 있다는 말입니다. 그러므로 curr=2일때의 sum+curr값은 1+2 = 3이 되는 것입니다. 그렇게 sum에는 0 -> 0+1 -> 0+1+2 이렇게 순차적으로 저장되다가 마지막에 3을 더하고 이를 반환합니다.

마지막으로 …문법인데 이 친구가 신기한 것이, [1, 2, ...[3]]는 [1,2,3]이 되고, [1, 2, ...[]]은 [1,2]가 됩니다. 이 문법에 대해서 더 알고 싶으신 분들은 이 분 블로그<https://yuddomack.tistory.com/entry/자바스크립트-문법-비구조화-할당>를 참고하시구 일단은 이렇다는 것만 압니다.

/*문제에 대해서만 볼려면 이 부분부터 보시면 됩니다.*/ 예시를 들어, let A = transpose([[1, 2, 3], [4, 5, 6]]) 라고 해보죠. transpose에서 각 요소를 분석하는 함수가 두 개 있습니다. reduce와 map입니다. reduce는 [1,2,3]과 [4,5,6]이 요소가 될 것이며, map은 reduce가 [1,2,3]일 때 1과 2와 3이 되며, [4,5,6]일 때는 4,5,6이 됩니다. 이 때 map은 각 요소에 ‘화살표 함수의 반환값’으로 대체해준다고 했죠? 그렇다면 map((_, i) => [(result[i] || []), row[i]])에서 reduce = [1,2,3]일 때 1 은 map = […(result[0]||[]),row[0])이 됩니다. 그런데 result[0]은 [][0]와 같고 이 값은 null입니다. […(null||[]),row[0])과 똑같기에 이 결과는 […[],1]이 됩니다. (여기서 A||B는 A의 값이 null이나 undefined가 라면 B를 반환하고, 아니라면 A를 반환합니다.) 같은 방식으로 2와 3은 […[],2],[…[],3]이 됩니다. 그러므로 reduce = [1,2,3]일 때 map을 통해서 반환되는 것은 [[…[],1],[…[],2],[…[],3]]이 되며, …문법은 빈배열을 무시해버리기 때문에 [[1],[2],[3]]이 됩니다.

다음 reduce가 [4,5,6]일 때에 result에는 ‘이전 인덱스의 반환값’인  [[1],[2],[3]]가 저장되어 있습니다. 그러므로 reduce가 [4,5,6]일 때에는 4에서 […(result[0],[]),row[0])인데 이 값은, […([1]||[]),row[0])과 같고 이는 […[1],4]와 같습니다. 그런데! …문법에서는 배열 안의 요소를 끄집어 내주기 때문에, 이는 [1,4]와 같습니다. 같은 방법으로 이후에는 [2,5],[3,6]이 나옵니다. 결론적으로 A에는 [[1,2,3],[4,5,6]]을 함수를 통해 변환해준 [[1,4],[2,5],[3,6]]이 저장되는 것입니다. 문제에서는 transpose([[0, 0, 0, 0, 0], [0, 0, 1, 0, 3], [0, 2, 5, 0, 1], [4, 2, 4, 4, 2], [3, 5, 1, 3, 1]])이기 때문에 이 값은 그렇다면, [[0, 0, 0, 4, 3],[0, 0, 2, 2, 5],[0, 1, 5, 4, 1],[0, 0, 0, 4, 3],[0, 3, 1, 2, 1]]이 됩니다. 이는 5X5배열의 행과 열을 바꾸어주는 것과 같지요!
```

  </p>
  </details>
  <br>
  <br>

#### ☁︎ 크레인 인형뽑기 게임

<br>

##### 문제 설명

게임개발자인 "죠르디"는 크레인 인형뽑기 기계를 모바일 게임으로 만들려고 합니다.
"죠르디"는 게임의 재미를 높이기 위해 화면 구성과 규칙을 다음과 같이 게임 로직에 반영하려고 합니다.

<br>

![crane_game_101](https://user-images.githubusercontent.com/79993356/119948994-609ff600-bfd4-11eb-98c6-a936b689103a.png)

<br>

게임 화면은 "1 x 1" 크기의 칸들로 이루어진 "N x N" 크기의 정사각 격자이며 위쪽에는 크레인이 있고 오른쪽에는 바구니가 있습니다. (위 그림은 "5 x 5" 크기의 예시입니다). 각 격자 칸에는 다양한 인형이 들어 있으며 인형이 없는 칸은 빈칸입니다. 모든 인형은 "1 x 1" 크기의 격자 한 칸을 차지하며 격자의 가장 아래 칸부터 차곡차곡 쌓여 있습니다. 게임 사용자는 크레인을 좌우로 움직여서 멈춘 위치에서 가장 위에 있는 인형을 집어 올릴 수 있습니다. 집어 올린 인형은 바구니에 쌓이게 되는 데, 이때 바구니의 가장 아래 칸부터 인형이 순서대로 쌓이게 됩니다. 다음 그림은 [1번, 5번, 3번] 위치에서 순서대로 인형을 집어 올려 바구니에 담은 모습입니다.

<br>

![crane_game_102](https://user-images.githubusercontent.com/79993356/119948990-5f6ec900-bfd4-11eb-97e2-31910b49f514.png)

<br>

만약 같은 모양의 인형 두 개가 바구니에 연속해서 쌓이게 되면 두 인형은 터뜨려지면서 바구니에서 사라지게 됩니다. 위 상태에서 이어서 [5번] 위치에서 인형을 집어 바구니에 쌓으면 같은 모양 인형 두 개가 없어집니다.

<br>

![crane_game_103](https://user-images.githubusercontent.com/79993356/119948982-5ed63280-bfd4-11eb-9eb3-c348704e9147.gif)

<br>

크레인 작동 시 인형이 집어지지 않는 경우는 없으나 만약 인형이 없는 곳에서 크레인을 작동시키는 경우에는 아무런 일도 일어나지 않습니다. 또한 바구니는 모든 인형이 들어갈 수 있을 만큼 충분히 크다고 가정합니다. (그림에서는 화면표시 제약으로 5칸만으로 표현하였음)
게임 화면의 격자의 상태가 담긴 2차원 배열 board와 인형을 집기 위해 크레인을 작동시킨 위치가 담긴 배열 moves가 매개변수로 주어질 때, 크레인을 모두 작동시킨 후 터트려져 사라진 인형의 개수를 return 하도록 solution 함수를 완성해주세요.

<br>

##### 제한사항

- board 배열은 2차원 배열로 크기는 "5 x 5" 이상 "30 x 30" 이하입니다.
- board의 각 칸에는 0 이상 100 이하인 정수가 담겨있습니다.
- 0은 빈 칸을 나타냅니다.
- 1 ~ 100의 각 숫자는 각기 다른 인형의 모양을 의미하며 같은 숫자는 같은 모양의 인형을 나타냅니다.
- moves 배열의 크기는 1 이상 1,000 이하입니다.
- moves 배열 각 원소들의 값은 1 이상이며 board 배열의 가로 크기 이하인 자연수입니다.

<br>

##### 입출력 예

> board  
> [[0,0,0,0,0],[0,0,1,0,3],[0,2,5,0,1],[4,2,4,4,2],[3,5,1,3,1]]

> moves
> [1,5,3,5,1,2,1,4]

> result
> 4

<br>

##### 입출력 예에 대한 설명

<>입출력 예 #1</>
인형의 처음 상태는 문제에 주어진 예시와 같습니다. 크레인이 [1, 5, 3, 5, 1, 2, 1, 4] 번 위치에서 차례대로 인형을 집어서 바구니에 옮겨 담은 후, 상태는 아래 그림과 같으며 바구니에 담는 과정에서 터트려져 사라진 인형은 4개 입니다.

![crane_game_104](https://user-images.githubusercontent.com/79993356/119948977-5c73d880-bfd4-11eb-952f-bd0cc5190639.jpg)

<br>

 <details><summary><b>Answer</b></summary>

   <p>

```javascript
const transpose = matrix =>
  matrix.reduce(
    (result, row) => row.map((_, i) => [...(result[i] || []), row[i]]),
    []
  );

/*0을 제외한 행의 요소들을 저장해주는 stacks를 만들어냄*/
const solution = (board, moves) => {
  const stacks = transpose(board).map(row =>
    row.reverse().filter(el => el !== 0)
  );
  const basket = [];
  let result = 0;

/*move를 분석해 이에 맞게 pop한 결과를 basket에 넣어준다
만약 중복된 값이라면 이를 삭제하고 result에 2를 더해준다*/
  for (const move of moves) {
    const pop = stacks[move - 1].pop();
    if (!pop) continue;
    if (pop === basket[basket.length - 1]) {
      basket.pop();
      result += 2;
      continue;
    }
    basket.push(pop);
  }

  return result;
};

transpose 함수에 관해서는 같은 주 문제의 '역배열'을 참고하세요!
역배열을 진행한 후, 각 행의 수를 basket이라는 변수에 넣어주는 과정입니다.

출처 :
https://programmers.co.kr/learn/courses/30/lessons/64061?language=javascript
```

  </p>
  </details>
  <br>
  <br>

#### ☁︎ 로또의 최고 순위와 최저 순위

```javascript
// 문제 설명

로또 6/45(이하 '로또'로 표기)는 1부터 45까지의 숫자 중 6개를 찍어서 맞히는 대표적인 복권입니다. 아래는 로또의 순위를 정하는 방식입니다. 1
순위	당첨 내용
1	   6개 번호가 모두 일치
2	   5개 번호가 일치
3    4개 번호가 일치
4	   3개 번호가 일치
5	   2개 번호가 일치
6	   그 외

로또를 구매한 민우는 당첨 번호 발표일을 학수고대하고 있었습니다.
하지만, 민우의 동생이 로또에 낙서를 하여, 일부 번호를 알아볼 수 없게 되었습니다.
당첨 번호 발표 후, 민우는 자신이 구매했던 로또로 당첨이 가능했던 최고 순위와 최저 순위를 알아보고 싶어 졌습니다.
알아볼 수 없는 번호를 0으로 표기하기로 하고, 민우가 구매한 로또 번호 6개가 44, 1, 0, 0, 31 25라고 가정해보겠습니다.
당첨 번호 6개가 31, 10, 45, 1, 6, 19라면, 당첨 가능한 최고 순위와 최저 순위의 한 예는 아래와 같습니다.

당첨 번호	     31	  10	 45	 1	6	 19	 결과
최고 순위 번호	31	0→10	44	1	0→6	25	4개 번호 일치, 3등
최저 순위 번호	31	0→11	44	1	0→7	25	2개 번호 일치, 5등

순서와 상관없이, 구매한 로또에 당첨 번호와 일치하는 번호가 있으면 맞힌 걸로 인정됩니다.
알아볼 수 없는 두 개의 번호를 각각 10, 6이라고 가정하면 3등에 당첨될 수 있습니다.
3등을 만드는 다른 방법들도 존재합니다. 하지만, 2등 이상으로 만드는 것은 불가능합니다.
알아볼 수 없는 두 개의 번호를 각각 11, 7이라고 가정하면 5등에 당첨될 수 있습니다.
5등을 만드는 다른 방법들도 존재합니다. 하지만, 6등(낙첨)으로 만드는 것은 불가능합니다.
민우가 구매한 로또 번호를 담은 배열 lottos, 당첨 번호를 담은 배열 win_nums가 매개변수로 주어집니다.
이때, 당첨 가능한 최고 순위와 최저 순위를 차례대로 배열에 담아서 return 하도록 solution 함수를 완성해주세요.

// 제한사항

lottos는 길이 6인 정수 배열입니다.
lottos의 모든 원소는 0 이상 45 이하인 정수입니다.
0은 알아볼 수 없는 숫자를 의미합니다.
0을 제외한 다른 숫자들은 lottos에 2개 이상 담겨있지 않습니다.
lottos의 원소들은 정렬되어 있지 않을 수도 있습니다.
win_nums은 길이 6인 정수 배열입니다.
win_nums의 모든 원소는 1 이상 45 이하인 정수입니다.
win_nums에는 같은 숫자가 2개 이상 담겨있지 않습니다.
win_nums의 원소들은 정렬되어 있지 않을 수도 있습니다.

// 입출력 예

lottos	win_nums	result
[44, 1, 0, 0, 31, 25]	[31, 10, 45, 1, 6, 19]	[3, 5]
[0, 0, 0, 0, 0, 0]	[38, 19, 20, 40, 15, 25]	[1, 6]
[45, 4, 35, 20, 3, 9]	[20, 9, 3, 45, 4, 35]	[1, 1]

// 입출력 예 설명

입출력 예 #1
문제 예시와 같습니다.

입출력 예 #2
알아볼 수 없는 번호들이 아래와 같았다면, 1등과 6등에 당첨될 수 있습니다.
당첨 번호	20	9	3	45	4	35	결과
최고 순위 번호	0→20	0→9	0→3	0→45	0→4	0→35	6개 번호 일치, 1등
최저 순위 번호	0→21	0→22	0→23	0→24	0→25	0→26	0개 번호 일치, 6등

입출력 예 #3
민우가 구매한 로또의 번호와 당첨 번호가 모두 일치하므로, 최고 순위와 최저 순위는 모두 1등입니다.
```

 <details><summary><b>Answer</b></summary>

   <p>

<a href="https://programmers.co.kr/learn/courses/30/lessons/77484?language=javascript">출처</a>

```javascript
// 📌 제가 사용한 풀이
function solution(lottos, win_nums) {
  let a = 7 - lottos.reduce((res, curr) => res += win_nums.reduce((res2, curr2) => res2 += (curr2 == curr) ? 1 : 0, 0), 0);
  let b = a - lottos.reduce((res, curr) => res += (curr == 0) ? 1 : 0, 0);
  let c = (b == 7) ? 6 : b, d = (a == 7) ? 6 : a

  return [c, d]
}

reduce를 세 번 사용한 풀이입니다.
변수가 네 번이나 사용되고, 반복도 세 번 사용되어서 불필요한 감이 있습니다.

// 📌 프로그래머스 풀이
function solution(lottos, win_nums) {
    const rank = [6, 6, 5, 4, 3, 2, 1];

    let minCount = lottos.filter(v => win_nums.includes(v)).length;
    let zeroCount = lottos.filter(v => !v).length;

    const maxCount = minCount + zeroCount;

    return [rank[maxCount], rank[minCount]];
}

filter을 사용해 (1) 일치하는 횟수를 mincount에 정의 (2) 0의 갯수를 zerocount에 정의해서 maxcount에 전달.
반복문도 두 번 사용했으며 변수도 세 번 사용되었기 때문에 제가 했던 풀이보다 짧은 실행 시간을 보여줍니다.
```

  </p>
  </details>
  <br>
  <br>
  
  #### ☁︎ 신규 아이디 추천

```javascript
// 문제 설명

카카오에 입사한 신입 개발자 네오는 "카카오계정개발팀"에 배치되어, 카카오 서비스에 가입하는 유저들의 아이디를 생성하는 업무를 담당하게 되었습니다. "네오"에게 주어진 첫 업무는 새로 가입하는 유저들이 카카오 아이디 규칙에 맞지 않는 아이디를 입력했을 때, 입력된 아이디와 유사하면서 규칙에 맞는 아이디를 추천해주는 프로그램을 개발하는 것입니다.
다음은 카카오 아이디의 규칙입니다.

아이디의 길이는 3자 이상 15자 이하여야 합니다.
아이디는 알파벳 소문자, 숫자, 빼기(-), 밑줄(_), 마침표(.) 문자만 사용할 수 있습니다.
단, 마침표(.)는 처음과 끝에 사용할 수 없으며 또한 연속으로 사용할 수 없습니다.

"네오"는 다음과 같이 7단계의 순차적인 처리 과정을 통해 신규 유저가 입력한 아이디가 카카오 아이디 규칙에 맞는 지 검사하고 규칙에 맞지 않은 경우 규칙에 맞는 새로운 아이디를 추천해 주려고 합니다.
신규 유저가 입력한 아이디가 new_id 라고 한다면,

1단계 new_id의 모든 대문자를 대응되는 소문자로 치환합니다.
2단계 new_id에서 알파벳 소문자, 숫자, 빼기(-), 밑줄(_), 마침표(.)를 제외한 모든 문자를 제거합니다.
3단계 new_id에서 마침표(.)가 2번 이상 연속된 부분을 하나의 마침표(.)로 치환합니다.
4단계 new_id에서 마침표(.)가 처음이나 끝에 위치한다면 제거합니다.
5단계 new_id가 빈 문자열이라면, new_id에 "a"를 대입합니다.
6단계 new_id의 길이가 16자 이상이면, new_id의 첫 15개의 문자를 제외한 나머지 문자들을 모두 제거합니다.
     만약 제거 후 마침표(.)가 new_id의 끝에 위치한다면 끝에 위치한 마침표(.) 문자를 제거합니다.
7단계 new_id의 길이가 2자 이하라면, new_id의 마지막 문자를 new_id의 길이가 3이 될 때까지 반복해서 끝에 붙입니다.

예를 들어, new_id 값이 "...!@BaT#*..y.abcdefghijklm" 라면, 위 7단계를 거치고 나면 new_id는 아래와 같이 변경됩니다.

1단계 대문자 'B'와 'T'가 소문자 'b'와 't'로 바뀌었습니다.
"...!@BaT#*..y.abcdefghijklm" → "...!@bat#*..y.abcdefghijklm"

2단계 '!', '@', '#', '*' 문자가 제거되었습니다.
"...!@bat#*..y.abcdefghijklm" → "...bat..y.abcdefghijklm"

3단계 '...'와 '..' 가 '.'로 바뀌었습니다.
"...bat..y.abcdefghijklm" → ".bat.y.abcdefghijklm"

4단계 아이디의 처음에 위치한 '.'가 제거되었습니다.
".bat.y.abcdefghijklm" → "bat.y.abcdefghijklm"

5단계 아이디가 빈 문자열이 아니므로 변화가 없습니다.
"bat.y.abcdefghijklm" → "bat.y.abcdefghijklm"

6단계 아이디의 길이가 16자 이상이므로, 처음 15자를 제외한 나머지 문자들이 제거되었습니다.
"bat.y.abcdefghijklm" → "bat.y.abcdefghi"

7단계 아이디의 길이가 2자 이하가 아니므로 변화가 없습니다.
"bat.y.abcdefghi" → "bat.y.abcdefghi"

따라서 신규 유저가 입력한 new_id가 "...!@BaT#*..y.abcdefghijklm"일 때, 네오의 프로그램이 추천하는 새로운 아이디는 "bat.y.abcdefghi" 입니다.

// [문제]

신규 유저가 입력한 아이디를 나타내는 new_id가 매개변수로 주어질 때, "네오"가 설계한 7단계의 처리 과정을 거친 후의 추천 아이디를 return 하도록 solution 함수를 완성해 주세요.

// [제한사항]

new_id는 길이 1 이상 1,000 이하인 문자열입니다.
new_id는 알파벳 대문자, 알파벳 소문자, 숫자, 특수문자로 구성되어 있습니다.
new_id에 나타날 수 있는 특수문자는 -_.~!@#$%^&*()=+[{]}:?,<>/ 로 한정됩니다.

// [입출력 예]

no	  new_id	                       result
예1	   "...!@BaT#*..y.abcdefghijklm"	"bat.y.abcdefghi"
예2	   "z-+.^."	                      "z--"
예3	   "=.="	                        "aaa"
예4	   "123_.def"	                    "123_.def"
예5	   "abcdefghijklmn.p"	            "abcdefghijklmn"

// 입출력 예에 대한 설명

입출력 예 #1
문제의 예시와 같습니다.

입출력 예 #2
7단계를 거치는 동안 new_id가 변화하는 과정은 아래와 같습니다.
1단계 변화 없습니다.
2단계 "z-+.^." → "z-.."
3단계 "z-.." → "z-."
4단계 "z-." → "z-"
5단계 변화 없습니다.
6단계 변화 없습니다.
7단계 "z-" → "z--"

입출력 예 #3
7단계를 거치는 동안 new_id가 변화하는 과정은 아래와 같습니다.
1단계 변화 없습니다.
2단계 "=.=" → "."
3단계 변화 없습니다.
4단계 "." → "" (new_id가 빈 문자열이 되었습니다.)
5단계 "" → "a"
6단계 변화 없습니다.
7단계 "a" → "aaa"

입출력 예 #4
1단계에서 7단계까지 거치는 동안 new_id("123_.def")는 변하지 않습니다. 즉, new_id가 처음부터 카카오의 아이디 규칙에 맞습니다.

입출력 예 #5
1단계 변화 없습니다.
2단계 변화 없습니다.
3단계 변화 없습니다.
4단계 변화 없습니다.
5단계 변화 없습니다.
6단계 "abcdefghijklmn.p" → "abcdefghijklmn." → "abcdefghijklmn"
7단계 변화 없습니다.
```

 <details><summary><b>Answer</b></summary>

   <p>

<a href="https://programmers.co.kr/learn/courses/30/lessons/72410?language=javascript">출처</a>

```javascript
// 📌 정규식이 없는 풀이

function solution(nid) {
  var ans = "";
  for (let i = 0; i < nid.length; i++) {
    let c = nid[i].toLowerCase(); // 1
    if ("0123456789abcdefghijklmnopqrstuvwxyz.-_".indexOf(c) === -1) continue;
    if (c === "." && ans[ans.length - 1] === ".") continue;
    ans += c; //2
  }
  if (ans[0] === ".") ans = ans.slice(1); //3
  ans = ans.slice(0, 15); //6
  if (ans[ans.length - 1] === ".") ans = ans.slice(0, ans.length - 1); //4
  if (!ans) ans = "a"; //5
  while (ans.length < 3) ans += ans[ans.length - 1]; //7
  return ans;
}
```

  </p>
  </details>
  <br>
  <br>
