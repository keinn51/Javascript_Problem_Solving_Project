# dndbekfrl1's Problems

### π Basic

<br>

### λμ΄λ : πΆ

<br>

#### βοΈ λ¬Έμμ΄ λ€λ£¨κΈ°

```javascript
λ¬Έμμ΄ sμ κΈΈμ΄κ° 4 λλ 6μ΄κ³ , μ«μλ‘λ§ κ΅¬μ±λμ΄μλμ§ νμΈνλ solution ν¨μλ₯Ό μμ±νμΈμ.
(μ: 1234λ Trueμ΄κ³ , a234λ Falseλ₯Ό λ°νν©λλ€.)

function solution(s){

}

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//μμ±ν λ΅
function solution(s) {
  var result = false;
  var length = s.length;
  if (length == 4 || length == 6) {
    result = true;
    var tmp = s.split("");
    tmp.forEach((item) => {
      if (isNaN(item)) {
        result = false;
      }
    });
  }
  return result;
}

isNaN()μ λ§€κ°λ³μκ° μ«μμΈμ§ κ²μ¬νλ ν¨μμλλ€.
Number()κ³Ό parseInt()λ μ¨λ³΄μλλ°, κ°μΈμ μΌλ‘ isNaN()μ΄ μ μΌ μ½λμ§κΈ° μ¬μ μ΅λλ€!

//λ€λ₯Έμ¬λ νμ΄
function solution(s) {
  return s.length == 4 || s.length == 6 ? !isNaN(s) : false;
}



//μΆμ² https://programmers.co.kr/learn/courses/30/lessons/12918
```

 </p>
 </details>
 <br>
 <br>

### π Basic

<br>

### λμ΄λ : πΆ

<br>

#### βοΈ λ μ μ μ¬μ΄μ ν©

```javascript
λ μ μ a, b μ¬μ΄μ μν λͺ¨λ  μ μμ ν©μ λ¦¬ν΄νλ solutionμ μμ±νμΈμ.
function solution(a,b){

}
```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//μμ±ν λ΅
function solution(a, b) {
  var result = 0;
  var start = 0;
  var finish = 0;
  if (a > b) {
    start = b;
    finish = a;
  } else {
    start = a;
    finish = b;
  }

  for (var i = start; i <= finish; i++) {
    result += i;
  }
  return result;
}
//λ€λ₯Έμ¬λ νμ΄
function solution(x) {
  return ((a + b) * (Math.abs(b - a) + 1)) / 2;
}

//μΆμ² https://programmers.co.kr/learn/courses/30/lessons/12912
```

 </p>
 </details>
 <br>
 <br>

### π Array

<br>

### λμ΄λ : πΆ

<br>

#### βοΈ κ°μ μ«μλ μ«μ΄

```javascript
λ°°μ΄ arrμ κ° μμλ μ«μ 0λΆν° 9κΉμ§λ‘ μ΄λ£¨μ΄μ Έ μμ΅λλ€. μ΄λ, λ°°μ΄ arrμμ μ°μμ μΌλ‘ λνλλ μ«μλ νλλ§ λ¨κΈ°κ³  μ λΆ μ κ±°νλ €κ³  ν©λλ€. λ¨, λ°°μ΄ arrμ μμλ€μ μμλ₯Ό μ μ§ν΄μΌ ν©λλ€.
(μ arr = [1, 1, 3, 3, 0, 1, 1] μ΄λ©΄ [1, 3, 0, 1] μ return ν©λλ€. arr = [4, 4, 4, 3, 3] μ΄λ©΄ [4, 3] μ return ν©λλ€.)

function solution(arr){

}

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
//μμ±ν λ΅
function solution(arr) {
  var result = [];
  result.push(arr[0]);
  len_result = 0;
  var length = arr.length;

  if (length > 0) {
    for (var i = 1; i < length; i++) {
      if (result[len_result] != arr[i]) {
        len_result += 1;
        result.push(arr[i]);
      }
    }
  }

  return result;
}

λ°°μ΄ resultκ³Ό arrλ₯Ό λΉκ΅νλ©΄μ μ°μλμ§ μμ κ°μ resultμ pushν΄ μ£Όμμ΅λλ€.

//λ€λ₯Έμ¬λ νμ΄
function solution(arr) {
  return arr.filter((val, index) => val != arr[index + 1]);
}
filterλ₯Ό μ°λ©΄ κ°λ¨νκ² κ΅¬νν  μ μμμ΅λλ€..!

function solution(arr) {
  var answer = [arr[0]];

  for (let i = 1; i < arr.length; i++) {
    if (answer[answer.length - 1] !== arr[i]) {
      answer.push(arr[i]);
    }
  }

  return answer;
}

//μΆμ² https://programmers.co.kr/learn/courses/30/lessons/12906
```
 </p>
 </details>
 <br>
 <br>

### π Function

<br>

### λμ΄λ : πΆπΆ

<br>

#### βοΈ νμ΄ν ν¨μ

```javascript
λ€μ ν¨μλ₯Ό νμ΄ν ν¨μλ‘ λ³κ²½ν΄λ³΄μΈμ.

function ask(question, yes, no){
  if(confirm(question)) yes();
  else no();
}

ask(
  "λμνμ­λκΉ?",
  function(){alert("λμνμ¨μ΅λλ€.");},
  function(){alert("μ·¨μ λ²νΌμ λλ₯΄μ¨μ΅λλ€.");}
);

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
ask(
  "λμνμ­λκΉ?",
  ()=>alert("λμνμ¨μ΅λλ€.");,
  ()=>alert("μ·¨μ λ²νΌμ λλ₯΄μ¨μ΅λλ€."); )


μ’ λ κ°κ²°ν λ¬Έλ²μΌλ‘ ννν  μ μλ νμ΄ν ν¨μμ λν΄ νμ΅νμ΅λλ€.
νμ΄ν ν¨μμ κ΅¬μ‘°λ '()'μμ μΈμλ₯Ό λ°κ³ , '=>'μ°μΈ‘μ κ²°κ³Όλ₯Ό λ°νν©λλ€.
map(), setInterval()κ³Ό κ°μ ν¨μμμ λ§μ΄ μ¬μ©λ©λλ€.
```
 </p>
 </details>
 <br>
 <br>

### π Function

<br>

### λμ΄λ : πΆπΆ

<br>

#### βοΈ νμ΄ν ν¨μ2

```javascript
λ€μ ν¨μλ₯Ό νμ΄ν ν¨μλ‘ λ³κ²½ν΄λ³΄μΈμ.

function Person() {
  this.age = 0;

  setInterval(function growUp() {
    this.age++;
  }, 1000);
}

var p = new Person();

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
function Person() {
  this.age = 0;

  setInterval(() => {
    this.age++;
  }, 1000);
}
```
 </p>
 </details>
 <br>
 <br>

### π Function

<br>

### λμ΄λ : πΆ

<br>

#### βοΈ μ¬κ·ν¨μ

```javascript
μ¬κ·ν¨μλ‘ μ£Όμ΄μ§ nλ²μ§Έ νΌλ³΄λμΉ μλ₯Ό κ³μ°νλ ν¨μλ₯Ό κ΅¬ννμΈμ.

function fibo(n){

}

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
function fibo(n) {
  if (n <= 1) {
    return n;
  }
  return fibo(n - 1) + fibo(n - 2);
}
```
 </p>
 </details>
 <br>
 <br>
