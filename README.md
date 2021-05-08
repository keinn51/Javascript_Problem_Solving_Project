![무제](https://user-images.githubusercontent.com/79993356/115105256-bbd3d700-9f98-11eb-9eac-0c6b1a04de21.png)


<br>

### 문제의 순서

<br>

<b>Basic ➤ Method ➤ If_and_switch ➤ Continue_and_Break ➤ For_and_While ➤ Function ➤ String_and_Object ➤ array ➤ This ➤ Promise</b>

<br>

### 문제는 어디서 왔는가

프론트 엔드 입문 공부를 하려고 한 학생들..

코딩테스트 대비 문제는 많은데... Javscipt 개념을 공부할 만한 문제가 너무 없다!

그래서 만든, Javascipt 문제를 모아와 만든 페이지입니다🙌

바로 이 곳에서 모아 왔습니다. (이외에도 다수의 블로그에서 출처하였습니다😗)

<br>

<a href="https://ko.javascript.info"><b>Javascript.info</b></a>

= 모던 JavaScript 튜토리얼은 상세한 설명과 함께 JavaScript 기본 개념 및 고급 개념을 다루는 홈페이지. Javascript의 기본 개념을 알 수 있으며, 간단한 문제도 풀어볼 수 있다.

<a href="https://github.com/dream-ellie/learn-javascript"><b>Ellie's note</b></a>

= 킹갓 엘리님의 수업과 함께 써내려간 노트를 모아둔 페이지. 이 페이지만 참고하는 것보다, 엘리님의 강의를 같이 들으면서 노트를 본다면 👍 (유튜브에 드림코딩 검색!)

<a href="https://www.notion.so/JS-100-94d97d294dd14c9b911a02c840fa9f2d"><b>Notion Java Problem 100</b></a>

= Javascript의 문제(거의 100문제)를 풀어볼 수 있는 페이지. 사회에 공헌하며 미래를 꿈꾸는 아이들 가르치며 소박하게 살고싶다는 저자님이 만드셨다. 좋은 사이트이지만 공부 분야별로 구분되어 있지 않다는 단점이 있다. 

<a href="https://github.com/lydiahallie/javascript-questions/blob/master/ko-KR/README-ko_KR.md">JavaScript 질문 목록</a>

= "초급부터 고급까지: JavaScript를 얼마나 잘 알고 있는지 테스트하거나, 지식을 조금 더 새롭게 하거나, 코딩 면접을 준비하세요!" 라는 취지의 문제 프로젝트. 이번 프로젝트를 만드는 데의 모토가 되었다!

<br>

분야 별로 문제가 구분되어 있고, 간단히 클릭하면 펼칠 수 있어요! 정답은 절대적이지 않아서 여러분들이 푼 게 맞을 수도 있습니다🙏

도움이 되셨으면 좋겠어요😄




<br>

### 난이도의 의미

🌶 : 

🌶🌶 : 

🌶🌶🌶 : 

<br>

---

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



2



=> 숫자 1은 true를 나타낸다.



````



 </p>

 </details>

 <br>

 <br>
 
 
 ### 🎁 If_and_Switch


<br>

### 난이도 : 🌶

<br>

#### ☁︎ 프롬프트(prompt) 대화상자를 이용해 간이 로그인 창을 구현해보세요

```javascript


사용자가 "Admin"를 입력하면 비밀번호를 물어보는 프롬프트 대화상자를 띄워주세요. 

이때 아무런 입력도 하지 않거나 Esc를 누르면 "취소되었습니다."라는 메시지를 보여주세요. 

틀린 비밀번호를 입력했다면 "인증에 실패하였습니다."라는 메시지를 보여주세요.

비밀번호 확인 절차는 다음과 같습니다.

- 맞는 비밀번호 "TheMaster"를 입력했다면 "환영합니다!"라는 메시지를 보여주세요.
- 틀린 비밀번호를 입력했다면 "인증에 실패하였습니다."라는 메시지를 보여주세요.
- 빈 문자열을 입력하거나 입력을 취소했다면 "취소되었습니다."라는 메시지를 보여주세요.


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

=> a에 1과 3이 더해지고, b=2 이므로 10 + 1 + 3 + 2 = 16
````

 </p>
 </details>
 <br>
 <br>

### 🎁 Function

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 자기소개


```javascript

신학기가 시작되고, 아이들이 돌아가면서 자기소개를 하기로 했습니다.

만약 입력으로 `김다정`이라는 이름이 주어지면 "안녕하세요. 저는 김다정입니다."라고 출력하게
해주세요.

**입출력**

입력 : 김다정
출력 : 안녕하세요. 저는 김다정입니다.

````

<details>
<summary><b>Answer</b></summary>

<p>

```javascript

function Introduce(name) {
 return console.log(`안녕하세요. 저는 ${name}입니다.`)
}

Introduce('김다정')

````

</p>
</details>
<br>
<br>

### 🎁 Array


<br>

### 난이도 : 🌶

<br>

#### ☁︎ 배열의 삭제

```javascript

다음 배열에서 400, 500를 삭제하는 code를 입력하세요.

var nums = [100, 200, 300, 400, 500];

```

<details><summary><b>Answer</b></summary>
  <p>

```javascript
var nums = [100, 200, 300, 400, 500];
nums.splice(3, 2);
console.log(nums);
```

 </p>
 </details>
 <br>
 <br>
 
 #### ☁︎ 배열의 내장함수

 ```javascript

 <pass>부분에 배열 내장함수를 이용하여 코드를 입력하고 다음과 같이 출력되게 하세요.

 ***데이터***

 var arr = [200, 100, 300];

 //pass

 console.log(arr);


 ***출력***

 [200, 100, 10000, 300]

 ```

 <details><summary><b>Answer</b></summary>

   <p>

 ```javascript
 var arr = [200, 100, 300];

 arr.splice(2, 0, 10000);

 console.log(arr);
 ```

  </p>
  </details>
  <br>
  <br>
