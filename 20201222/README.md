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
# ✌20201225
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
```js
alert(prompt('당신의 나이는?')) // 먼저 '당신의 나이는?' 경고창이 뜬 후 결과값을 
                                // 넣으면 결과값이 경고창에 뜸

```
```html
<html>
<head>
    <meta charset="utf-8"/>
</head>
<body>
    <script>
        id = prompt('아이디를 입력해주세요.')
        if(id=='egoing'){                    
            alert('아이디가 일치 합니다.')     //입력값에 따라 결과가 다르게 나옴
        } else {
            alert('아이디가 일치하지 않습니다.')
        }
    </script>
</body>
</html>
```

- 로그인

```html
<html>
<head>
    <meta charset="utf-8"/>
</head>
<body>
    <script>
        id = prompt('아이디를 입력해주세요.')
        if(id=='4win1'){
        	var password = prompt('비밀번호를 입력해주세요');
        	if(password == '111111'){
        		alert('로그인 하셨습니다.'+id+'님 반값습니다.');
        	} else {
        		alert('비밀번호가 다릅니다.')
        	}
        } else {
            alert('아이디가 일치하지 않습니다.') 
        }
    </script>
</body>
</html>
```

- 논리연산자 

-  **&&**(and연산자) : 좌항과 우항이 모두 참일 때에만 참이 된다. 

```js
if(true && true)     //true
if(true && false)    //false
if(false && true)    //false 
if(false && false)   //false
```
- &&의 활용

```html
<html>   
<head>
    <meta charset="utf-8"/>  
</head>
<body>
    <script>
        var id = prompt('아이디를 입력해주세요.')
        var password = prompt('비밀번호를 입력해주세요');
        if(id=='egoing' && password == '111111'){
        		alert('로그인 하셨습니다.'+id+'님 반값습니다.');
        } else {
            alert('아이디가 일치하지 않습니다.')  
        }//위의 로그인과 완벽하게 일치하는 코드는 아니지만 논리연산자롤 활용하여 바꿀 수 있다. 
    </script>
</body>
</html>
```

- ||(or연산자) : 좌항과 우항 중 하나라도 true라면 true가 되는 연산자다. 

```js
if(true || true){
    alert(1);
}                   //1
if(true || false){
    alert(2);
}                   //2
if(false || true){
    alert(3);
}                   //3
if(false || false){
    alert(4);
}                   //실행안됨
```                 
- ||의 활용

```html
<html>
<head>
    <meta charset="utf-8"/>
</head>
<body>
    <script>
       id = prompt('아이디를 입력해주세요.');
if(id==='4win1' || id==='승원' || id==='saseungwon'){
    alert('인증 했습니다.');
} else {
    alert('인증에 실패 했습니다.');
}
    </script>
</body>
</html>
```
```html
<html>
<head>
    <meta charset="utf-8"/>
</head>
<body>
    <script>
       id = prompt('아이디를 입력해주세요.');
password = prompt('비밀번호를 입력해주세요.');
if(id==='4win1' || id==='승원' || id==='saseungwon'){ && password==='111111'){
    alert('인증 했습니다.');
} else {
    alert('인증에 실패 했습니다.');
}
    </script>
</body>
</html>
```
- ! : 부정의 의미, Boolean 값을 역전시킨다. true를 false로 false를 true로 만든다.

```js
if(!true && !true){
    alert(1);
}                       //실행안됨
if(!false && !true){
    alert(2);
}                       //실행안됨
if(!true && !false){
    alert(3);
}                       //실행안됨
if(!false && !false){
    alert(4);
}                       //4
```

- false로 간주되는 데이터 형
```js
if(!''){alert('빈 문자열')}
if(!undefined){alert('undefined');}
var a; if(!a){alert('값이 할당되지 않은 변수'); }
if(!null){alert('null');}
if(!NaN){alert('NaN');}
```


# ✌20201226
## 📚반복문(loop, iterate)

- while

```js
while (조건){
    반복해서 실행할 코드 //true에서 false가 될 때까지 반복해서 실행한다. 
}
```
```js
while(true){  
    document.write('coding everybody <br />');  // <br /> : 줄바꿈
}   //true에서 끝나면 무한loop에 빠지기 때문에 적당한 시점에 false로 바뀌어야 한다. 
```

- 반복조건

```html
<html>
<head>
    <title></title>
</head>
<body>
    <script type="text/javascript">
		var i = 0;
		while(i < 10){// 종료조건으로 i의 값이 10보다 작다면 true, 같거나 크다면 false가 된다.
    		document.write('coding everybody <br />');// 반복이 실행될 때마다 coding everybody <br />이 출력된다.
   			 i = i + 1;
}
    </script>
</body>
</html>
```

- **for**

```js
for(초기화; 반복조건; 반복이 될 때마다 실행되는 코드){
    반복해서 실행될 코드
}
```
```html
<html>
<head>

</head>
<body>
    <script type="text/javascript">
    /*
		var i = 0;/
		while(i < 10){
    		document.write('coding everybody <br />');
   		 i = i + 1;
         i++; 는  i=i+1; 과 같음. 
}	*/
	for(var i = 0; i < 10; i = i + 1){ //맨끝에는 세미콜론 쓰면 안됨
    	document.write('coding everybody'+i+'<br />');
}
    </script>
</body>
</html>
```
- i의 값이 0이다.
- 실행이 되면 i의 값이 1씩 증가한다. 
- i의 값이 10이 되었을 때 false가 된다.
```js
for
(var i = 0;         //초기화
i < 10;             //반복조건
i = i + 1)          //반복이 될 때마다 실행되는 코드
```
```html
<html>
<head>

</head>
<body>
    <script type="text/javascript">
    for(var i = 0; i < 1000; i++){
    	document.write('coding everybody'+(i*2)+'<br />');
}   //반복문을 사용하면 사람의 한계를 극복할 수 있다. 

    /*
    	document.write("coding everybody 1 <br />" );
    	document.write("coding everybody 2 <br />" );
    	document.write("coding everybody 3 <br />" );
    	document.write("coding everybody 4 <br />" );
    	document.write("coding everybody 5 <br />" );
    	document.write("coding everybody 6 <br />" );
    	document.write("coding everybody 7 <br />" );
    	document.write("coding everybody 8 <br />" );
    	document.write("coding everybody 9 <br />" );
    	document.write("coding everybody 10 <br />" );
		*/

    /*
		var i = 0;/
		while(i < 10){
    		document.write('coding everybody <br />');
   		 i = i + 1;
}	
	for(var i = 0; i < 10; i = i + 1;){
    	document.write('coding everybody'+i+'<br />');
}	*/
    </script>
</body>
</html>
```

### 반복문의 제어
- break : 현재의 반복문을 완전히 종료시키고 반복문 바깥으로 빠져나가라. 반복작업을 중간에 중단시키고 싶을 때에 사용

```html
<html>
<head> 

</head>
<body>
    <script type="text/javascript">
   for(var i = 0; i < 10; i++){
    if(i === 5) {                   //i의 값이 5가 되었을 때 break가 실행된다. 
        break;                      // 01234
    }
    document.write('coding everybody'+i+'<br />');
}
    </script>
</body>
</html>
```
- continue : 지정한 그 순간에만 종료시키고 반복문을 계속 실행시킨다. 

```html
<html>
<head>

</head>
<body>
    <script type="text/javascript">
   for(var i = 0; i < 10; i++){
    if(i === 5) {
        continue;                   //5에서 중지되고 다시 반복문을 계속한다.
    }
    document.write('coding everybody'+i+'<br />');
}
    </script>
</body>
</html>
```