# 2nd Week Problem Sharing

## Keinn51

### 🎁 Variable

<br>

### 난이도 : 🌶

<br>

#### ☁︎ Var & Let (2)

```javascript
// 무엇이 출력될까요?

for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1);
}

for (let i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1);
}
```

- A: `0 1 2` 그리고 `0 1 2`
- B: `0 1 2` 그리고 `3 3 3`
- C: `3 3 3` 그리고 `0 1 2`

<details><summary><b>Answer</b></summary>
  <p>

#### 정답: C

<a href="https://developer.mozilla.org/ko/docs/Web/API/WindowOrWorkerGlobalScope/setTimeout">개념 참고 사이트1 </a>

<a href=" https://www.bangseongbeom.com/javascript-var-let.html#fn:create-per-iteration-environment">개념 참고 사이트2</a>

<br>
<b>setTimeout 기본 구문</b>
=> window.setTimeout(function, milliseconds);
=> milliseconds후에 function을 호출하겠다!
<br>

첫 번째의 루프 변수 `i`는 `var` 키워드를 사용해 선언되어 있기 때문에, 이 값은 <b>전역 변수</b>가 됩니다.

루프 동안, 단항 연산자 `++`를 사용하여, 매번 `i`의 값을 `1`씩 증가했어요. 그러니까 세 번의 setTimeout을 통해 1밀리초 뒤에 console을 세 번 실행할 때에는, 루프를 이미 세 번 돌았기 때문에 i는 3이 되어 있는 거에요.

두 번째 루프에서, 변수 `i`는 `let` 키워드를 사용해 선언되었어요: `let`(그리고 `const`) 키워드로 선언된 변수는 블록 범위예요(블록은 `{ }` 사이의 모든 것). 여기서 가장 중요한 건, 이 때의 let은 각각의 반복 동안, `i`는 새로운 값이라는 거에요.

i=0, i=1, i=2 라고 할 때 각각의 i는 새로운 i라는 거죠. var에서 전역변수 i를 설정해주고 이 값을 하나씩 추가해준 것과는 다르답니다. 그렇기 때문에 나중에 불러온 setTimeout 함수에서도 0,1,2가 그대로 남아 있는 거에요!

 </p>
 </details>

 <br>
 <br>

### 🎁 object

<br>

### 난이도 : 🌶

<br>

#### ☁︎ 객체의 복사 방법

```javascript
// 무엇이 출력 될까요?

let c = { greeting: "Hey!" };
let d;

d = c;
c.greeting = "Hello";
console.log(d.greeting);
```

- A: `Hello`
- B: `Hey!`
- C: `undefined`
- D: `ReferenceError`
- E: `TypeError`

<details><summary><b>Answer</b></summary>
  <p>
    
#### 정답: A

<a href="https://ko.javascript.info/object-copy">개념 참고 사이트</a>

객체와 원시 타입의 근본적인 차이 중 하나는 객체는 ‘참조에 의해(by reference)’ 저장되고 복사된다는 것입니다.

원시값(문자열, 숫자, 불린 값)은 ‘값 그대로’ 저장·할당되고 복사되는 반면에 말이죠.

같은 상황에서 다음과 같이 했다면 어땠을까요?

```javascript
let c = 4;
let d;

d = c;
c = 5;
console.log(d);
```

d는 그대로 4가 나올 것입니다. c의 값을 그대로 복사해와서 d에 저장했기 때문에, c의 변화와 상관 없이 d는 이미 4로 고정되어 있습니다.

그런데 객체의 동작방식은 이와 다릅니다.

변수엔 객체가 그대로 저장되는 것이 아니라, 객체가 저장되어있는 '메모리 주소’인 객체에 대한 '참조 값’이 저장됩니다.

<br>

우선 변수 `c`는 객체에 대한 값을 유지해요. 그 후, `c`와 동일한 객체 참조를 `d`에 할당해요.

<img src="https://i.imgur.com/ko5k0fs.png" width="200">

한 개의 객체를 변경하면, 그것들 모두 변경해요.

 </p>
 </details>

 <br>
 <br>
