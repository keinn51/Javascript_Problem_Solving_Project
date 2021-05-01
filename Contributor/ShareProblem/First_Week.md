# 1st Week Problem Sharing



## Keinn51

### 🎁 If & Switch



<br>



### 난이도 : 🌶



<br>



#### ☁︎ 프롬프트(prompt) 대화상자를 이용해 간이 로그인 창을 구현해보세요



```javascript





사용자가 "Admin"를 입력하면 비밀번호를 물어보는 프롬프트 대화상자를 띄워주세요. 



이때 아무런 입력도 하지 않거나 Esc를 누르면 "취소되었습니다."라는 메시지를 보여주세요. 



틀린 비밀번호를 입력했다면 "인증에 실패하였습니다."라는 메시지를 보여주세요.



비밀번호 확인 절차는 다음과 같습니다.



\- 맞는 비밀번호 "TheMaster"를 입력했다면 "환영합니다!"라는 메시지를 보여주세요.

\- 틀린 비밀번호를 입력했다면 "인증에 실패하였습니다."라는 메시지를 보여주세요.

\- 빈 문자열을 입력하거나 입력을 취소했다면 "취소되었습니다."라는 메시지를 보여주세요.





중첩 if 블록을 사용하고, 코드 전체의 가독성을 고려해 답안을 작성하세요.



힌트: 프롬프트 창에 아무것도 입력하지 않으면 빈 문자열인 ''가, ESC를 누르면 null이 반환됩니다.



```



<details><summary><b>Answer</b></summary>

<p>


```javasript

let Admin = prompt(`who's there?`);



if (Admin == 'Admin') {

 let Password = prompt('Password?');

 if (Password == 'TheMaster') {

  alert('Welcome!');

 }

 else if (Password == '' || Password == null) {

  alert('Cancleled');

 }

 else {

  alert('Wrong Password');

 }

}

else if (Admin == '' || Admin == null) {

 alert('Cancleled');

}

else {

 alert(`I don't know you`);

}

```



</p>

</details>

<br>

<br>



### 🎁 For And While



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



=> a에 1과 3이 더해지고, b=2 이므로 10 + 1 + 3 + 2 = 16

````



 </p>

 </details>

 <br>

 <br>


## joo-ju

### 🎁 Basic

  

<br>

  

### 난이도 : 🌶

  


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

### 🎁 For_and_While

  

<br>

  

### 난이도 : 🌶

  

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
 

