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

또 reduce를 살펴보자면, [1, 2, 3].reduce((sum, curr) => sum + curr, 0); 은 0+1+2+3의 결과를 반환해줍니다.
sum은 초기값인 0입니다. reduce에서 curr =1일 때, sum에는 이전 반환값인 0이 저장되어 있는 상태입니다.
그러므로 이 때 sum+curr의 결과값으로 0+1 = 1이 반환되며 , 이는 ‘다음 인덱스’의 sum이 되는 겁니다.
이 말은 curr=2일 때 이전 인덱스에서의 반환값인 화살표 함수의 반환값(sum + curr)인 0+1이 불려와 sum에 저장되어 있다는 말입니다.
그러므로 curr=2일때의 sum+curr값은 1+2 = 3이 되는 것입니다. 그렇게 sum에는 0 -> 0+1 -> 0+1+2 이렇게 순차적으로 저장되다가 마지막에 3을 더하고 이를 반환합니다.

마지막으로 …문법인데 이 친구가 신기한 것이, [1, 2, ...[3]]는 [1,2,3]이 되고, [1, 2, ...[]]은 [1,2]가 됩니다.
이 문법에 대해서 더 알고 싶으신 분들은 이 분 블로그<https://yuddomack.tistory.com/entry/자바스크립트-문법-비구조화-할당>를 참고하시구 일단은 이렇다는 것만 압니다.

/*문제에 대해서만 볼려면 이 부분부터 보시면 됩니다.*/ 예시를 들어, let A = transpose([[1, 2, 3], [4, 5, 6]]) 라고 해보죠.
transpose에서 각 요소를 분석하는 함수가 두 개 있습니다. reduce와 map입니다.
reduce는 [1,2,3]과 [4,5,6]이 요소가 될 것이며, map은 reduce가 [1,2,3]일 때 1과 2와 3이 되며, [4,5,6]일 때는 4,5,6이 됩니다.
이 때 map은 각 요소에 ‘화살표 함수의 반환값’으로 대체해준다고 했죠?
그렇다면 map((_, i) => [(result[i] || []), row[i]])에서 reduce = [1,2,3]일 때 1 은 map = […(result[0]||[]),row[0])이 됩니다.
그런데 result[0]은 [][0]와 같고 이 값은 null입니다. […(null||[]),row[0])과 똑같기에 이 결과는 […[],1]이 됩니다.
(여기서 A||B는 A의 값이 null이나 undefined가 라면 B를 반환하고, 아니라면 A를 반환합니다.) 같은 방식으로 2와 3은 […[],2],[…[],3]이 됩니다.
그러므로 reduce = [1,2,3]일 때 map을 통해서 반환되는 것은 [[…[],1],[…[],2],[…[],3]]이 되며, …문법은 빈배열을 무시해버리기 때문에 [[1],[2],[3]]이 됩니다.

다음 reduce가 [4,5,6]일 때에 result에는 ‘이전 인덱스의 반환값’인  [[1],[2],[3]]가 저장되어 있습니다.
그러므로 reduce가 [4,5,6]일 때에는 4에서 […(result[0],[]),row[0])인데 이 값은, […([1]||[]),row[0])과 같고 이는 […[1],4]와 같습니다.
그런데! …문법에서는 배열 안의 요소를 끄집어 내주기 때문에, 이는 [1,4]와 같습니다. 같은 방법으로 이후에는 [2,5],[3,6]이 나옵니다.
결론적으로 A에는 [[1,2,3],[4,5,6]]을 함수를 통해 변환해준 [[1,4],[2,5],[3,6]]이 저장되는 것입니다.
문제에서는 transpose([[0, 0, 0, 0, 0], [0, 0, 1, 0, 3], [0, 2, 5, 0, 1], [4, 2, 4, 4, 2], [3, 5, 1, 3, 1]])이기 때문에
이 값은 그렇다면, [[0, 0, 0, 4, 3],[0, 0, 2, 2, 5],[0, 1, 5, 4, 1],[0, 0, 0, 4, 3],[0, 3, 1, 2, 1]]이 됩니다. 이는 5X5배열의 행과 열을 바꾸어주는 것과 같지요!
```

  </p>
  </details>
  <br>
  <br>
  
## by kuk329

### 🎁 Basic

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 문제1: 다음 코드의 출력값을 예측해 보세요.

```javascript
alert(2 + 2 + "1");
```

<details><summary><b>Answer</b></summary>
<p>

```javascript
정답: '41' (문자열)


우선 연산은 왼쪽에서 오른쪽으로 순차적으로 진행된다. 그리고 두개의 숫자 뒤에
문자열이 오는 경우 , 숫자가 먼저 더해지고, 그 후 더해진 숫자와 문자열과의 병합이 일어난다.

이처럼 이항 덧셈 연산자 + 는 문자열과 변환이라는 특별한 기능을 제공한다.
다른 산술 연산자가 오직 숫자형의 피연산자만 다루고, 피연산자가 숫자형이 아닌 경우에 그 형을 숫자형으로
바꾸는 것과는 대조적이다.

* 참고로 - 와 / 연산자도 어떤식으로 문자형 피연산자를 다루는지 보면

alert( 6 - '2'); // 4  : '2' 를 숫자로 바꾼 후 연산이 진행된다.
alert( '6' / 2 ); // 3  :  두 피연산자가 숫자로 바뀐 후 연산이 진행된다.

* 추가

덧셈 연산자 +는 이항 연산자 뿐만 아니라 단항 연산자로도 사용할 수 있다.
이때 피연산자가 숫자가 아닐경우 숫자형으로의 변환이 일어난다.
즉 Number(..) 와 동일한 역할을 해주는 것이다.

alert( +true ) // 1 (숫자)
alert( +"" );  //  0 (숫자)

```

</p>
</details>

<br>
<br>

### 🎁 Basic

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 문제2: 다음 2개의 변수에 저장된 값들을 숫자형으로 만들어서 더해보세요.

```javascript
let apples = "2";
let oranges = "3";
```

<details><summary><b>Answer</b></summary>
<p>

```javascript
답:
alert(+apples + +oranges); // 5 (숫자)

+ 추가 답:
alert( Number(apples) + Number(oranges) ); // 5 (숫자)


* 참고

alert( apples + oranges ); // 23 (문자열) : 이항 덧셈 연산자는 문자열을 연결한다.


쉬운 개념이지만 잘 모를수도 있는 개념일것같아서 저도 이번에 공부하며 새로 알게된 내용이라 공유합니다 !
```

</p>
</details>

<br>
<br>

# dndbekfrl1's Problems

### 🎁 Basic

<br>

### 난이도 : 🌶🌶

<br>

#### ☁︎ 신규 아이디 추천

```javascript
[출처:https://programmers.co.kr/learn/courses/30/lessons/72410]
신규 유저가 입력한 아이디를 나타내는 new_id가 매개변수로 주어질 때, "네오"가 설계한 7단계의 처리 과정을 거친 후의 추천 아이디를 return 하도록 solution 함수를 완성해 주세요.
(문제 설명이 길어서 생략합니다! 프로그래머스에서 확인해주세요)

function solution(new_id) {
    var answer = '';

    return answer;
}
```

<details><summary><b>Answer</b></summary>

<p>

```javascript
이번 문제로 정규식을 알아봤습니다.

다른 사람 풀이
function solution(new_id) {
    const answer = new_id
        .toLowerCase()
        .replace(/[^\w-_.]/g, '')
        .replace(/\.{2,}/g, '.')
        .replace(/^\.|\.$/g, '')
        .replace(/^$/, 'a')
        .slice(0, 15).replace(/\.$/, '');
    const len = answer.length;
    return len > 2 ? answer : answer + answer.charAt(len - 1).repeat(3 - len);
}

다음 사이트에서 정규식을 이해하기 좋습니다.
[https://regexr.com/]

/[^\w-_.]/g -> 알파벳 소문자 숫자 빼기 밑줄 마침표를 제외한 모든 문자를 제거
^ : 제외
\w : word를 표현. 알파벳 + 숫자 + _
- : [\w-_.] \w와 _.
g : Global - 문자열 내의 모든 패턴을 찾음

/\.{2,}/g -> 마침표(.)가 2번 이상 연속된 부분을 하나의 마침표로 변경
\. : .이 포함
{2,} : 2개 이상
g : Global - 문자열 내의 모든 패턴을 찾음

/^\.|\.$/g -> 마침표(.)가 처음 또는 끝에 위치
^\. : .으로 시작
\.$ : .으로 끝

/^$/ -> 빈 문자열

```

</p>
</details>

<br>
<br>

### 🎁 Basic

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 년월일

```javascript
[출처: https://velog.io/@jinjinhyojin/JavaScript-%EC%97%B0%EC%8A%B5-%EB%AC%B8%EC%A0%9C]
인자를 세개 받습니다.
첫번째 인자는 년도에 해당하는 숫자입니다.
두번째 인자는 월에 해당하는 숫자입니다.
세번째 인자는 일에 해당하는 숫자입니다.

년도 인자만 받았을 경우 → "1234년" 과 같은 형식의 문자열을 리턴 해주세요.
년도,월 인자를 받았을 경우 → 년도와 월을 조합해서 "1234년 5월" 과 같은 형식의 문자열을 리턴 해주세요.
년도,월,일 인자를 전부 받았을 경우 → 년도,월,일을 조합해서 "1234/5/6" 과 같은 형식의 문자열을 리턴 해주세요.

meetAt(2022); // 결과 --> "2022년"
meetAt(2032, 3); // 결과 --> "2032년 3월"
meetAt(1987, 10, 28); // 결과 --> "1987/10/28"


function meetAt(year, month, date){
  answer ='';
  return answer;
}

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//작성한 답
function meetAt(year, month, date) {
  if (year && month && date) {
    answer = year + "/" + month + "/" + date;
  } else if (year && month) {
    answer = year + "년 " + month + "월";
  } else {
    answer = year + "년";
  }
  return answer;
}

//작성자 답
function meetAt(year, month, date) {
  let todayYear = year;
  let todayMonth = month;
  let todayDate = date;

  if (todayDate) {
    return `${todayYear}/${todayMonth}/${todayDate}`;
  }
  if (todayMonth) {
    return `${todayYear}년 ${todayMonth}월`;
  }
  if (todayYear) {
    return `${todayYear}년`;
  }
}
// ✅ Date 를 먼저 해야만 하는 이유는 ?
// 위에서 아래로 계산하니까 빡빡한 조건을 위로 (정확한 조건 )
// if ()가 true라면, 진실이라면
```

</p>
</details>

<br>
<br>
