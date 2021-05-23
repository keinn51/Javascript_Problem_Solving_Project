# 2st Week Problem Sharing

## by kuk329

### 🎁 Method

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 문제1: 몇 번째 행성인가요?

##### 우리 태양계를 이루고 있는 행성은 수성, 금성, 지구, 화성, 목성 , 토성, 천왕성, 해왕성으로 총 8개 입니다.

##### 저희는 우리 태양계의 n번째 행성이 무엇인지 알고싶습니다.

##### 입력으로 행성의 순서를 나타내는 숫자 n이 입력됩니다. 출력으로 그 순서에 해당하는 행성의 이름을 출력해 주세요.

##### 예를들어 1이 입력되면, 첫번째 행성인 수성이 출력됩니다.

```javascript
입출력;
입력: 1;
출력: 수성;
```

<details><summary><b>Answer</b></summary>
<p>

```javascript
const planet = ['0','수성','금성','지구','화성','목성','토성','천왕성','해왕성']
const num = alert('입력(1~8):')
console.log(planet[Number(num)]);


사용된 개념: prompt 함수 & 형변환

->prompt 함수
브라우저에서 제공하는 함수로 인자는 두개를 받을수 있다.
ex) result = prompt(title,[default])
함수가 실행되면 텍스트 메시지와 입력 필드, 확인 및 취소 버튼이 있는 모달창을 띄워준다.
title 은 사용자에게 보여줄 문자열을 입력하면 된다.
default 는 입력 필드의 초기값을 넣어주면 되지만 필수는 아니다.

->형변환
전달받은 값을 적절한 자료형으로 바꾸어주는걸 형 변환(type conversion)이라고 한다.
문자형으로 변환-String(value) , 숫자형으로 변환-Number(value), 불린형으로 변환-Boolean(value) 가 있다.




```

</p>
</details>

<br>
<br>

### 🎁 If_and_switch

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 문제2: 3의 배수 인가요?

##### 영희는 친구와 게임을 하고 있습니다. 서로 돌아가며 랜덤으로 숫자를 하나 말하고 그게 3의 배수이면 박수를 치고 아니면 그 숫자를 그대로 말하는

##### 게임입니다. 입력으로 랜덤한 숫자 n이 주어집니다.

##### 만약 그수가 3의 배수라면 '짝'이라는 글자를, 3의 배수가 아니라면 n을 그대로 출력해주세요.

```javascript
입출력;

입력: 3;
출력: 짝;

입력: 2;
출력: 2;
```

<details><summary><b>Answer</b></summary>
<p>

```javascript
const num = Number(prompt("아무 숫자 입력: "));
if (num % 3 == 0) {
  console.log("짝");
} else {
  console.log(num);
}
```

</p>
</details>

<br>
<br>

### 🎁 Method

<br>

### 난이도 : 🌶🌶

<br>

#### ☁︎ 문제3: 로꾸꺼

##### 문장이 입력되면 거꾸로 출력하는 프로그램을 만들어 봅시다.

```javascript
입출력;

입력: 거꾸로;
출력: 로꾸거;
```

<details><summary><b>Answer</b></summary>
<p>

```javascript
function reverse(str){
    let newStr="";
    for(let i = str.length-1; i>=0; i--){
        newStr+=str[i];
    }
    console.log(newStr);
}

reverse("거꾸로")

사용된 개념: 함수
자바스크립트 에서는 함수를 선언할때 function 함수이름(매개변수,...){ 수행할 문장들... }
이렇게 만든다.

+ 추가 답변
const n = prompt('입력하세요.');
const reverseString = n.split('').reverse().join('');
console.log(reverseString);
*split() 메서드는 문자열을 배열로 만들어 반환하고,
reverse()메서드는 배열의 순서를 반전하며,
join() 메서드는 원소를 모두 붙여 문자열로 반환한다.

```

</p>
</details>

<br>
<br>

### 🎁 For_and_While

<br>

### 난이도 : 🌶🌶

<br>

#### ☁︎ 문제4 : 평균 점수

##### 영하네 반은 국어, 수학, 영어 시험을 보았습니다. 영하는 친구들의 평균 점수를 구해주기로 했습니다.

##### 공백으로 구분하여 세 과목의 점수가 주어지면 전체 평균 점수를 구하는 프로그램을 작성하세요.

##### 단, 소수점 자리는 모두 버립니다.

```javascript

입출력

입력: 20 30 40
출력: 30

```

<details><summary><b>Answer</b></summary>
<p>

```javascript
const numList = prompt('과목 3개 점수를 입력하세요 : ').split(' ');
let sum = 0;
for(let i = 0 ; i<3; i++>){
    sum+=parseInt(scores[i],10); // 십진수의 형태의 숫자로 데이터 타입을 변환합니다.
}
console.log(Math.floor(sum/3)); //Math.floor 메서드는 소수점 자리를 모두 버림합니다.

사용된 개념:
parseInt(string, radix(option)) 함수는 첫번째 인자를 문자열로 변환하고 파싱하고,
그 문자열을 파싱하여 정수나 NaN을 리턴한다.
radix는 string이 표현하는 정수를 나타내는 2와 36사이의 진수를 넣는다.

Math.floor() 함수는 주어진 숫자와 같거나 작은 정수 중에서 가장 큰 수를 반환한다.

```

</p>
</details>

<br>
<br>

### 🎁 Method

<br>

### 난이도 : 🌶🌶

<br>

#### ☁︎ 문제5 : 제곱을 구하자

##### 공백으로 구분하여 두 숫자 a와b가 주어지면, a의 b승을 구하는 프로그램을 작하세요.

```javascript
// 없음
```

<details><summary><b>Answer</b></summary>
<p>

```javascript
let n = prompt("두 수를 입력하세요:").split(" ");
console.log(Math.pow(parseInt(n[0], 10), parseInt(n[1], 10)));
```

</p>
</details>

<br>
<br>

### 🎁 Method

<br>

### 난이도 : 🌶🌶

<br>

#### ☁︎ 문제6 : 몫과 나머지

##### 공백으로 구분하여 두 숫자가 주어집니다.

##### 두 번째 숫자로 첫번째 숫자를 나누었을 때 그 몫과 나머지를 공백으로 구분하여 출력하세요s

```javascript
입출력

입력: 10 2
출력: 5 0


```

<details><summary><b>Answer</b></summary>
<p>

```javascript
const num = prompt('두 숫자 입력':).split(' ');
const a=parseInt(num[0],10)
const b=parseInt(num[1],10)
const result = a/b;
const remain = a % b;
console.log(result,remain)

```

</p>
</details>

<br>
<br>
