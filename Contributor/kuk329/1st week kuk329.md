# 1st Week Problem Sharing

## by kuk329

### 🎁 array

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 문제1: 배열의 삭제

##### 다음 배열에서 400, 500를 삭제하는 code를 입력하세요.

```javascript
var nums = [100, 200, 300, 400, 500];
```

<details><summary><b>Answer</b></summary>
<p>

```javascript
const result=nums.splice(3,2);
console.log(nums); // [100,200,300]
console.log(result); // [400,500]

사용된 개념: splice()함수
splice() 메서드는 배열의 기존 요소를 삭제 또는 교체 또는 새 요소를 추가해서 배열의 내용을 변경한다.
첫번째 인자에는 변경할 값이 들어있는 인덱스 시작 번호를 넣어주고 ,
두번째 인자에는 삭제할 값의 갯수를 넣어준다. (option)
배열에 추가할 값이 있으면 그 값을 인자로 계속 넣어주면된다. (option)
반환값의 경우 제거한 요소를 담은 배열이 반환된다.


+ 추가
pop()을 이용하는 방법도 가능. 단 pop()은 배열의 가장 끝에있는 값부터 제거하기 때문에 두번 해줘야됨.
var nums = [100,200,300,400,500];
nums.pop(); // [100,200,300,400]
nums.pop(); // [100,200,300]

```

</p>
</details>

<br>
<br>

### 🎁 array

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 문제2: 배열의 내장함수

##### pass 부분에 배열 내장함수를 이용하여 코드를 입력하고 다음과 같이 출력되게 하세요.

```javascript
var arr = [200, 100, 300];
//pass
console.log(arr);

출력[(200, 100, 10000, 300)];
```

<details><summary><b>Answer</b></summary>
<p>

```javascript
arr.splice(2, 0, 10000);
console.log(arr);

출력[(200, 100, 10000, 300)];
```

</p>
</details>

<br>
<br>

### 🎁 Variable

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 문제3: 변수의 타입

##### 다음 출력으로 올바른 것은?

```javascript
var arr = [100,200,300];
console.log(typeof(arr));

1) undefined
2) string
3) number
4) object

```

<details><summary><b>Answer</b></summary>
<p>

```javascript
4) object

개념 :
자바스크립트에는 7개의 기본 타입과 object 타입이 있다.

기본타입
Boolean,Null,undefined,Number,String,Symbol

object 타입
컴퓨터 과학에서, 객체는 식별자로 참조할수 있는, 메모리에 있는 값이다.
배열(array)은 정수키를 가지는 일련의 값들을 표현하기 위한 object이다.

```

</p>
</details>

<br>
<br>

### 🎁 Method

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 문제4 : concat을 활용한 출력 방법

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

### 🎁 ddd

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 문제5 :

#####

```javascript

```

<details><summary><b>Answer</b></summary>
<p>

```javascript

```

</p>
</details>

<br>
<br>

### 🎁 ddd

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 문제6

#####

```javascript

```

<details><summary><b>Answer</b></summary>
<p>

```javascript

```

</p>
</details>

<br>
<br>
