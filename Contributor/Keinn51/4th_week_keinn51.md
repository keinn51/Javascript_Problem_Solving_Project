### ๐ Basic

<br>

#### ์ง์๋ ๊ณต์ ๋ฌธ์ ์๋๋ค.

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ ๋ฌธ์์ด ๋ค๋ฃจ๊ธฐ

```javascript
๋ฌธ์์ด s์ ๊ธธ์ด๊ฐ 4 ๋๋ 6์ด๊ณ , ์ซ์๋ก๋ง ๊ตฌ์ฑ๋์ด์๋์ง ํ์ธํ๋ solution ํจ์๋ฅผ ์์ฑํ์ธ์.
(์: 1234๋ true์ด๊ณ , a234๋ false๋ฅผ ๋ฐํํฉ๋๋ค.)

function solution(s){

}

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
function solution(s) {
  return s.length == 4 || s.length == 6 ? !isNaN(s) : false;
}

//์ถ์ฒ https://programmers.co.kr/learn/courses/30/lessons/12918
```

 </p>
 </details>
 <br>
 <br>

#### ์์ง๋ ๊ณต์ ๋ฌธ์ ์๋๋ค.

 <br>

### ๋์ด๋ : ๐ถ๐ถ

 <br>

#### โ๏ธ ์ฐ์ฐ์

```javascript
์๋ ํํ์์ ๊ฒฐ๊ณผ๋ฅผ ์์ธกํด ๋ณด์ธ์.
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
1)  10      ""์ ๋น ๋ฌธ์์ด๋ก ์ทจ๊ธ๋๊ณ , ๋ฌธ์์ด + ์ซ์๊ฐ ๋๋ฉด ์ซ์๋ ๋ฌธ์ ์ทจ๊ธ์ ๋ฐ๋๋ค.
2)  -1      ""์ ๋ฌธ์์ด์ธ๋ฐ ์ซ์ 0์ผ๋ก ๋ณํฉ๋๋ค.
3)  1       ์ฐธ:1 / ๊ฑฐ์ง:0
4)  2       +๋ฅผ ์ ์ธํ ์ฐ์  ์ฐ์ฐ์๋ ํผ์ฐ์ฐ์๊ฐ ์ซ์ํ์ด ์๋๊ฒฝ์ฐ ์ซ์ํ์ผ๋ก ๋ฐ๊ฟ.
5)  6       +๋ฅผ ์ ์ธํ ์ฐ์  ์ฐ์ฐ์๋ ํผ์ฐ์ฐ์๊ฐ ์ซ์ํ์ด ์๋๊ฒฝ์ฐ ์ซ์ํ์ผ๋ก ๋ฐ๊ฟ.
6)  9px     ๋ฌธ์์ด ๋ํ๊ธฐ
7)  $45     ๋ฌธ์์ด ๋ํ๊ธฐ
8)  2       +๋ฅผ ์ ์ธํ ์ฐ์  ์ฐ์ฐ์๋ ํผ์ฐ์ฐ์๊ฐ ์ซ์ํ์ด ์๋๊ฒฝ์ฐ ์ซ์ํ์ผ๋ก ๋ฐ๊ฟ.
9)  NaN     "4px"์ ์ซ์๋ก ๋ณํํ  ์ ์๊ธฐ ๋๋ฌธ์ NaN.
10) Infinty ์ฐ์  ์ฐ์ฐ
11)  -9 5   ๋ฌธ์์ด ๋ํ๊ธฐ
12) -14     ๋ฌธ์์ด์ด ์ซ์ํ์ผ๋ก ๋ณํ๋ฉด ์๋ค ๊ณต๋ฐฑ์ด ์ญ์ ๋๋ค.
13) 1       null์ ์ซ์ํ ๋ณํ์ 0.
14) NaN     undefined๋ ์ซ์ํ ๋ณํ์ NaN.
15) -2      ๋ฌธ์์ด์ด ์ซ์ํ์ผ๋ก ๋ณํ๋ฉด ์๋ค ๊ณต๋ฐฑ์ด ์ญ์ ๋๋๋ฐ, ๊ณต๋ฐฑ๋ง๋๋ ๋ฌธ์์ด์ด ์ญ์ ๋์ด ""๋ก ์ธ์๋๊ณ  ์ด๊ฒ์ด 0์ผ๋ก ์ธ์๋๋ค.

<1> A+B ์์๋ A๊ฐ ๋ฌธ์์ด์ผ ๋ B๋ฅผ ๋ฌธ์์ด์ผ๋ก ์ธ์ํ์ง๋ง,
<2> A-B ์์๋ A๊ฐ ๋ฌธ์์ด์ด์ด๋ ์ซ์๋ก ๋ณํํ๋ค. ๋ง์ฝ A๊ฐ ์ซ์๋ก ๋ณํ์ด ๋์ง ์๋๋ค๋ฉด NaN์ด ๋์ด๋ฒ๋ฆฐ๋ค.
```

 </p>
 </details>
 <br>
 <br>

### ๐ Array

<br>

#### ์ง์๋ ๊ณต์ ๋ฌธ์ ์๋๋ค.

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ ๊ฐ์ ์ซ์๋ ์ซ์ด

```javascript
๋ฐฐ์ด arr์ ๊ฐ ์์๋ ์ซ์ 0๋ถํฐ 9๊น์ง๋ก ์ด๋ฃจ์ด์ ธ ์์ต๋๋ค. ์ด๋, ๋ฐฐ์ด arr์์ ์ฐ์์ ์ผ๋ก ๋ํ๋๋ ์ซ์๋ ํ๋๋ง ๋จ๊ธฐ๊ณ  ์ ๋ถ ์ ๊ฑฐํ๋ ค๊ณ  ํฉ๋๋ค. ๋จ, ๋ฐฐ์ด arr์ ์์๋ค์ ์์๋ฅผ ์ ์งํด์ผ ํฉ๋๋ค.
(์ arr = [1, 1, 3, 3, 0, 1, 1] ์ด๋ฉด [1, 3, 0, 1] ์ return ํฉ๋๋ค. arr = [4, 4, 4, 3, 3] ์ด๋ฉด [4, 3] ์ return ํฉ๋๋ค.)

function solution(arr){

}

```

<details><summary><b>Answer</b></summary>

<p>

```javascript
// ๐ ์์ฑํ ๋ต
function solution(arr) {
  let answer = [arr[0]];

  arr.forEach(element => {
    (!(answer[answer.length - 1] == element)) ? answer.push(element) : ''
  });

  return answer
}

๋ฐฐ์ด result๊ณผ arr๋ฅผ ๋น๊ตํ๋ฉด์ ์ฐ์๋์ง ์์ ๊ฐ์ result์ pushํด ์ฃผ์์ต๋๋ค.

// ๐ ํ๋ก๊ทธ๋๋จธ์ค 1ํฐ์ด ํ์ด

function solution(arr)
{
    return arr.filter((val,index) => val != arr[index+1]);
}

//์ถ์ฒ https://programmers.co.kr/learn/courses/30/lessons/12906
```

 </p>
 </details>
 <br>
 <br>

#### โ๏ธ ํฐ์ผ๋ชฌ

```javascript
// ๋ฌธ์  ์ค๋ช

๋น์ ์ ํฐ์ผ๋ชฌ์ ์ก๊ธฐ ์ํ ์ค๋ ์ฌํ ๋์, ํ ๋ฐ์ฌ๋์ ์ฐ๊ตฌ์ค์ ๋์ฐฉํ์ต๋๋ค. ํ ๋ฐ์ฌ๋์ ๋น์ ์๊ฒ ์์ ์ ์ฐ๊ตฌ์ค์ ์๋ ์ด N ๋ง๋ฆฌ์ ํฐ์ผ๋ชฌ ์ค์์ N/2๋ง๋ฆฌ๋ฅผ ๊ฐ์ ธ๊ฐ๋ ์ข๋ค๊ณ  ํ์ต๋๋ค.
ํ ๋ฐ์ฌ๋ ์ฐ๊ตฌ์ค์ ํฐ์ผ๋ชฌ์ ์ข๋ฅ์ ๋ฐ๋ผ ๋ฒํธ๋ฅผ ๋ถ์ฌ ๊ตฌ๋ถํฉ๋๋ค. ๋ฐ๋ผ์ ๊ฐ์ ์ข๋ฅ์ ํฐ์ผ๋ชฌ์ ๊ฐ์ ๋ฒํธ๋ฅผ ๊ฐ์ง๊ณ  ์์ต๋๋ค. ์๋ฅผ ๋ค์ด ์ฐ๊ตฌ์ค์ ์ด 4๋ง๋ฆฌ์ ํฐ์ผ๋ชฌ์ด ์๊ณ , ๊ฐ ํฐ์ผ๋ชฌ์ ์ข๋ฅ ๋ฒํธ๊ฐ [3๋ฒ, 1๋ฒ, 2๋ฒ, 3๋ฒ]์ด๋ผ๋ฉด ์ด๋ 3๋ฒ ํฐ์ผ๋ชฌ ๋ ๋ง๋ฆฌ, 1๋ฒ ํฐ์ผ๋ชฌ ํ ๋ง๋ฆฌ, 2๋ฒ ํฐ์ผ๋ชฌ ํ ๋ง๋ฆฌ๊ฐ ์์์ ๋ํ๋๋๋ค. ์ด๋, 4๋ง๋ฆฌ์ ํฐ์ผ๋ชฌ ์ค 2๋ง๋ฆฌ๋ฅผ ๊ณ ๋ฅด๋ ๋ฐฉ๋ฒ์ ๋ค์๊ณผ ๊ฐ์ด 6๊ฐ์ง๊ฐ ์์ต๋๋ค.

์ฒซ ๋ฒ์งธ(3๋ฒ), ๋ ๋ฒ์งธ(1๋ฒ) ํฐ์ผ๋ชฌ์ ์ ํ
์ฒซ ๋ฒ์งธ(3๋ฒ), ์ธ ๋ฒ์งธ(2๋ฒ) ํฐ์ผ๋ชฌ์ ์ ํ
์ฒซ ๋ฒ์งธ(3๋ฒ), ๋ค ๋ฒ์งธ(3๋ฒ) ํฐ์ผ๋ชฌ์ ์ ํ
๋ ๋ฒ์งธ(1๋ฒ), ์ธ ๋ฒ์งธ(2๋ฒ) ํฐ์ผ๋ชฌ์ ์ ํ
๋ ๋ฒ์งธ(1๋ฒ), ๋ค ๋ฒ์งธ(3๋ฒ) ํฐ์ผ๋ชฌ์ ์ ํ
์ธ ๋ฒ์งธ(2๋ฒ), ๋ค ๋ฒ์งธ(3๋ฒ) ํฐ์ผ๋ชฌ์ ์ ํ

์ด๋, ์ฒซ ๋ฒ์งธ(3๋ฒ) ํฐ์ผ๋ชฌ๊ณผ ๋ค ๋ฒ์งธ(3๋ฒ) ํฐ์ผ๋ชฌ์ ์ ํํ๋ ๋ฐฉ๋ฒ์ ํ ์ข๋ฅ(3๋ฒ ํฐ์ผ๋ชฌ ๋ ๋ง๋ฆฌ)์ ํฐ์ผ๋ชฌ๋ง ๊ฐ์ง ์ ์์ง๋ง, ๋ค๋ฅธ ๋ฐฉ๋ฒ๋ค์ ๋ชจ๋ ๋ ์ข๋ฅ์ ํฐ์ผ๋ชฌ์ ๊ฐ์ง ์ ์์ต๋๋ค. ๋ฐ๋ผ์ ์ ์์์์ ๊ฐ์ง ์ ์๋ ํฐ์ผ๋ชฌ ์ข๋ฅ ์์ ์ต๋๊ฐ์ 2๊ฐ ๋ฉ๋๋ค.
๋น์ ์ ์ต๋ํ ๋ค์ํ ์ข๋ฅ์ ํฐ์ผ๋ชฌ์ ๊ฐ์ง๊ธธ ์ํ๊ธฐ ๋๋ฌธ์, ์ต๋ํ ๋ง์ ์ข๋ฅ์ ํฐ์ผ๋ชฌ์ ํฌํจํด์ N/2๋ง๋ฆฌ๋ฅผ ์ ํํ๋ ค ํฉ๋๋ค. N๋ง๋ฆฌ ํฐ์ผ๋ชฌ์ ์ข๋ฅ ๋ฒํธ๊ฐ ๋ด๊ธด ๋ฐฐ์ด nums๊ฐ ๋งค๊ฐ๋ณ์๋ก ์ฃผ์ด์ง ๋, N/2๋ง๋ฆฌ์ ํฐ์ผ๋ชฌ์ ์ ํํ๋ ๋ฐฉ๋ฒ ์ค, ๊ฐ์ฅ ๋ง์ ์ข๋ฅ์ ํฐ์ผ๋ชฌ์ ์ ํํ๋ ๋ฐฉ๋ฒ์ ์ฐพ์, ๊ทธ๋์ ํฐ์ผ๋ชฌ ์ข๋ฅ ๋ฒํธ์ ๊ฐ์๋ฅผ return ํ๋๋ก solution ํจ์๋ฅผ ์์ฑํด์ฃผ์ธ์.

// ์ ํ์ฌํญ

nums๋ ํฐ์ผ๋ชฌ์ ์ข๋ฅ ๋ฒํธ๊ฐ ๋ด๊ธด 1์ฐจ์ ๋ฐฐ์ด์๋๋ค.
nums์ ๊ธธ์ด(N)๋ 1 ์ด์ 10,000 ์ดํ์ ์์ฐ์์ด๋ฉฐ, ํญ์ ์ง์๋ก ์ฃผ์ด์ง๋๋ค.
ํฐ์ผ๋ชฌ์ ์ข๋ฅ ๋ฒํธ๋ 1 ์ด์ 200,000 ์ดํ์ ์์ฐ์๋ก ๋ํ๋๋๋ค.
๊ฐ์ฅ ๋ง์ ์ข๋ฅ์ ํฐ์ผ๋ชฌ์ ์ ํํ๋ ๋ฐฉ๋ฒ์ด ์ฌ๋ฌ ๊ฐ์ง์ธ ๊ฒฝ์ฐ์๋, ์ ํํ  ์ ์๋ ํฐ์ผ๋ชฌ ์ข๋ฅ ๊ฐ์์ ์ต๋๊ฐ ํ๋๋ง return ํ๋ฉด ๋ฉ๋๋ค.

// ์์ถ๋ ฅ ์

nums	          result
[3,1,2,3]	      2
[3,3,3,2,2,4]	  3
[3,3,3,2,2,2]	  2

// ์์ถ๋ ฅ ์ ์ค๋ช

์์ถ๋ ฅ ์ #1
๋ฌธ์ ์ ์์์ ๊ฐ์ต๋๋ค.

์์ถ๋ ฅ ์ #2
6๋ง๋ฆฌ์ ํฐ์ผ๋ชฌ์ด ์์ผ๋ฏ๋ก, 3๋ง๋ฆฌ์ ํฐ์ผ๋ชฌ์ ๊ณจ๋ผ์ผ ํฉ๋๋ค.
๊ฐ์ฅ ๋ง์ ์ข๋ฅ์ ํฐ์ผ๋ชฌ์ ๊ณ ๋ฅด๊ธฐ ์ํด์๋ 3๋ฒ ํฐ์ผ๋ชฌ ํ ๋ง๋ฆฌ, 2๋ฒ ํฐ์ผ๋ชฌ ํ ๋ง๋ฆฌ, 4๋ฒ ํฐ์ผ๋ชฌ ํ ๋ง๋ฆฌ๋ฅผ ๊ณ ๋ฅด๋ฉด ๋๋ฉฐ, ๋ฐ๋ผ์ 3์ return ํฉ๋๋ค.

์์ถ๋ ฅ ์ #3
6๋ง๋ฆฌ์ ํฐ์ผ๋ชฌ์ด ์์ผ๋ฏ๋ก, 3๋ง๋ฆฌ์ ํฐ์ผ๋ชฌ์ ๊ณจ๋ผ์ผ ํฉ๋๋ค.
๊ฐ์ฅ ๋ง์ ์ข๋ฅ์ ํฐ์ผ๋ชฌ์ ๊ณ ๋ฅด๊ธฐ ์ํด์๋ 3๋ฒ ํฐ์ผ๋ชฌ ํ ๋ง๋ฆฌ์ 2๋ฒ ํฐ์ผ๋ชฌ ๋ ๋ง๋ฆฌ๋ฅผ ๊ณ ๋ฅด๊ฑฐ๋, ํน์ 3๋ฒ ํฐ์ผ๋ชฌ ๋ ๋ง๋ฆฌ์ 3๋ฒ ํฐ์ผ๋ชฌ ํ ๋ง๋ฆฌ๋ฅผ ๊ณ ๋ฅด๋ฉด ๋ฉ๋๋ค. ๋ฐ๋ผ์ ์ต๋ ๊ณ ๋ฅผ ์ ์๋ ํฐ์ผ๋ชฌ ์ข๋ฅ์ ์๋ 2์๋๋ค.
```

 <details><summary><b>Answer</b></summary>

   <p>

```javascript
function solution(nums) {
  let answer = new Set(nums);
  return answer.size <= nums.length / 2 ? answer.size : nums.length / 2;
}
```

  </p>
  </details>
  <br>
  <br>

#### โ๏ธ ์์๋ํ๊ธฐ

```javascript
// ๋ฌธ์  ์ค๋ช

์ด๋ค ์ ์๋ค์ด ์์ต๋๋ค. ์ด ์ ์๋ค์ ์ ๋๊ฐ์ ์ฐจ๋ก๋๋ก ๋ด์ ์ ์ ๋ฐฐ์ด absolutes์ ์ด ์ ์๋ค์ ๋ถํธ๋ฅผ ์ฐจ๋ก๋๋ก ๋ด์ ๋ถ๋ฆฌ์ธ ๋ฐฐ์ด signs๊ฐ ๋งค๊ฐ๋ณ์๋ก ์ฃผ์ด์ง๋๋ค. ์ค์  ์ ์๋ค์ ํฉ์ ๊ตฌํ์ฌ return ํ๋๋ก solution ํจ์๋ฅผ ์์ฑํด์ฃผ์ธ์.

// ์ ํ์ฌํญ

absolutes์ ๊ธธ์ด๋ 1 ์ด์ 1,000 ์ดํ์๋๋ค.
absolutes์ ๋ชจ๋  ์๋ ๊ฐ๊ฐ 1 ์ด์ 1,000 ์ดํ์๋๋ค.
signs์ ๊ธธ์ด๋ absolutes์ ๊ธธ์ด์ ๊ฐ์ต๋๋ค.
signs[i] ๊ฐ ์ฐธ์ด๋ฉด absolutes[i] ์ ์ค์  ์ ์๊ฐ ์์์์, ๊ทธ๋ ์ง ์์ผ๋ฉด ์์์์ ์๋ฏธํฉ๋๋ค.

// ์์ถ๋ ฅ ์

absolutes	  signs	              result
[4,7,12]    [true,false,true]	  9
[1,2,3]	    [false,false,true]	0

// ์์ถ๋ ฅ ์ ์ค๋ช

์์ถ๋ ฅ ์ #1
signs๊ฐ [true,false,true] ์ด๋ฏ๋ก, ์ค์  ์๋ค์ ๊ฐ์ ๊ฐ๊ฐ 4, -7, 12์๋๋ค.
๋ฐ๋ผ์ ์ธ ์์ ํฉ์ธ 9๋ฅผ return ํด์ผ ํฉ๋๋ค.
์์ถ๋ ฅ ์ #2
signs๊ฐ [false,false,true] ์ด๋ฏ๋ก, ์ค์  ์๋ค์ ๊ฐ์ ๊ฐ๊ฐ -1, -2, 3์๋๋ค.
๋ฐ๋ผ์ ์ธ ์์ ํฉ์ธ 0์ return ํด์ผ ํฉ๋๋ค.
```

 <details><summary><b>Answer</b></summary>

   <p>

```javascript
function solution(absolutes, signs) {
  let answer = 0;

  absolutes.forEach((element, i) => {
    answer += signs[i] ? absolutes[i] : -absolutes[i];
  });

  return answer;
}
```

  </p>
  </details>
  <br>
  <br>

### ๋์ด๋ : ๐ถ๐ถ

<br>

#### โ๏ธ ๋ชจ์๊ณ ์ฌ

```javascript
// ๋ฌธ์  ์ค๋ช

์ํฌ์๋ ์ํ์ ํฌ๊ธฐํ ์ฌ๋์ ์ค๋ง์๋๋ค. ์ํฌ์ ์ผ์ธ๋ฐฉ์ ๋ชจ์๊ณ ์ฌ์ ์ํ ๋ฌธ์ ๋ฅผ ์ ๋ถ ์ฐ์ผ๋ ค ํฉ๋๋ค. ์ํฌ์๋ 1๋ฒ ๋ฌธ์ ๋ถํฐ ๋ง์ง๋ง ๋ฌธ์ ๊น์ง ๋ค์๊ณผ ๊ฐ์ด ์ฐ์ต๋๋ค.

1๋ฒ ์ํฌ์๊ฐ ์ฐ๋ ๋ฐฉ์: 1, 2, 3, 4, 5, 1, 2, 3, 4, 5, ...
2๋ฒ ์ํฌ์๊ฐ ์ฐ๋ ๋ฐฉ์: 2, 1, 2, 3, 2, 4, 2, 5, 2, 1, 2, 3, 2, 4, 2, 5, ...
3๋ฒ ์ํฌ์๊ฐ ์ฐ๋ ๋ฐฉ์: 3, 3, 1, 1, 2, 2, 4, 4, 5, 5, 3, 3, 1, 1, 2, 2, 4, 4, 5, 5, ...

1๋ฒ ๋ฌธ์ ๋ถํฐ ๋ง์ง๋ง ๋ฌธ์ ๊น์ง์ ์ ๋ต์ด ์์๋๋ก ๋ค์ ๋ฐฐ์ด answers๊ฐ ์ฃผ์ด์ก์ ๋, ๊ฐ์ฅ ๋ง์ ๋ฌธ์ ๋ฅผ ๋งํ ์ฌ๋์ด ๋๊ตฌ์ธ์ง ๋ฐฐ์ด์ ๋ด์ return ํ๋๋ก solution ํจ์๋ฅผ ์์ฑํด์ฃผ์ธ์.

// ์ ํ ์กฐ๊ฑด

์ํ์ ์ต๋ 10,000 ๋ฌธ์ ๋ก ๊ตฌ์ฑ๋์ด์์ต๋๋ค.
๋ฌธ์ ์ ์ ๋ต์ 1, 2, 3, 4, 5์ค ํ๋์๋๋ค.
๊ฐ์ฅ ๋์ ์ ์๋ฅผ ๋ฐ์ ์ฌ๋์ด ์ฌ๋ฟ์ผ ๊ฒฝ์ฐ, returnํ๋ ๊ฐ์ ์ค๋ฆ์ฐจ์ ์ ๋ ฌํด์ฃผ์ธ์.

// ์์ถ๋ ฅ ์

answers: [1,2,3,4,5]	return: [1]
answers: [1,3,2,4,2]	return: [1,2,3]

// ์์ถ๋ ฅ ์ ์ค๋ช

์์ถ๋ ฅ ์ #1
์ํฌ์ 1์ ๋ชจ๋  ๋ฌธ์ ๋ฅผ ๋งํ์ต๋๋ค.
์ํฌ์ 2๋ ๋ชจ๋  ๋ฌธ์ ๋ฅผ ํ๋ ธ์ต๋๋ค.
์ํฌ์ 3์ ๋ชจ๋  ๋ฌธ์ ๋ฅผ ํ๋ ธ์ต๋๋ค.
๋ฐ๋ผ์ ๊ฐ์ฅ ๋ฌธ์ ๋ฅผ ๋ง์ด ๋งํ ์ฌ๋์ ์ํฌ์ 1์๋๋ค.

์์ถ๋ ฅ ์ #2
๋ชจ๋  ์ฌ๋์ด 2๋ฌธ์ ์ฉ์ ๋ง์ท์ต๋๋ค.
```

 <details><summary><b>Answer</b></summary>

   <p>

```javascript
์ถ์ฒ : https://programmers.co.kr/learn/challenges

// ๐ ๋ฐ๋ณต์ ์ ๊ฒํ๋ ํ์ด

function solution(array) {
  var answer = [];
  let one = [1, 2, 3, 4, 5];
  let two = [2, 1, 2, 3, 2, 4, 2, 5];
  let three = [3, 3, 1, 1, 2, 2, 4, 4, 5, 5];

  let count1 = 0,
    count2 = 0,
    count3 = 0;

  for (let i = 0; i < array.length; i++) {
    if (array[i] == one[i % one.length]) {
      count1++;
    }
    if (array[i] == two[i % two.length]) {
      count2++;
    }
    if (array[i] == three[i % three.length]) {
      count3++;
    }
  }

  let high = Math.max(count1, count2, count3);

  if (high == count1) {
    answer.push(1);
  }
  if (high == count2) {
    answer.push(2);
  }
  if (high == count3) {
    answer.push(3);
  }

  return answer;
}

// ๐ ๋ณ์ ์ค์ ์ ์ ๊ฒ ํ๋ ํ์ด

function solution(answers) {
  var answer = [];
  var a1 = [1, 2, 3, 4, 5];
  var a2 = [2, 1, 2, 3, 2, 4, 2, 5];
  var a3 = [3, 3, 1, 1, 2, 2, 4, 4, 5, 5];

  var a1c = answers.filter((a, i) => a === a1[i % a1.length]).length;
  var a2c = answers.filter((a, i) => a === a2[i % a2.length]).length;
  var a3c = answers.filter((a, i) => a === a3[i % a3.length]).length;
  var max = Math.max(a1c, a2c, a3c);

  if (a1c === max) {
    answer.push(1);
  }
  if (a2c === max) {
    answer.push(2);
  }
  if (a3c === max) {
    answer.push(3);
  }

  return answer;
}
```

  </p>
  </details>
  <br>
  <br>

### ๋์ด๋ : ๐ถ๐ถ

<br>

#### โ๏ธ ๊ธฐ๋ฅ๊ฐ๋ฐ ๋ฐ ๋ฐฐํฌ

```javascript
// ๋ฌธ์  ์ค๋ช

ํ๋ก๊ทธ๋๋จธ์ค ํ์์๋ ๊ธฐ๋ฅ ๊ฐ์  ์์์ ์ํ ์ค์๋๋ค. ๊ฐ ๊ธฐ๋ฅ์ ์ง๋๊ฐ 100%์ผ ๋ ์๋น์ค์ ๋ฐ์ํ  ์ ์์ต๋๋ค.
๋, ๊ฐ ๊ธฐ๋ฅ์ ๊ฐ๋ฐ์๋๋ ๋ชจ๋ ๋ค๋ฅด๊ธฐ ๋๋ฌธ์ ๋ค์ ์๋ ๊ธฐ๋ฅ์ด ์์ ์๋ ๊ธฐ๋ฅ๋ณด๋ค ๋จผ์  ๊ฐ๋ฐ๋  ์ ์๊ณ , ์ด๋ ๋ค์ ์๋ ๊ธฐ๋ฅ์ ์์ ์๋ ๊ธฐ๋ฅ์ด ๋ฐฐํฌ๋  ๋ ํจ๊ป ๋ฐฐํฌ๋ฉ๋๋ค.
๋จผ์  ๋ฐฐํฌ๋์ด์ผ ํ๋ ์์๋๋ก ์์์ ์ง๋๊ฐ ์ ํ ์ ์ ๋ฐฐ์ด progresses์ ๊ฐ ์์์ ๊ฐ๋ฐ ์๋๊ฐ ์ ํ ์ ์ ๋ฐฐ์ด speeds๊ฐ ์ฃผ์ด์ง ๋ ๊ฐ ๋ฐฐํฌ๋ง๋ค ๋ช ๊ฐ์ ๊ธฐ๋ฅ์ด ๋ฐฐํฌ๋๋์ง๋ฅผ return ํ๋๋ก solution ํจ์๋ฅผ ์์ฑํ์ธ์.

// ์ ํ ์ฌํญ

์์์ ๊ฐ์(progresses, speeds๋ฐฐ์ด์ ๊ธธ์ด)๋ 100๊ฐ ์ดํ์๋๋ค.
์์ ์ง๋๋ 100 ๋ฏธ๋ง์ ์์ฐ์์๋๋ค.
์์ ์๋๋ 100 ์ดํ์ ์์ฐ์์๋๋ค.
๋ฐฐํฌ๋ ํ๋ฃจ์ ํ ๋ฒ๋ง ํ  ์ ์์ผ๋ฉฐ, ํ๋ฃจ์ ๋์ ์ด๋ฃจ์ด์ง๋ค๊ณ  ๊ฐ์ ํฉ๋๋ค. ์๋ฅผ ๋ค์ด ์ง๋์จ์ด 95%์ธ ์์์ ๊ฐ๋ฐ ์๋๊ฐ ํ๋ฃจ์ 4%๋ผ๋ฉด ๋ฐฐํฌ๋ 2์ผ ๋ค์ ์ด๋ฃจ์ด์ง๋๋ค.

// ์์ถ๋ ฅ ์

progresses	              speeds	            return
[93, 30, 55]	            [1, 30, 5]	        [2, 1]
[95, 90, 99, 99, 80, 99]	[1, 1, 1, 1, 1, 1]	[1, 3, 2]
[95, 80, 99, 99, 90, 99]  [1, 1, 1, 1, 1, 1]  [1, 5]

// ์์ถ๋ ฅ ์ ์ค๋ช

& ์์ถ๋ ฅ ์ #1
์ฒซ ๋ฒ์งธ ๊ธฐ๋ฅ์ 93% ์๋ฃ๋์ด ์๊ณ  ํ๋ฃจ์ 1%์ฉ ์์์ด ๊ฐ๋ฅํ๋ฏ๋ก 7์ผ๊ฐ ์์ ํ ๋ฐฐํฌ๊ฐ ๊ฐ๋ฅํฉ๋๋ค.
๋ ๋ฒ์งธ ๊ธฐ๋ฅ์ 30%๊ฐ ์๋ฃ๋์ด ์๊ณ  ํ๋ฃจ์ 30%์ฉ ์์์ด ๊ฐ๋ฅํ๋ฏ๋ก 3์ผ๊ฐ ์์ ํ ๋ฐฐํฌ๊ฐ ๊ฐ๋ฅํฉ๋๋ค. ํ์ง๋ง ์ด์  ์ฒซ ๋ฒ์งธ ๊ธฐ๋ฅ์ด ์์ง ์์ฑ๋ ์ํ๊ฐ ์๋๊ธฐ ๋๋ฌธ์ ์ฒซ ๋ฒ์งธ ๊ธฐ๋ฅ์ด ๋ฐฐํฌ๋๋ 7์ผ์งธ ๋ฐฐํฌ๋ฉ๋๋ค.
์ธ ๋ฒ์งธ ๊ธฐ๋ฅ์ 55%๊ฐ ์๋ฃ๋์ด ์๊ณ  ํ๋ฃจ์ 5%์ฉ ์์์ด ๊ฐ๋ฅํ๋ฏ๋ก 9์ผ๊ฐ ์์ ํ ๋ฐฐํฌ๊ฐ ๊ฐ๋ฅํฉ๋๋ค.
๋ฐ๋ผ์ 7์ผ์งธ์ 2๊ฐ์ ๊ธฐ๋ฅ, 9์ผ์งธ์ 1๊ฐ์ ๊ธฐ๋ฅ์ด ๋ฐฐํฌ๋ฉ๋๋ค.

& ์์ถ๋ ฅ ์ #2
๋ชจ๋  ๊ธฐ๋ฅ์ด ํ๋ฃจ์ 1%์ฉ ์์์ด ๊ฐ๋ฅํ๋ฏ๋ก, ์์์ด ๋๋๊ธฐ๊น์ง ๋จ์ ์ผ์๋ ๊ฐ๊ฐ 5์ผ, 10์ผ, 1์ผ, 1์ผ, 20์ผ, 1์ผ์๋๋ค. ์ด๋ค ๊ธฐ๋ฅ์ด ๋จผ์  ์์ฑ๋์๋๋ผ๋ ์์ ์๋ ๋ชจ๋  ๊ธฐ๋ฅ์ด ์์ฑ๋์ง ์์ผ๋ฉด ๋ฐฐํฌ๊ฐ ๋ถ๊ฐ๋ฅํฉ๋๋ค.
๋ฐ๋ผ์ 5์ผ์งธ์ 1๊ฐ์ ๊ธฐ๋ฅ, 10์ผ์งธ์ 3๊ฐ์ ๊ธฐ๋ฅ, 20์ผ์งธ์ 2๊ฐ์ ๊ธฐ๋ฅ์ด ๋ฐฐํฌ๋ฉ๋๋ค.
```

 <details><summary><b>Answer</b></summary>

   <p>

```javascript
์ถ์ฒ : https://programmers.co.kr/learn/challenges

// ๐ ํ๋ก๊ทธ๋๋จธ์ค 1ํฐ์ด ํ์ด
function solution(progresses, speeds) {
    let answer = [0];
    let days = progresses.map((progress, index) => Math.ceil((100 - progress) / speeds[index]));
    let maxDay = days[0];

    for(let i = 0, j = 0; i< days.length; i++){
        if(days[i] <= maxDay) {
            answer[j] += 1;
        } else {
            maxDay = days[i];
            answer[++j] = 1;
        }
    }

    return answer;
}

```

 </p>
 </details>
 <br>
 <br>


### ๐ If_and_switch

<br>

### ๋์ด๋ : ๐ถ

<br>

#### โ๏ธ 'if'๋ฅผ '?'๋ก ๊ต์ฒดํ๊ธฐ

```javascript
์กฐ๊ฑด๋ถ ์ฐ์ฐ์ '?'๋ฅผ ์ด์ฉํด if๋ฌธ์ด ์ฌ์ฉ๋ ์๋ ์ฝ๋๋ฅผ ๋ณํํด๋ณด์ธ์. ๋์ ๊ฒฐ๊ณผ๋ ๋์ผํด์ผ ํฉ๋๋ค.

let result;

let a = 1, b = 5;

if (a + b < 4) {
  result = '๋ฏธ๋ง';
} else {
  result = '์ด์';
}
```

 <details><summary><b>Answer</b></summary>

   <p>

```javascript
let result;

let a = 1,
  b = 5;

result = a + b < 4 ? "๋ฏธ๋ง" : "์ด์";
```

  </p>
  </details>
  <br>
  <br>

#### โ๏ธ 'if..else'๋ฅผ '?'๋ก ๊ต์ฒดํ๊ธฐ

```javascript
์กฐ๊ฑด๋ถ ์ฐ์ฐ์ '?'๋ฅผ ์ฌ์ฉํด if..else๋ฌธ์ด ์ฌ์ฉ๋ ์๋ ์ฝ๋๋ฅผ ๋ณํํด๋ณด์ธ์. ๋์ ๊ฒฐ๊ณผ๋ ๋์ผํด์ผ ํฉ๋๋ค.

๊ฐ๋์ฑ์ ์ํด ํํ์์ ์ฌ๋ฌ ์ค๋ก ๋ถํ ํด ์์ฑํด ๋ณด์๊ธธ ๋ฐ๋๋๋ค.

let message;

let login = prompt('Enter Your position: ');

if (login == '์ง์') {
  message = '์๋ํ์ธ์.';
} else if (login == '์์') {
  message = 'ํ์ํฉ๋๋ค.';
} else if (login == '') {
  message = '๋ก๊ทธ์ธ์ด ํ์ํฉ๋๋ค.';
} else {
  message = '';
}
```

 <details><summary><b>Answer</b></summary>

   <p> 

```javascript
let message;

let login = prompt("Enter Your position: ");

message =
  login == "์ง์"
    ? "์๋ํ์ธ์."
    : login == "์์"
    ? "ํ์ํฉ๋๋ค."
    : login == ""
    ? "๋ก๊ทธ์ธ์ด ํ์ํฉ๋๋ค."
    : "";

alert(message);
```

  </p>
  </details>
  <br>
  <br>
