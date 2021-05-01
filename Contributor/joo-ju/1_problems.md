
  

### 🎁 Array

  

<br>

  

### 난이도 : 🌶

  

<br>

  

#### ☁︎ 배열의 삭제

  
  

```javascript

다음  배열에서  400, 500를  삭제하는  code를  입력하세요.

  

var  nums = [100, 200, 300, 400, 500];

  
  

````

  
  

<details><summary><b>Answer</b></summary>

  

<p>

  

```javascript

var nums = [100, 200, 300, 400, 500];

nums.pop();

nums.pop();

  

console.log(nums);

````

  

</p>

</details>

<br>

<br>


  

<br>

  

#### ☁︎ 배열의 내장함수

  
  

```javascript

<pass>부분에 배열 내장함수를 이용하여 코드를 입력하고 다음과 같이 출력되게 하세요.

  

데이터

var arr = [200, 100, 300];

//pass

console.log(arr);

  

출력

[200, 100, 10000, 300]

````

  
  

<details><summary><b>Answer</b></summary>

  

<p>

  

```javascript

var arr = [200, 100, 300];

arr.splice(2, 0, 10000);

console.log(arr);

````

  

</p>

</details>

<br>

<br>

### 🎁 For_and_While

  

<br>

  

### 난이도 : 🌶

  

<br>

  

#### ☁︎ for문 계산

  
  

```javascript

다음 코드의 출력 값으로 알맞은 것은?

  

var a = 10;

var b = 2;

  

for(var i=1; i<5; i+=2){

a += i;

}

  

console.log(a+b);

````

  
  

<details><summary><b>Answer</b></summary>

  

<p>

  

```javascript

16

````

  

</p>

</details>

<br>

<br>


<br>

  

#### ☁︎ 별 찍기

  
  

```javascript

크리스마스 날, 은비는 친구들과 함께 파티를 하기로 했습니다. 그런데, 크리스마스 트리를 사는 것을 깜빡하고 말았습니다. 온 가게를 돌아다녀 봤지만 크리스마스 트리는 모두 품절이었습니다.

하는 수 없이 은비는 프로그래밍으로 트리를 만들기로 합니다.

  

은비를 위해 프로그램을 작성해 주세요.

  

입력

5


출력
*
***
*****
*******
*********

  

````

  
  

<details><summary><b>Answer</b></summary>

  

<p>

  

```javascript

const n = prompt('숫자를 입력하세요.');

let tree = '';

  

for(let i=1; i<=n; i++){

let  star = '';

for(let  j=1; j<=n-i; j++){

star += ' ';

}

for(let k=1; k<=2*i-1; k++){

star += '*';

}

tree += star + '\n';

}

  
console.log(tree);

````
 

</p>

</details>

<br>

<br>

### 🎁 Basic

  

<br>

  

### 난이도 : 🌶

  

<br>

  

#### ☁︎ False

  
  

```javascript

다음은 자바스크립트 문법 중에서 False로 취급하는 것들 입니다.

앗, False로 취급하지 않는 것이 하나 있네요! **True를 찾아주세요.**

  

1) NaN

2) 1

3) ""

4) 0

5) undefined

  
  

````

  
  

<details><summary><b>Answer</b></summary>

  

<p>

  

```javascript

2) 1

````

  

</p>

</details>

<br>

<br>

<br>

  

#### ☁︎ 객체의 키 이름 중복

  
  

```javascript

자바스크립트 객체를 다음과 같이 만들었다.

출력값을 입력하시오. (출력값은 공백을 넣지 않습니다. )

  

var d = {

'height':180,

'weight':78,

'weight':84,

'temperature':36,

'eyesight':1

};

  

console.log(d['weight']);

  

````

  
  

<details><summary><b>Answer</b></summary>

  

<p>

  

```javascript

84

// 마지막 값을 출력한다.

````

  

</p>

</details>

<br>

<br>


<br>

  

#### ☁︎ concat을 활용한 출력방법

  
  

```javascript

다음 소스 코드를 완성하여 날짜와 시간을 출력하시오.

  

데이터

var year = '2019';

var month = '04';

var day = '26';

var hour = '11';

var minute = '34';

var second = '27';

  

var result = //빈칸을 채워주세요

  

console.log(result);

  
  

출력

2019/04/26 11:34:27

  
  

````

  
  

<details><summary><b>Answer</b></summary>

  

<p>

  

```javascript

var year = '2019';

var month = '04';

var day = '26';

var hour = '11';

var minute = '34';

var second = '27';

  

var result = year.concat('/', month, '/', day, ' ', hour, ':', minute, ':', second);

  

console.log(result);

````

  

</p>

</details>

<br>

<br>


