
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

#### 수진님 공유문제입니다.

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

<1> A+B 에서는 A가 문자열일 때 B를 문자열으로 인식하지만,
<2> A-B 에서는 A가 문자열이어도 숫자로 변환한다. 만약 A가 숫자로 변환이 되지 않는다면 NaN이 되어버린다.
```

 </p>
 </details>
 <br>
 <br>

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

#### ☁︎ 음양더하기

```javascript
// 문제 설명

어떤 정수들이 있습니다. 이 정수들의 절댓값을 차례대로 담은 정수 배열 absolutes와 이 정수들의 부호를 차례대로 담은 불리언 배열 signs가 매개변수로 주어집니다. 실제 정수들의 합을 구하여 return 하도록 solution 함수를 완성해주세요.

// 제한사항

absolutes의 길이는 1 이상 1,000 이하입니다.
absolutes의 모든 수는 각각 1 이상 1,000 이하입니다.
signs의 길이는 absolutes의 길이와 같습니다.
signs[i] 가 참이면 absolutes[i] 의 실제 정수가 양수임을, 그렇지 않으면 음수임을 의미합니다.

// 입출력 예

absolutes	  signs	              result
[4,7,12]    [true,false,true]	  9
[1,2,3]	    [false,false,true]	0

// 입출력 예 설명

입출력 예 #1
signs가 [true,false,true] 이므로, 실제 수들의 값은 각각 4, -7, 12입니다.
따라서 세 수의 합인 9를 return 해야 합니다.
입출력 예 #2
signs가 [false,false,true] 이므로, 실제 수들의 값은 각각 -1, -2, 3입니다.
따라서 세 수의 합인 0을 return 해야 합니다.
```

 <details><summary><b>Answer</b></summary>

   <p>

```javascript
function solution(absolutes, signs) {
  let answer = 0;

  absolutes.forEach((element, i) => {
    answer += signs[i] ? absolutes[i] : -absolutes[i];
  });

  return answer;
}
```

  </p>
  </details>
  <br>
  <br>

### 난이도 : 🌶🌶

<br>

#### ☁︎ 모의고사

```javascript
// 문제 설명

수포자는 수학을 포기한 사람의 준말입니다. 수포자 삼인방은 모의고사에 수학 문제를 전부 찍으려 합니다. 수포자는 1번 문제부터 마지막 문제까지 다음과 같이 찍습니다.

1번 수포자가 찍는 방식: 1, 2, 3, 4, 5, 1, 2, 3, 4, 5, ...
2번 수포자가 찍는 방식: 2, 1, 2, 3, 2, 4, 2, 5, 2, 1, 2, 3, 2, 4, 2, 5, ...
3번 수포자가 찍는 방식: 3, 3, 1, 1, 2, 2, 4, 4, 5, 5, 3, 3, 1, 1, 2, 2, 4, 4, 5, 5, ...

1번 문제부터 마지막 문제까지의 정답이 순서대로 들은 배열 answers가 주어졌을 때, 가장 많은 문제를 맞힌 사람이 누구인지 배열에 담아 return 하도록 solution 함수를 작성해주세요.

// 제한 조건

시험은 최대 10,000 문제로 구성되어있습니다.
문제의 정답은 1, 2, 3, 4, 5중 하나입니다.
가장 높은 점수를 받은 사람이 여럿일 경우, return하는 값을 오름차순 정렬해주세요.

// 입출력 예

answers: [1,2,3,4,5]	return: [1]
answers: [1,3,2,4,2]	return: [1,2,3]

// 입출력 예 설명

입출력 예 #1
수포자 1은 모든 문제를 맞혔습니다.
수포자 2는 모든 문제를 틀렸습니다.
수포자 3은 모든 문제를 틀렸습니다.
따라서 가장 문제를 많이 맞힌 사람은 수포자 1입니다.

입출력 예 #2
모든 사람이 2문제씩을 맞췄습니다.
```

 <details><summary><b>Answer</b></summary>

   <p>

```javascript
출처 : https://programmers.co.kr/learn/challenges

// 📌 반복을 적게하는 풀이

function solution(array) {
  var answer = [];
  let one = [1, 2, 3, 4, 5];
  let two = [2, 1, 2, 3, 2, 4, 2, 5];
  let three = [3, 3, 1, 1, 2, 2, 4, 4, 5, 5];

  let count1 = 0,
    count2 = 0,
    count3 = 0;

  for (let i = 0; i < array.length; i++) {
    if (array[i] == one[i % one.length]) {
      count1++;
    }
    if (array[i] == two[i % two.length]) {
      count2++;
    }
    if (array[i] == three[i % three.length]) {
      count3++;
    }
  }

  let high = Math.max(count1, count2, count3);

  if (high == count1) {
    answer.push(1);
  }
  if (high == count2) {
    answer.push(2);
  }
  if (high == count3) {
    answer.push(3);
  }

  return answer;
}

// 📌 변수 설정을 적게 하는 풀이

function solution(answers) {
  var answer = [];
  var a1 = [1, 2, 3, 4, 5];
  var a2 = [2, 1, 2, 3, 2, 4, 2, 5];
  var a3 = [3, 3, 1, 1, 2, 2, 4, 4, 5, 5];

  var a1c = answers.filter((a, i) => a === a1[i % a1.length]).length;
  var a2c = answers.filter((a, i) => a === a2[i % a2.length]).length;
  var a3c = answers.filter((a, i) => a === a3[i % a3.length]).length;
  var max = Math.max(a1c, a2c, a3c);

  if (a1c === max) {
    answer.push(1);
  }
  if (a2c === max) {
    answer.push(2);
  }
  if (a3c === max) {
    answer.push(3);
  }

  return answer;
}
```

  </p>
  </details>
  <br>
  <br>

### 난이도 : 🌶🌶

<br>

#### ☁︎ 기능개발 및 배포

```javascript
// 문제 설명

프로그래머스 팀에서는 기능 개선 작업을 수행 중입니다. 각 기능은 진도가 100%일 때 서비스에 반영할 수 있습니다.
또, 각 기능의 개발속도는 모두 다르기 때문에 뒤에 있는 기능이 앞에 있는 기능보다 먼저 개발될 수 있고, 이때 뒤에 있는 기능은 앞에 있는 기능이 배포될 때 함께 배포됩니다.
먼저 배포되어야 하는 순서대로 작업의 진도가 적힌 정수 배열 progresses와 각 작업의 개발 속도가 적힌 정수 배열 speeds가 주어질 때 각 배포마다 몇 개의 기능이 배포되는지를 return 하도록 solution 함수를 완성하세요.

// 제한 사항

작업의 개수(progresses, speeds배열의 길이)는 100개 이하입니다.
작업 진도는 100 미만의 자연수입니다.
작업 속도는 100 이하의 자연수입니다.
배포는 하루에 한 번만 할 수 있으며, 하루의 끝에 이루어진다고 가정합니다. 예를 들어 진도율이 95%인 작업의 개발 속도가 하루에 4%라면 배포는 2일 뒤에 이루어집니다.

// 입출력 예

progresses	              speeds	            return
[93, 30, 55]	            [1, 30, 5]	        [2, 1]
[95, 90, 99, 99, 80, 99]	[1, 1, 1, 1, 1, 1]	[1, 3, 2]
[95, 80, 99, 99, 90, 99]  [1, 1, 1, 1, 1, 1]  [1, 5]

// 입출력 예 설명

& 입출력 예 #1
첫 번째 기능은 93% 완료되어 있고 하루에 1%씩 작업이 가능하므로 7일간 작업 후 배포가 가능합니다.
두 번째 기능은 30%가 완료되어 있고 하루에 30%씩 작업이 가능하므로 3일간 작업 후 배포가 가능합니다. 하지만 이전 첫 번째 기능이 아직 완성된 상태가 아니기 때문에 첫 번째 기능이 배포되는 7일째 배포됩니다.
세 번째 기능은 55%가 완료되어 있고 하루에 5%씩 작업이 가능하므로 9일간 작업 후 배포가 가능합니다.
따라서 7일째에 2개의 기능, 9일째에 1개의 기능이 배포됩니다.

& 입출력 예 #2
모든 기능이 하루에 1%씩 작업이 가능하므로, 작업이 끝나기까지 남은 일수는 각각 5일, 10일, 1일, 1일, 20일, 1일입니다. 어떤 기능이 먼저 완성되었더라도 앞에 있는 모든 기능이 완성되지 않으면 배포가 불가능합니다.
따라서 5일째에 1개의 기능, 10일째에 3개의 기능, 20일째에 2개의 기능이 배포됩니다.
```

 <details><summary><b>Answer</b></summary>

   <p>

```javascript
출처 : https://programmers.co.kr/learn/challenges

// 📌 프로그래머스 1티어 풀이
function solution(progresses, speeds) {
    let answer = [0];
    let days = progresses.map((progress, index) => Math.ceil((100 - progress) / speeds[index]));
    let maxDay = days[0];

    for(let i = 0, j = 0; i< days.length; i++){
        if(days[i] <= maxDay) {
            answer[j] += 1;
        } else {
            maxDay = days[i];
            answer[++j] = 1;
        }
    }

    return answer;
}

```

 </p>
 </details>
 <br>
 <br>


### 🎁 If_and_switch

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 'if'를 '?'로 교체하기

```javascript
조건부 연산자 '?'를 이용해 if문이 사용된 아래 코드를 변형해보세요. 동작 결과는 동일해야 합니다.

let result;

let a = 1, b = 5;

if (a + b < 4) {
  result = '미만';
} else {
  result = '이상';
}
```

 <details><summary><b>Answer</b></summary>

   <p>

```javascript
let result;

let a = 1,
  b = 5;

result = a + b < 4 ? "미만" : "이상";
```

  </p>
  </details>
  <br>
  <br>

#### ☁︎ 'if..else'를 '?'로 교체하기

```javascript
조건부 연산자 '?'를 사용해 if..else문이 사용된 아래 코드를 변형해보세요. 동작 결과는 동일해야 합니다.

가독성을 위해 표현식을 여러 줄로 분할해 작성해 보시길 바랍니다.

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
