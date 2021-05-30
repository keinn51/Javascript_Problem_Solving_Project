# 5th Week Problem Sharing

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

```

</p>
</details>

<br>
<br>

### 🎁 Object

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 문제3: 행성 문제2

#### 우리 태양계를 이루는 행성은 수성, 금성, 지구, 화성, 목성, 토성, 천왕성, 해왕성이 있습니다.

#### 이 행성들의 영어 이름은 mercury, Venus, Earth, Mars, Jupiter, Saturn, Uranus, Neptune 입니다.

#### 행성의 한글 이름을 입력하면 영어 이름을 반환하는 프로그램을 만들어 주세요.

```javascript
//없음
```

<details><summary><b>Answer</b></summary>
<p>

```javascript

const planet = {
     '수성':'Mercury',
    '금성':'Venus',
    '지수':'Earth',
    '화성':'Mars',
    '목성':'Jupiter',
    '토성':'Saturn',
    '천왕성':'Uranus',
    '해왕성':'Neptune',

};

const pick = prompt('행성 이름 입력');
console.log(planet[pick]);


사용 개념: 객체(object)

객체형은 원시형과 달리 다향한 데이터를 담을수 있으며  '키 : 값' 으로 구성된다.
객체는 중괄호를 이용해 만들수 있고 중괄호 안에는 키(key):값(value) 쌍으로 구성된 프로퍼테(property)를
여러개 넣을 수 있는데, 키 에는 문자형, 값 에는 모든 자료형이 허용된다.

*생성 예시*

let user = {
    name : "John",
    age : 30
};


```

</p>
</details>

<br>
<br>

### 🎁 Object

<br>

### 난이도 : 🌶🌶

<br>

#### ☁︎ 문제4 : 객체 만들기

##### 첫번째 입력에서는 학생의 이름이 공백으로 구분되어 입력되고, 두 번째에는

##### 그 학생의 수학 점수가 공백으로 구분되어 주어집니다.

##### 두 개를 합쳐 학생의 이름이 key이고 value가 수학 점수인 객체를 출력해주세요.

```javascript

입력
Yujin Hyewon
70 100

출력
{'Yujin':70 , 'Hyewon' : 100}

```

<details><summary><b>Answer</b></summary>
<p>

```javascript
const name = prompt("이름").split(" ");
const score = prompt("점수").split(" ");
const obj = {};

for (let i = 0; i < name.length; i++) {
  obj[name[i]] = parseInt(score[i], 10);
}
console.log(obj);
```

</p>
</details>

<br>
<br>

### 🎁 Method

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 문제5 : 2-gram

##### 2-gram이란 문자열에서 2개의 연속된 요소를 출력하는 방법입니다.

##### 예를 들어 'Javascript'를 2-gram으로 반복해 본다면 다음과 같은 결과가 나옵니다.

##### 입력으로 문자열이 주어지면 2-gram으로 출력하는 프로그램을 작성해 주세요.

```javascript

입력
Javascript

출력
J a
a v
v a
a s
s c
c r
r i
i p
p t

```

<details><summary><b>Answer</b></summary>
<p>

```javascript
let str = prompt("문자열 입력");

for (let i = 0; i < str.length - 1; i++) {
  console.log(str[i], str[i + 1]);
}
```

</p>
</details>

<br>
<br>

### 🎁 Method

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 문제6 : 대문자만 지나가세요

##### 친구는 영어 학원 아르바이트를 하고 있습니다. 반 아이들은 알파벳을 공부하는 학생들인데 오늘은

##### 대분자 쓰기 시험을 봤습니다.

##### 알파벳 하나만을 입력하고 그 알파벳이 대문자이면 YES를 아니면 NO를 출력하는 프로그램을 만들어 주세요.

```javascript
// 없음
```

<details><summary><b>Answer</b></summary>
<p>

```javascript

const alpha = prompt('알파벳 입력');

if(alpha === alpha.toUpperCase()){
    console.log("YES");
}else{
    console.log("NO");
}


사용된 개념:
1. toUpperCase()
위 함수는 문자열을 대문자로 반환해서 반환한다.
ex). console.log('alphabet'.toUpperCase()); //'ALPHABET'

2. == vs ===

==(loose equality)

245 == '245' // return true
true == 1   // return true
undefined == null  // return true
'abc' == new String('abc')  // return true
'true' == true  // return true
true == 2   // return true



===(strict equality)

245 == '245' // return false
true == 1   // return false
undefined == null  // return false
'abc' == new String('abc')  // return false
```

</p>
</details>

<br>
<br>
