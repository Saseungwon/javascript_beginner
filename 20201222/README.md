# ✌20201222 
- `alert`는 **경고창**을 띄울 수 있다.

```html
<html>
<head>
	<title></title>
</head>
<body>
<script type="text/javascript">
	alert(2*8);
</script>
</body>
</html>
```

# ✌20201223 
## 📚 문자의 표현

1. 문자는 반드시 작은따옴표와 작은따옴표 사이, 혹은 큰 따음표와 큰 따옴표 사이에 작성해야함.
2. 따옴표 : 지금부터 나오는 것은 문자야
```html
<html>
<head>
	<title></title>
</head>
<body>
<script type="text/javascript">
	alert("coding everybody");
</script>
</body>
</html>
```
3. 큰 따옴표에서 작은 따옴표로 끝나면 오류 
```js
alert('coding everybody'); // coding everybody 
alert("coding everybody"); // coding everybody

// alert("coding everybody'); // VM96:1 Uncaught SyntaxError: Invalid or unexpected token
alert("coding everybody'") // coding everybody'
```
4. 두 개의 큰 따옴표 사이에 있는 작은 따옴표 하나는 그저 문자로 인식할뿐이다.  
```js
alert("egoing's coding everybody");
// egoing's coding everybody
alert('egoing"s coding everbody');
// egoing"s coding everbody
```
5. 따옴표 사이에 같은 따옴표가 들어가면 뭐하자는거야? 라고 인식해서 오류, 그래서 `\` 역슬래쉬를 붙여줘야함.
 
```js
// 실행 안 됨
// alert('egoing's coding everybody')
// VM402:1 Uncaught SyntaxError: missing ) after argument list
```

6. 역슬래쉬 : 역슬래쉬 바로 뒤에 있는 문자 하나는 그냥 정보로서 해석한다.
7. \'(escape) : 문자로 역할을 해제시킨다. 
```js
alert('egoing\'s coding everybody'); // egoing\'s coding everybody
```
8. 1과 "1" 은 다르다. 1은 숫자, "1"은 문자
``` js
typeof 1
"number"
typeof "1"
"string"
```

## 📚문자에 대한 명령들
   1. 줄바꿈 : \n  

```html
<html>
<head>
	<title></title>
</head>
<body>
<script type="text/javascript">
	alert("coding\neverybody");
</script>
</body>
</html>
```

2. 문자와 문자 결합 : + (codingeverybody)

```html
<html>
<head>
	<title></title>
</head>
<body>
<script type="text/javascript">
	alert("coding"+"everybody");
</script>
</body>
</html>
```
3. 문자와 문자 결합시 공백 만들고 싶을 때 : " "

```html
<html>
<head>
	<title></title>
</head>
<body>
<script type="text/javascript">
	alert("coding"+" "+"everybody");
</script>
</body>
</html>
```

4. 숫자와 문자는 다르다.

```js
1+1
2

"1"+"1"
"11"
```
5. 문자의 수를 세어주는 .length

```js
"coding everybody".length
16
"code".length
4
```

6. stringValue.indexOf(searchValue[,fromIndex]) 
```js
"code".indexOf("c")
0
"code".indexOf("o")
1
"code".indexOf("d")
2
"code".indexOf("e")
3
```

## 📚변수사용법
 - 변수 : 문자, 숫자 같은 값을 담는 컨테이너로 값을 유지할 필요가 있을 때 사용한다. 여기에 담겨진 값은 다른 값으로 바꿀 수 있다. 대명사와 비슷한 역할을 한다. 

 - 변수의 선언 : 자바스크립트에서 변수는 var로 시작한다. 처음 변수를 사용할 때는 앞에 var 붙여주고 그 다음부터 사용할 때는 이미 변수를 만들었기 때문에 var을 사용하지 않아도 된다. 

``` js
var a = 1;   // 1
alert(a);    // 1

a = 10;
10
alert(a);   // 10

a=1;
1
b=2;
2
alert(a+b); // 3

a=2;
2
alert(a+b); // 4
```

- 변수의 값이 꼭 숫자만 올 수 있는 것은 아니다. 문자도 가능

```js
var first='coding';
alert(first + 'everybody');  // codingeverybody

 first = '코딩'
"코딩"
alert(first+'everybody');  // 코딩everybody

var a = 'coding', b = 'everybody';
alert(a+b);  // codingeverybody
```

- 변수는 코드의 재활용성을 높여준다.(유지보수를 쉽게해줌)

```js
a = 100;  // 변할 수 있는 영역

a = a + 10; //
alert(a);
a = a / 10;
alert(a);       변하지 않는 영역
a = a - 10;
alert(a);
a = a * 10;      
alert(a);                          //
```

# ✌20201224
## 📚주석
-  // : 슬래쉬 두 개 뒤에 있는 내용은 주석이니 해석하지 말아라. 
-  잘 만들어진 코드는 좋은 주석을 가지고 있음. 적당하고 적합한 설명이 부가되어있는 코드

```html
<html>
<head>
	<title></title>
</head>
<body>
<script type="text/javascript">
	// 실습용 코드 입니다. (이처럼 도움말을 줄때 사용 가능)
	alert(1+2); // 결과 : 3
</script>
</body>
</html>
```

- /*   */ : 여러 줄을 주석으로 사용 가능

```html
<html>
<head>
	<title></title>
</head>
<body>
<script type="text/javascript">
	/*
		여러줄을
		주석으로
		사용가능 
	*/
</script>
</body>
</html>
```

- 어떤 코드를 일시적으로 동작하지 않게 할 때도 주석을 사용

```html
<html>
<head>
	<title></title>
</head>
<body>
<script type="text/javascript">
	//alert(1+2);
</script>
</body>
</html>
```

## 📚줄바꿈과 여백
- ";"(세미콜론) : 명령이 끝났다라는 것을 명시적으로 표시할 때 쓰는 기호
- 두 줄에 각각 하나의 명령씩만 있으면 작동이 되지만 한 줄에 두 개의 명령이 있으면 반드시 세미콜론을 써야함.

```html
<html>
<head>
	<title></title>
</head>
<body>
<script type="text/javascript">

	var a = 1
	0alert(a)

	var a = 1; alert(a); // 한 줄에 두개의 명령..반드시 세미콜론을 써야함 

</script>
</body>
</html>
```

## 📚비교
- 연산자란?
  1. 연산자 : 어떤 작업을 컴퓨터에게 지시하기 위한 기호 ex) a = 1
  2. 대입 연산자 : a = 1 -->  여기서 "="
  3. 비교 연산자 : 결과는 true, false 중 하나다. true, false는 블린(boolean)이라고 불리는 데이터 형식


- ==(동등연산자, equal operator) : 좌항과 우항을 비교해 값이 같으면 true, 다르면 false
```js
alert(1==2)             //false
alert(1==1)             //true
alert("one"=="two")     //false 
alert("one"=="one")     //true
```

- *===*(일치 연산자, strict equal operator) : 좌항과 우항이 정확하게 같을 때 true
-  == 보다는 ===를 사용하는 것을 강력 추천. ==는 쓰지말자.
```js
alert(1=='1');          //true
alert(1==='1');         //false
```
- **null**  vs  **undefined**
	1. null : 값이 없다.(프로그래머의 의도O)
	2. undefined : 값이 없다. (프로그래머의 의도X)
```js
alert(null == undefined);       //true
alert(null === undefined);      //false
```

- 데이터타입 정리
  
  1. boolean : true / false
  2. number : ... -1, 0, 1, 2, 3...
  3. string : "a"  "b" "c"
  4. undefined : undefined
  5. null : null

- 자바스크립트에서 동등연산자(==)는  숫자 1을 true로 간주한다. 숫자 1이 아닌 수는 false
```js
alert(true == 1);               //true
alert(true == 2);               //false
alert(true == 3);               //false

alert(true === 1);              //false

alert(0 === -0);                //true
alert(NaN === NaN);             //false  0/0(계산할 수 없음)
```

- **!** : 부정을 의미한다. !=는 ==와 정반대의 결과를 보여준다.

```js
alert(1!=2);            //true
alert(1!=1);            //false
alert("one"!="two");    //true
alert("one"!="one");    //false
```
- /  > : 좌향이 우향보다 크면 true, 아니면 false 
```js
alert(10>20);   //false
alert(10>1);    //true
alert(10>10);   //false
```
- /  >= :  좌항이 우항보다 크거나 같다.

```js
alert(10>=20);      //false
alert(10>=1);       //true
alert(10>=10);      //true
```

## 📚조건문

- 조건문 : 주어진 조건에 따라서 에플리케이션을 다르게 동작하도록 하는 것이다. 
- **if(true)** : 중괄호 안쪽에 있는 부분이 실행됨

```js
if(true){
	alert('result : true');  //true
}

if(true){
    alert(1);
    alert(2);
    alert(3);
    alert(4);
}
alert(5);                    //12345 출력
```
- **if(false)** : 중괄호 안쪽에 있는 부분이 무시됨
 ```js
if(false)){
	alert('result : true');  //아무것도 출력되지않음
}

if(false){
    alert(1);
    alert(2);
    alert(3);
    alert(4);
}
alert(5);                    //5 출력, false이므로 중괄호 구간이 실행되지 않는다. 
```

- **else** : 참일 때는 어떤 일을 하고, 거짓일 때는 어떤 일을 한다라는 것을 지정해준다.

``` js
if(true){
    alert(1);
} else {
    alert(2);
}                  //1

if(false){
    alert(1);
} else {
    alert(2);
}                  //2
```
- **else if** : 앞쪽에 있는  if가 실행되지 않았을 때 else if(true)가 실행됨.

```js
if(false){
    alert(1);      //false : 건너뜀
} else if(true){
    alert(2);      //2
} else if(true){
    alert(3);      //true지만 앞쪽에 나오는 조건구문이 실행되었기 때문에 건너뜀
} else {
    alert(4);
}
```
```js
if(false){         
    alert(1);      //false : 건너뜀
} else if(false){  
    alert(2);      //false : 건너뜀
} else if(true){
    alert(3);      //3
} else {
    alert(4);
}
```
```js
if(false){
    alert(1);      //false : 건너뜀
} else if(false){
    alert(2);      //false : 건너뜀
} else if(false){
    alert(3);      //false : 건너뜀
} else {
    alert(4);      //4
}
```

   
   - prompt(''); : 어떠한 값을 사용자로부터 받을 수 있는 기능

```js
prompt('당신의 나이는?');
"25"
```