# dndbekfrl1's Problems

### π Basic

<br>

### λμ΄λ : πΆπΆ

<br>

#### βοΈ μ κ· μμ΄λ μΆμ²

```javascript
[μΆμ²:https://programmers.co.kr/learn/courses/30/lessons/72410]
μ κ· μ μ κ° μλ ₯ν μμ΄λλ₯Ό λνλ΄λ new_idκ° λ§€κ°λ³μλ‘ μ£Όμ΄μ§ λ, "λ€μ€"κ° μ€κ³ν 7λ¨κ³μ μ²λ¦¬ κ³Όμ μ κ±°μΉ νμ μΆμ² μμ΄λλ₯Ό return νλλ‘ solution ν¨μλ₯Ό μμ±ν΄ μ£ΌμΈμ.
(λ¬Έμ  μ€λͺμ΄ κΈΈμ΄μ μλ΅ν©λλ€! νλ‘κ·Έλλ¨Έμ€μμ νμΈν΄μ£ΌμΈμ)

function solution(new_id) {
    var answer = '';

    return answer;
}
```

<details><summary><b>Answer</b></summary>

<p>

```javascript
μ΄λ² λ¬Έμ λ‘ μ κ·μμ μμλ΄€μ΅λλ€.

λ€λ₯Έ μ¬λ νμ΄
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

λ€μ μ¬μ΄νΈμμ μ κ·μμ μ΄ν΄νκΈ° μ’μ΅λλ€.
[https://regexr.com/]

/[^\w-_.]/g -> μνλ²³ μλ¬Έμ μ«μ λΉΌκΈ° λ°μ€ λ§μΉ¨νλ₯Ό μ μΈν λͺ¨λ  λ¬Έμλ₯Ό μ κ±°
^ : μ μΈ
\w : wordλ₯Ό νν. μνλ²³ + μ«μ + _
- : [\w-_.] \wμ _.
g : Global - λ¬Έμμ΄ λ΄μ λͺ¨λ  ν¨ν΄μ μ°Ύμ

/\.{2,}/g -> λ§μΉ¨ν(.)κ° 2λ² μ΄μ μ°μλ λΆλΆμ νλμ λ§μΉ¨νλ‘ λ³κ²½
\. : .μ΄ ν¬ν¨
{2,} : 2κ° μ΄μ
g : Global - λ¬Έμμ΄ λ΄μ λͺ¨λ  ν¨ν΄μ μ°Ύμ

/^\.|\.$/g -> λ§μΉ¨ν(.)κ° μ²μ λλ λμ μμΉ
^\. : .μΌλ‘ μμ
\.$ : .μΌλ‘ λ

/^$/ -> λΉ λ¬Έμμ΄

```

</p>
</details>

<br>
<br>

### π Basic

<br>

### λμ΄λ : πΆ

<br>

#### βοΈ λμμΌ

```javascript
[μΆμ²: https://velog.io/@jinjinhyojin/JavaScript-%EC%97%B0%EC%8A%B5-%EB%AC%B8%EC%A0%9C]
μΈμλ₯Ό μΈκ° λ°μ΅λλ€.
μ²«λ²μ§Έ μΈμλ λλμ ν΄λΉνλ μ«μμλλ€.
λλ²μ§Έ μΈμλ μμ ν΄λΉνλ μ«μμλλ€.
μΈλ²μ§Έ μΈμλ μΌμ ν΄λΉνλ μ«μμλλ€.

λλ μΈμλ§ λ°μμ κ²½μ° β "1234λ" κ³Ό κ°μ νμμ λ¬Έμμ΄μ λ¦¬ν΄ ν΄μ£ΌμΈμ.
λλ,μ μΈμλ₯Ό λ°μμ κ²½μ° β λλμ μμ μ‘°ν©ν΄μ "1234λ 5μ" κ³Ό κ°μ νμμ λ¬Έμμ΄μ λ¦¬ν΄ ν΄μ£ΌμΈμ.
λλ,μ,μΌ μΈμλ₯Ό μ λΆ λ°μμ κ²½μ° β λλ,μ,μΌμ μ‘°ν©ν΄μ "1234/5/6" κ³Ό κ°μ νμμ λ¬Έμμ΄μ λ¦¬ν΄ ν΄μ£ΌμΈμ.

meetAt(2022); // κ²°κ³Ό --> "2022λ"
meetAt(2032, 3); // κ²°κ³Ό --> "2032λ 3μ"
meetAt(1987, 10, 28); // κ²°κ³Ό --> "1987/10/28"


function meetAt(year, month, date){
  answer ='';
  return answer;
}

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//μμ±ν λ΅
function meetAt(year, month, date) {
  if (year && month && date) {
    answer = year + "/" + month + "/" + date;
  } else if (year && month) {
    answer = year + "λ " + month + "μ";
  } else {
    answer = year + "λ";
  }
  return answer;
}

//μμ±μ λ΅
function meetAt(year, month, date) {
  let todayYear = year;
  let todayMonth = month;
  let todayDate = date;

  if (todayDate) {
    return `${todayYear}/${todayMonth}/${todayDate}`;
  }
  if (todayMonth) {
    return `${todayYear}λ ${todayMonth}μ`;
  }
  if (todayYear) {
    return `${todayYear}λ`;
  }
}
// β Date λ₯Ό λ¨Όμ  ν΄μΌλ§ νλ μ΄μ λ ?
// μμμ μλλ‘ κ³μ°νλκΉ λΉ‘λΉ‘ν μ‘°κ±΄μ μλ‘ (μ νν μ‘°κ±΄ )
// if ()κ° trueλΌλ©΄, μ§μ€μ΄λΌλ©΄
```

</p>
</details>

<br>
<br>

### π Basic

<br>

### λμ΄λ : πΆ

<br>

#### βοΈ μμνλ³

```javascript
[μΆμ²: JS100μ  41]

μ«μκ° μ£Όμ΄μ§λ©΄ μμμΈμ§ μλμ§ νλ³νλ νλ‘κ·Έλ¨μ μμ±ν΄μ£ΌμΈμ.
μμμ΄λ©΄ YESλ‘, μμκ° μλλ©΄ NOλ‘ μΆλ ₯ν΄μ£ΌμΈμ.
(μμ : 1κ³Ό μκΈ° μμ λ§μΌλ‘ λλμ΄λ¨μ΄μ§λ 1λ³΄λ€ ν° μμ μ μ)
```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//μμ±ν λ΅
μ κ³±κ·Ό μ΄μ©ν΄ νμ΄

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

//λ΅μ
const num = prompt("μ«μλ₯Ό μλ ₯νμΈμ.");

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

### π Basic

<br>

### λμ΄λ : πΆ

<br>

#### βοΈ 2020λ

```javascript
[μΆμ²: JS100μ  42]

2020λ 1μ 1μΌμ μμμΌμλλ€. 2020λ aμ bμΌμ λ¬΄μ¨ μμΌμΌκΉμ?
λ μ a, bλ₯Ό μλ ₯λ°μ 2020λ aμ bμΌμ΄ λ¬΄μ¨ μμΌμΈμ§ λ¦¬ν΄νλ ν¨μ solutionμ μμ±νμΈμ.
μμΌμ μ΄λ¦μ μΌμμΌλΆν° ν μμΌκΉμ§ κ°κ° SUN, MON, TUE, WED, THU, FRI, SAT μλλ€.

μλ₯Ό λ€μ΄ a = 5, b = 24λΌλ©΄ 5μ 24μΌμ μΌμμΌμ΄λ―λ‘ λ¬Έμμ΄ "SUN"λ₯Ό λ°ννμΈμ.

**μ ν μ‘°κ±΄**
2020λμ μ€λμλλ€.
2020λ aμ bμΌμ μ€μ λ‘ μλ λ μλλ€.
(13μ 26μΌμ΄λ 2μ 45μΌ κ°μ λ μ§λ μ£Όμ΄μ§μ§ μμ΅λλ€.)
```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//μμ±ν λ΅
function solution(month, day) {
  const week = ["SUN", "MON", "TUE", "WED", "THU", "RFI", "SAT"];
  const date = new Date();
  date.setYear(2020);
  date.setMonth(1);
  date.setDate(1);

  return week[date.getDay()];
}

//λ΅μ
const month = prompt("μμ μλ ₯νμΈμ.");
const date = prompt("μΌμ μλ ₯νμΈμ.");

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

### π Basic

<br>

### λμ΄λ : πΆ

<br>

#### βοΈ 10μ§μλ₯Ό 2μ§μλ‘

```javascript
[μΆμ²: JS100μ  43]

μ°λ¦¬κ° νν μ¬μ©νλ μ«μ 1, 8, 19, 28893 λ±λ±...μ 10μ§μ μ²΄κ³μλλ€.
μ΄λ₯Ό μ»΄ν¨ν°κ° μμ λ€μ μ μλ 2μ§μλ‘ λ°κΎΈλ €κ³  ν©λλ€. μ΄λ»κ² ν΄μΌν κΉμ?

μ¬μ©μμκ² μ«μλ₯Ό μλ ₯λ°κ³  μ΄λ₯Ό 2μ§μλ₯Ό λ°κΎΈκ³  κ·Έ κ°μ μΆλ ₯ν΄μ£ΌμΈμ.


```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//μμ±ν λ΅
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

let n = prompt("μ«μλ₯Ό μλ ₯νμΈμ");
solve(n);

//λ΅μ
let a = prompt("10μ§μλ₯Ό μλ ₯ν΄μ£ΌμΈμ.");
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

### π Basic

<br>

### λμ΄λ : πΆ

<br>

#### βοΈ κ° μλ¦¬μμ ν©

```javascript
[μΆμ²: JS100μ  44]
μ¬μ©μκ° μλ ₯ν μμ μ μμ κ° μλ¦¬μμ ν©μ κ΅¬νλ νλ‘κ·Έλ¨μ λ§λ€μ΄μ£ΌμΈμ

μλ₯Όλ€μ΄
18234 = 1+8+2+3+4 μ΄κ³  μ λ΅μ 18 μλλ€.
3849 = 3+8+4+9 μ΄κ³  μ λ΅μ 24μλλ€.

μμΆλ ₯

μλ ₯ : 18234
μΆλ ₯ : 18

μλ ₯ : 3849
μΆλ ₯ : 24

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//μμ±ν λ΅
function solution(n) {
  let answer = 0;
  while (n > 0) {
    answer += n % 10;
    n = Math.floor(n / 10);
  }
  console.log(answer);
}

let n = prompt("μ«μλ₯Ό μλ ₯νμΈμ");
solution(n);

//λ΅μ
let n = prompt("μ«μλ₯Ό μλ ₯νμΈμ.");
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
