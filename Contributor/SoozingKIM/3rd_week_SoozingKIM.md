# SoozingKIM's Problems

### 🎁 Basic

 <br>

### 난이도 : 🌶

 <br>

#### ☁︎ let 변수선언

```javascript
admin과 user이라는 변수를 선언하세요.
user에 값으로 "John"을 할당해 보세요.
user의 값을 admin에 복사해 보세요.
admin의 값을 alert 창에 띄워보세요. "John"이 출력되어야 합니다.
```

 <details><summary><b>Answer</b></summary>
 <p>

```javascript
let admin, user;
user = "John";
admin = user;
alert(user);
```

 </p>
 </details>
 <br>
 <br>

### 🎁 Basic

 <br>

### 난이도 : 🌶

 <br>

#### ☁︎ const 상수 (대문자상수)

```javascript
아래 코드를 평가해 보시기 바랍니다.
const birthday = '18.04.1982';
const age = someCode(birthday);
위 코드의 상수 birthday는 태어난 날짜 정보를 담고 있습니다.
age라는 상수는 나이에 관한 값을 담고 있는데 birthday를 조작하여 그 값을 도출합니다.
(생일을 이용하여 나이를 도출하는 코드는 간결성을 위해 여기선 언급하지 않겠습니다. 이 문제에서 해당 코드가 중요한 역할을 하지 않기도 합니다)
이런 상황에서 birthday를 대문자 상수로 바꾸는 것이 적절할까요?
age 역시 대문자 상수로 바꾸는 것이 괜찮은 선택일까요?
```

 <details><summary><b>Answer</b></summary>
 <p>
  
 ```javascript
 BIRTHDAY는 괜찮지만, age는 소문자가 좋다.
 태어난 날짜는 변하지 않지만 나이는 매년 변하기 때문!
 ```
 </p>
 </details>
 <br>
 <br>

 ### 🎁 Basic
 <br>

 ### 난이도 : 🌶
 <br>

 #### ☁︎ 문자열 출력
 ```javascript
 아래 스크립트의 결과를 예측해 보세요.
 let name = "Ilya";
 alert( `hello ${1}` ); 
 alert( `hello ${"name"}` ); 
 alert( `hello ${name}` ); 
 ````
 <details><summary><b>Answer</b></summary>
 <p>
  
 ```javascript
 hello 1
 hello name
 hello Ilya
 => `` (백틱) 안에 있는 문자열에 ${}를 이용해 속에 변수명을 넣으면 변수가 가지고 있는 값을 출력한다.
 ```
 </p>
 </details>
 <br>
 <br>


 ### 🎁 Basic
 <br>

 ### 난이도 : 🌶
 <br>

 #### ☁︎ prompt 사용하기
 ```javascript
 사용자에게 이름을 물어보고, 입력받은 이름을 그대로 출력해주는 페이지를 만들어 보세요.
 ````
 <details><summary><b>Answer</b></summary>
 <p>
  
 ```javascript
 let user = prompt('사용자의 이름을 입력해주세요.','');
 alert( `입력된 이름은 '${user}' 입니다.`);
 => prompt 는 사용자가 입력한 값을 문자열로 반환하기 때문에 그걸 담아줄 변수와 함께 사용한다.
 ```
 </p>
 </details>
 <br>
 <br>

 ### 🎁 Basic
 <br>

 ### 난이도 : 🌶
 <br>
 
 #### ☁︎ 단항연산자 '+'
 ```javascript
 아래 코드는 사용자에게 숫자 2개를 입력받은 다음 그 합을 보여줍니다.
 그런데 의도한대로 동작하지 않습니다. 
 프롬프트 창에 세팅한 기본값을 수정하지 않은 경우 덧셈의 결과는 12가 됩니다.
 왜 그럴까요? 예시가 제대로 동작하도록 코드를 수정해보세요. 결과는 3이 되어야 합니다.
 let a = prompt("덧셈할 첫 번쨰 숫자를 입력해주세요.", 1);
 let b = prompt("뎃셈할 두 번째 숫자를 입력해주세요.", 2);
 alert(a+b);
 ````
 <details><summary><b>Answer</b></summary>
 <p>
  
 ```javascript
 입력된 1 과 2 는 문자열로 인식이 된다. 따라서 1+2 는 12 가 되어 출력이 된 것이다.
 이것을 숫자형으로 변환시키기 위해서는 '+' 단항연산자를 이용한 두 가지 방법이 존재한다.
 첫번째)
 let a = prompt("덧셈할 첫 번쨰 숫자를 입력해주세요.", 1);
 let b = prompt("뎃셈할 두 번째 숫자를 입력해주세요.", 2);
 alert(+a + +b);
 두번째)
 let a = +prompt("덧셈할 첫 번쨰 숫자를 입력해주세요.", 1);
 let b = +prompt("뎃셈할 두 번째 숫자를 입력해주세요.", 2);
 alert(a+b);
 ```

 </p>
 </details>
 <br>
 <br>

### 🎁 Basic

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
```

 </p>
 </details>
 <br>
 <br>
