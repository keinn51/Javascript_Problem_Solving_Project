# SoozingKIM's Problems

### 🎁 Basic

 <br>

### 난이도 : 🌶

 <br>

#### ☁︎ 비교 연산자

```javascript
아래 표현식들의 결과를 예측해보세요.

1)  5 > 4
2)  "apple" > "pineapple"
3)  "2" > "12"
4)  undefined == null
5)  undefined === null
6)  null == "\n0\n"
7)  null === +"\n0\n" 
```

 <details><summary><b>Answer</b></summary>
 <p>

```javascript
1)  true
2)  false   -> 사전순 비교
3)  true    -> 숫자인듯 하지만 문자열이므로 사전순 비교
4)  true    -> == 비교에서 undefined 와 null 은 같다.
5)  false   -> === 비교에서는 다르면 무조건 다르다.
6)  false   -> == 비교에서 null 은 무조건 undefined 와만 같다.
7)  false   -> === 비교에서는 다르면 무조건 다르다.
```

 </p>
 </details>
 <br>
 <br>


 ### 🎁 Basic
 <br>

 ### 난이도 : 🌶 🌶
 <br>

 #### ☁︎ 논리 연산자
 ```javascript
아래 코드의 결과를 예측해 보세요.

alert( alert(1) || 2 || alert(3) );
alert( alert(1) && alert(2) );

 ````
 <details><summary><b>Answer</b></summary>
 <p>
  
 ```javascript
alert(1)에 의해 1 창이 뜨고, 2 가 참이므로 2 가 뜬 후 문장 종료.
alert(1)에 의해 1 창이 뜨고, alert()는 undefined를 반환하므로 flasy라 문장 종료.
 ```
 </p>
 </details>
 <br>
 <br>

### 🎁   If_and_Switch

 <br>

### 난이도 : 🌶🌶

 <br>

#### ☁︎ 조건문

```javascript
if..else 구조를 이용해 "자바스크립트의 ‘공식’ 이름은 무엇일까요?"라는 질문을 하는 코드를 작성해 보세요.
사용자가 'ECMAScript’를 입력했다면 ‘정답입니다!’, 아니라면 '모르셨나요? 정답은 ECMAScript입니다!'라는 메시지를 보여주세요.
```

 <details><summary><b>Answer</b></summary>
 <p>
  
 ```javascript
let question = prompt("자바스크립트의 '공식' 이름은 무엇일까요?", '');
if (question=='ECMAScript'){
    alert('정답입니다.');
}
else{
    alert( '모르셨나요? 정답은 ECMAScript입니다!');
}
 ```
 </p>
 </details>
 <br>
 <br>


 ### 🎁 If_and_Switch
 <br>

 ### 난이도 : 🌶 🌶
 <br>
 
 #### ☁︎ 조건문과 논리 연산자
 ```javascript
아래 표현식에서 어떤  alert가 실행될까요? 

if( -1||0 ) alert( 'first');
if( -1&&0 ) alert( 'second' );
if(null||-1&&1) alert( 'third' );
 ````
 <details><summary><b>Answer</b></summary>
 <p>
  
 ```javascript
0은 거짓, 다른 숫자는 다 참이다.
-1 || 0     은 true
-1 && 0     은 false
null||true  는 trye
따라서 'first', 'third' 실행됨.
 ```

 </p>
 </details>
 <br>
 <br>


 ### 🎁 If_and_Switch
 <br>

 ### 난이도 : 🌶 🌶 🌶
 <br>

 #### ☁︎ 간이 로그인 창 구현하기
 ```javascript
프롬프트(prompt) 대화상자를 이용해 간이 로그인 창을 구현해보세요.
사용자가 "Admin"를 입력하면 비밀번호를 물어보는 프롬프트 대화상자를 띄워주세요.
이때 아무런 입력도 하지 않거나 Esc를 누르면 "취소되었습니다."라는 메시지를 보여주세요. 
틀린 비밀번호를 입력했다면 "인증에 실패하였습니다."라는 메시지를 보여주세요.

- 비밀번호 확인 절차는 다음과 같습니다.
맞는 비밀번호 "TheMaster"를 입력했다면 "환영합니다!"라는 메시지를 보여주세요.
틀린 비밀번호를 입력했다면 "인증에 실패하였습니다."라는 메시지를 보여주세요.
빈 문자열을 입력하거나 입력을 취소했다면 "취소되었습니다."라는 메시지를 보여주세요.
 ````
 <details><summary><b>Answer</b></summary>
 <p>
  
 ```javascript
let user = prompt("사용자를 입력하세요.",'');
if( user=="Admin"){
    let password = prompt("비밀번호를 입력하세요.",'');
    if (password=="TheMaster"){
        alert("환영합니다!");
    }else if(password==""||password==null){
        alert("취소되었습니다.");
    }else{
        alert("인증에 실패하였습니다.");
    }
}else if(user==" "||user==null){
    alert("취소되었습니다..");
}else{
    alert("인증에 실패하였습니다.");
}
 ```
 </p>
 </details>
 <br>
 <br>

### 🎁 For_and_While

 <br>

### 난이도 : 🌶🌶🌶

 <br>

#### ☁︎ 프롬프트 창 구현하기

```javascript
사용자가 100보다 큰 숫자를 입력하도록 안내하는 프롬프트 창을 띄워보세요.
사용자가 조건에 맞지 않은 값을 입력한 경우 반복문을 사용해 동일한 프롬프트 창을 띄워줍시다.

사용자가 100을 초과하는 숫자를 입력하거나 취소 버튼을 누른 경우, 
혹은 아무것도 입력하지 않고 확인 버튼을 누른 경우엔
더는 프롬프트 창을 띄워주지 않아도 됩니다.

사용자가 오직 숫자만 입력한다고 가정하고 답안을 작성하도록 해봅시다.
숫자가 아닌 값이 입력되는 예외 상황은 처리하지 않아도 됩니다.


<details><summary><b>Answer</b></summary>
 <p>

```javascript
----- 정답 예시 1번 -----

let num = 0;
while( num<=100 ){
    num = prompt( "100보다 큰 숫자를 입력하세요.", '' );
    if( !num ) break;
}

----- 정답 예시 2번 -----

let num;
do{
    num = prompt( "100보다 큰 숫자를 입력하세요.", '' );
}while( num<=100 && num );

-> num이 빈 값이거나 null 일 경우 falsy 이므로 && 연산시 false가 반환되어 반복문 나감.

```

 </p>
 </details>
 <br>
 <br>
