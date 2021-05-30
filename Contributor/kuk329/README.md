
### 🎁 Basic

#### ☁︎ 문제: 다음 코드의 출력값을 예측해 보세요.

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

#### ☁︎ 문제: 다음 2개의 변수에 저장된 값들을 숫자형으로 만들어서 더해보세요.

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

### 🎁 Method

<br>

#### ☁︎ 문제 : 2-gram

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

#### ☁︎ 문제 : 대문자만 지나가세요

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


#### ☁︎ 문제 : concat을 활용한 출력 방법

##### 다음 소스 코드를 완성하여 날짜와 시간을 출력하시오.

```javascript
데이터
var year = '2021';
var month = '05';
var day = '15';
var hour = '11';
var minute = '15';
var second = '20';

var result = // 빈칸을 채워주세요

console.log(result);

출력
2021/05/15 11:15:20


```

<details><summary><b>Answer</b></summary>
<p>

```javascript


var result =  year.concat('/').concat(month).concat('/').concat(day).concat(' ').concat(hour).concat(':').concat(minute).concat(':').concat(second);

개념 :
concat() 메서드는 매개변수로 전달된 문자열을 메서드를 호출한 문자열에 붙여서 새로운 문자열을 반환한다.

```

</p>
</details>

<br>
<br>



