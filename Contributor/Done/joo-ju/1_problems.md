
  

### ๐ Array

  

<br>

  

### ๋์ด๋ : ๐ถ

  

<br>

  

#### โ๏ธ ๋ฐฐ์ด์ ์ญ์ 

  
  

```javascript

๋ค์  ๋ฐฐ์ด์์  400, 500๋ฅผ  ์ญ์ ํ๋  code๋ฅผ  ์๋ ฅํ์ธ์.

  

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

  

#### โ๏ธ ๋ฐฐ์ด์ ๋ด์ฅํจ์

  
  

```javascript

<pass>๋ถ๋ถ์ ๋ฐฐ์ด ๋ด์ฅํจ์๋ฅผ ์ด์ฉํ์ฌ ์ฝ๋๋ฅผ ์๋ ฅํ๊ณ  ๋ค์๊ณผ ๊ฐ์ด ์ถ๋ ฅ๋๊ฒ ํ์ธ์.

  

๋ฐ์ดํฐ

var arr = [200, 100, 300];

//pass

console.log(arr);

  

์ถ๋ ฅ

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

### ๐ For_and_While

  

<br>

  

### ๋์ด๋ : ๐ถ

  

<br>

  

#### โ๏ธ for๋ฌธ ๊ณ์ฐ

  
  

```javascript

๋ค์ ์ฝ๋์ ์ถ๋ ฅ ๊ฐ์ผ๋ก ์๋ง์ ๊ฒ์?

  

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

  

#### โ๏ธ ๋ณ ์ฐ๊ธฐ

  
  

```javascript

ํฌ๋ฆฌ์ค๋ง์ค ๋ , ์๋น๋ ์น๊ตฌ๋ค๊ณผ ํจ๊ป ํํฐ๋ฅผ ํ๊ธฐ๋ก ํ์ต๋๋ค. ๊ทธ๋ฐ๋ฐ, ํฌ๋ฆฌ์ค๋ง์ค ํธ๋ฆฌ๋ฅผ ์ฌ๋ ๊ฒ์ ๊น๋นกํ๊ณ  ๋ง์์ต๋๋ค. ์จ ๊ฐ๊ฒ๋ฅผ ๋์๋ค๋ ๋ดค์ง๋ง ํฌ๋ฆฌ์ค๋ง์ค ํธ๋ฆฌ๋ ๋ชจ๋ ํ์ ์ด์์ต๋๋ค.

ํ๋ ์ ์์ด ์๋น๋ ํ๋ก๊ทธ๋๋ฐ์ผ๋ก ํธ๋ฆฌ๋ฅผ ๋ง๋ค๊ธฐ๋ก ํฉ๋๋ค.

  

์๋น๋ฅผ ์ํด ํ๋ก๊ทธ๋จ์ ์์ฑํด ์ฃผ์ธ์.

  

์๋ ฅ

5


์ถ๋ ฅ
*
***
*****
*******
*********

  

````

  
  

<details><summary><b>Answer</b></summary>

  

<p>

  

```javascript

const n = prompt('์ซ์๋ฅผ ์๋ ฅํ์ธ์.');

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

### ๐ Basic

  

<br>

  

### ๋์ด๋ : ๐ถ

  

<br>

  

#### โ๏ธ False

  
  

```javascript

๋ค์์ ์๋ฐ์คํฌ๋ฆฝํธ ๋ฌธ๋ฒ ์ค์์ False๋ก ์ทจ๊ธํ๋ ๊ฒ๋ค ์๋๋ค.

์, False๋ก ์ทจ๊ธํ์ง ์๋ ๊ฒ์ด ํ๋ ์๋ค์! **True๋ฅผ ์ฐพ์์ฃผ์ธ์.**

  

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

  

#### โ๏ธ ๊ฐ์ฒด์ ํค ์ด๋ฆ ์ค๋ณต

  
  

```javascript

์๋ฐ์คํฌ๋ฆฝํธ ๊ฐ์ฒด๋ฅผ ๋ค์๊ณผ ๊ฐ์ด ๋ง๋ค์๋ค.

์ถ๋ ฅ๊ฐ์ ์๋ ฅํ์์ค. (์ถ๋ ฅ๊ฐ์ ๊ณต๋ฐฑ์ ๋ฃ์ง ์์ต๋๋ค. )

  

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

// ๋ง์ง๋ง ๊ฐ์ ์ถ๋ ฅํ๋ค.

````

  

</p>

</details>

<br>

<br>


<br>

  

#### โ๏ธ concat์ ํ์ฉํ ์ถ๋ ฅ๋ฐฉ๋ฒ

  
  

```javascript

๋ค์ ์์ค ์ฝ๋๋ฅผ ์์ฑํ์ฌ ๋ ์ง์ ์๊ฐ์ ์ถ๋ ฅํ์์ค.

  

๋ฐ์ดํฐ

var year = '2019';

var month = '04';

var day = '26';

var hour = '11';

var minute = '34';

var second = '27';

  

var result = //๋น์นธ์ ์ฑ์์ฃผ์ธ์

  

console.log(result);

  
  

์ถ๋ ฅ

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


