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
