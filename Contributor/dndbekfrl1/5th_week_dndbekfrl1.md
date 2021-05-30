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

### 🎁 Basic

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 소수판별

```javascript
[출처: JS100제 41]

숫자가 주어지면 소수인지 아닌지 판별하는 프로그램을 작성해주세요.
소수이면 YES로, 소수가 아니면 NO로 출력해주세요.
(소수 : 1과 자기 자신만으로 나누어떨어지는 1보다 큰 양의 정수)
```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//작성한 답
제곱근 이용해 풀이

function solution(num) {
  answer = "YES";
  if (num === 2) return answer;

  for (let i = 2; i < Math.floor(Math.sqrt(num)); i++) {
    if (num % i === 0) {
      answer = "No";
      return answer;
    }
  }
  return answer;
}

//답안
const num = prompt("숫자를 입력하세요.");

function check_prime(num) {
  for (let i = 2; i < num; i++) {
    const result = num % i;
    if (result === 0) {
      console.log("NO");
      return false;
    }
  }
  if (num === 1) {
    console.log("NO");
    return;
  }
  console.log("YES");
}

check_prime(num);
```

</p>
</details>

<br>
<br>

### 🎁 Basic

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 2020년

```javascript
[출처: JS100제 42]

2020년 1월 1일은 수요일입니다. 2020년 a월 b일은 무슨 요일일까요?
두 수 a, b를 입력받아 2020년 a월 b일이 무슨 요일인지 리턴하는 함수 solution을 완성하세요.
요일의 이름은 일요일부터 토요일까지 각각 SUN, MON, TUE, WED, THU, FRI, SAT 입니다.

예를 들어 a = 5, b = 24라면 5월 24일은 일요일이므로 문자열 "SUN"를 반환하세요.

**제한 조건**
2020년은 윤년입니다.
2020년 a월 b일은 실제로 있는 날입니다.
(13월 26일이나 2월 45일 같은 날짜는 주어지지 않습니다.)
```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//작성한 답
function solution(month, day) {
  const week = ["SUN", "MON", "TUE", "WED", "THU", "RFI", "SAT"];
  const date = new Date();
  date.setYear(2020);
  date.setMonth(1);
  date.setDate(1);

  return week[date.getDay()];
}

//답안
const month = prompt("월을 입력하세요.");
const date = prompt("일을 입력하세요.");

function solution(a, b) {
  const day = ["SUN", "MON", "TUE", "WED", "THU", "FRI", "SAT"];

  const x = new Date("2020-" + a + "-" + b);
  return day[x.getDay()];
}
console.log(solution(month, date));
```

</p>
</details>

<br>
<br>

### 🎁 Basic

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 10진수를 2진수로

```javascript
[출처: JS100제 43]

우리가 흔히 사용하는 숫자 1, 8, 19, 28893 등등...은 10진수 체계입니다.
이를 컴퓨터가 알아 들을 수 있는 2진수로 바꾸려고 합니다. 어떻게 해야할까요?

사용자에게 숫자를 입력받고 이를 2진수를 바꾸고 그 값을 출력해주세요.


```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//작성한 답
function solve(n) {
  let answer = [];
  let res = "";

  while (n > 0) {
    answer.push(n % 2);
    n = parseInt(n / 2);
  }
  answer.reverse();

  for (let i = 0; i < answer.length; i++) {
    res += answer[i];
  }
  return res;
}

let n = prompt("숫자를 입력하세요");
solve(n);

//답안
let a = prompt("10진수를 입력해주세요.");
let b = [];
let result = "";

while (a) {
  b.push(a % 2);
  a = parseInt(a / 2, 10);
}
b.reverse();

b.forEach((n) => {
  result += n;
});

console.log(result);
```

</p>
</details>

<br>
<br>

### 🎁 Basic

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 각 자리수의 합

```javascript
[출처: JS100제 44]
사용자가 입력한 양의 정수의 각 자리수의 합을 구하는 프로그램을 만들어주세요

예를들어
18234 = 1+8+2+3+4 이고 정답은 18 입니다.
3849 = 3+8+4+9 이고 정답은 24입니다.

입출력

입력 : 18234
출력 : 18

입력 : 3849
출력 : 24

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//작성한 답
function solution(n) {
  let answer = 0;
  while (n > 0) {
    answer += n % 10;
    n = Math.floor(n / 10);
  }
  console.log(answer);
}

let n = prompt("숫자를 입력하세요");
solution(n);

//답안
let n = prompt("숫자를 입력하세요.");
let sum = 0;

while (n !== 0) {
  sum += n % 10;
  n = Math.floor(n / 10);
}

console.log(sum);
```

</p>
</details>

<br>
<br>
