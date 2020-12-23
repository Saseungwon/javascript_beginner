# ✌ 20201222 
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

## 📚 문자에 대한 명령들
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

## 📚 변수사용법
 - 변수 : 문자, 숫자 같은 값을 담는 컨테이너로 값을 유지할 필요가 있을 때 사용한다. 여기에 담겨진 값은 다른 값으로 바꿀 수 있다. 대명사와 비슷한 역할을 한다. 

 - 변수의 선언 : 자바스크립트에서 변수는 var로 시작한다. 처음 변수를 사용할 때는 앞에 var 붙여주고 그 다음부터 사용할 때는 이미 변수를 만들었기 때문에 var을 사용하지 않아도 된다. 

``` js
var a = 1; // 1
alert(a);  // 1

a = 10;
10
alert(a); // 10

a=1;
1
b=2;
2
alert(a+b); // 3

a=2;
2
alert(a+b);  // 4
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