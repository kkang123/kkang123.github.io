---
layout: post
title: 자바와 자바스크립트의 차이
tags: [javascript]
categories: javascript
---

# 자바와 자바스크립트의 차이

|자바|자바스크립트|
|---|---|
|컴파일 언어|인터프리터 언어|
|타입 검사를 엄격하게 함|	타입을 명시하지 않음|
|클래스(class) 기반의 객체 지향 언어|	프로토타입(prototype) 기반의 객체 지향 언어|

# 자바스크립트의 기본 타입

원시 타입(primitive type)은 다음과 같다.

 

1. 숫자(number)

2. 문자열(string)

3. 불리언(boolean)

4. 심볼(symbol) : ECMAScript 6부터 제공됨

5. undefined

<br>

- 객체 타입(object type)

6. 객체(object)
```js
var num = 10;          // 숫자

var myName = "홍길동"; // 문자열

var str;               // undefined
```

<br>

- 숫자(number)

자바스크립트는 다른 언어와는 달리 정수와 실수를 따로 구분하지 않고, 모든 수를 실수 하나로만 표현합니다.  
또한, 매우 큰 수나 매우 작은 수를 표현할 경우에는 e 표기법을 사용할 수 있습니다.
```js
var firstNum = 10;     // 소수점을 사용하지 않은 표현

var secondNum = 10.00; // 소수점을 사용한 표현

var thirdNum = 10e6;   // 10000000

var fourthNum = 10e-6; // 0.00001
```

<br>

- 문자열(string)

자바스크립트에서 문자열은 큰따옴표("")나 작은따옴표('')로 둘러싸인 문자의 집합을 의미합니다.  
큰따옴표는 작은따옴표로 둘러싸인 문자열에만 포함될 수 있으며, 작은따옴표는 큰따옴표로 둘러싸인 문자열에만 포함될 수 있습니다.
```js
var firstStr = "이것도 문자열입니다.";      // 큰따옴표를 사용한 문자열

var secondStr = '이것도 문자열입니다.';     // 작은따옴표를 사용한 문자열

var thirdStr = "나의 이름은 '홍길동'이야."  // 작은따옴표는 큰따옴표로 둘러싸인 문자열에만 포함될 수 있음.

var fourthStr = '나의 이름은 "홍길동"이야.' // 큰따옴표는 작은따옴표로 둘러싸인 문자열에만 포함될 수 있음.
```

<br>

`자바스크립트에서는 숫자와 문자열을 더할 수도 있습니다.`

이럴 경우에 자바스크립트는 숫자를 문자열로 자동 변환하여, 두 문자열을 연결하는 연산을 수행합니다.
```js
var num = 10;

var str = "JavaScript";

document.getElementById("result").innerHTML = (num + str); // 10JavaScript

```

<br>

- 불리언(boolean)  

불리언 값은 참(true)과 거짓(false)을 표현합니다.

```js
var firstNum = 10;

var secondNum = 11;

document.getElementById("result").innerHTML = (firstNum == secondNum); // false
```

<br>

- 심볼(symbol)

심볼 타입은 ECMAScript 6부터 새롭게 추가된 타입입니다.  
심볼은 유일하고 변경할 수 없는 타입으로, 객체의 프로퍼티를 위한 식별자로 사용할 수 있습니다.
```js
var sym = Symbol("javascript");  // symbol 타입

var symObj = Object(sym);        // object 타입
```
`심볼 타입은 익스플로러에서 지원하지 않습니다.`

<br>

- typeof 연산자

typeof 연산자는 피연산자의 타입을 반환하는 피연산자가 단 하나뿐인 연산자입니다.
```js
typeof 10;        // number 타입

typeof "문자열";  // string 타입

typeof true;      // boolean 타입

typeof undefined; // undefined 타입

typeof null;      // object 타입

```

- null과 undefined

자바스크립트에서 null이란 object 타입이며, 아직 '값'이 정해지지 않은 것을 의미합니다.  

또한, undefined란 null과는 달리 '타입'이 정해지지 않은 것을 의미합니다.  

따라서 자바스크립트에서 undefined는 초기화되지 않은 변수나 존재하지 않는 값에 접근할 때 반환됩니다.

```js
var num;          // 초기화하지 않았으므로 undefined 값을 반환함.

var str = null;   // object 타입의 null 값

typeof secondNum; // 정의되지 않은 변수에 접근하면 undefined 값을 반환함.

```

null과 undefined는 동등 연산자(==)와 일치 연산자(===)로 비교할 때 그 결괏값이 다르므로 주의해야 합니다.

null과 undefined는 타입을 제외하면 같은 의미지만, 타입이 다르므로 일치하지는 않습니다.
```js
null ==  undefined; // true

null === undefined; // false
```

- 객체(object)

자바스크립트의 기본 타입은 객체(object)입니다.

객체(object)란 실생활에서 우리가 인식할 수 있는 사물로 이해할 수 있습니다.

객체는 여러 프로퍼티(property)나 메소드(method)를 같은 이름으로 묶어놓은 일종의 집합체입니다.

```js
var dog = { name: "해피", age: 3 }; // 객체의 생성

// 객체의 프로퍼티 참조

document.getElementById("result").innerHTML =

    "강아지의 이름은 " + dog.name + "이고, 나이는 " + dog.age + "살 입니다.";
```

---

# 타입변환(type conversion)
자바스크립트는 타입 검사가 매우 유연한 언어입니다.

자바스크립트의 변수는 타입이 정해져 있지 않으며, 같은 변수에 다른 타입의 값을 다시 대입할 수도 있습니다.

```js
var num = 20; // Number 타입의 20

num = "이십"; // String 타입의 "이십"

var num;      // 한 변수에 여러 번 대입할 수는 있지만, 변수의 재선언은 할 수 없습니다. 재선언문은 무시됩니다.
```

- 묵시적 타입 변환(implicit type conversion)

자바스크립트는 특정 타입의 값을 기대하는 곳에 다른 타입의 값이 오면, 자동으로 타입을 변환하여 사용합니다.

즉, 문자열 값이 오길 기대하는 곳에 숫자가 오더라도 자바스크립트는 알아서 숫자를 문자열로 변환하여 사용합니다.
```js
10 + "문자열"; // 문자열 연결을 위해 숫자 10이 문자열로 변환됨.

"3" * "5";     // 곱셈 연산을 위해 두 문자열이 모두 숫자로 변환됨.

1 - "문자열";  // NaN


//위의 세 번째 예제에서 뺄셈 연산을 위해 문자열이 숫자로 변환되어야 하나, 해당 문자열은 두 번째 예제의 문자열과는 달리 숫자로 변환될 수 없는 문자열입니다.

//따라서 의미에 맞게 자동으로 타입을 변환할 수 없으므로, 자바스크립트는 NaN 값을 반환합니다.
```

<br>


- 명시적 타입 변환(explicit type conversion)

자바스크립트에서는 묵시적 타입 변환을 많이 사용하지만, 명시적으로 타입을 변환할 방법도 제공합니다.

명시적 타입 변환을 위해 자바스크립트가 제공하는 전역 함수는 다음과 같습니다.

1. Number()

2. String()

3. Boolean()

4. Object()

5. parseInt()

6. parseFloat()

```js
Number("10"); // 숫자 10

String(true); // 문자열 "true"

Boolean(0);   // 불리언 false

Object(3);    // new Number(3)와 동일한 결과로 숫자 3
```
<br>

- 숫자를 문자열로 변환

숫자를 문자열로 변환하는 가장 간단한 방법은 String() 함수를 사용하는 것입니다.

또한, null과 undefined를 제외한 모든 타입의 값이 가지고 있는 toString() 메소드를 사용할 수도 있습니다.

 

숫자(Number) 객체는 숫자를 문자열로 변환하는 다음과 같은 메소드를 별도로 제공합니다.

 

1. toExponential()

2. toFixed()

3. toPrecision()

|메소드|설명|
|---|---|
|toExponential()|	정수 부분은 1자리, 소수 부분은 입력받은 수만큼 e 표기법을 사용하여 숫자를 문자열로 변환함.|
|toFixed()|	소수 부분을 입력받은 수만큼 사용하여 숫자를 문자열로 변환함.|
|toPrecision()|	입력받은 수만큼 유효 자릿수를 사용하여 숫자를 문자열로 변환함.|

메소드(method)란 객체의 프로퍼티 값으로 함수를 갖는 프로퍼티를 의미합니다.

메소드에 대한 더 자세한 사항은 자바스크립트 객체의 개념 수업에서 확인할 수 있습니다.

<br>

- 불리언 값을 문자열로 변환

불리언 값을 문자열로 변환하는 방법에는 String() 함수와 toString() 메소드를 사용하는 방법이 있습니다.

```js
String(true);     // 문자열 "true"

false.toString(); // 문자열 "false"
```


- 날짜를 문자열이나 숫자로 변환

날짜를 문자열로 변환하는 방법에는 String() 함수와 toString() 메소드를 사용하는 방법이 있습니다.

자바스크립트에서 날짜(Date) 객체는 문자열과 숫자로 모두 변환할 수 있는 유일한 타입입니다.

 

>날짜(Date) 객체는 날짜를 숫자로 변환하는 다음과 같은 메소드를 별도로 제공합니다.


1. getDate() - 날짜 중 일자를 숫자로 반환함. (1 ~ 31)

2. getDay() - 날짜 중 요일을 숫자로 반환함. (일요일 : 0 ~ 토요일 : 6)

3. getFullYear() - 날짜 중 연도를 4자리 숫자로 반환함. (yyyy년)

4. getMonth() - 날짜 중 월을 숫자로 반환함. (1월 : 0 ~ 12월 : 11)

5. getTime() - 1970년 1월 1일부터 현재까지의 시간을 밀리초(millisecond) 단위의 숫자로 반환함.

6. getHours() - 시간 중 시를 숫자로 반환함. (0 ~ 23)

7. getMinutes() - 시간 중 분을 숫자로 반환함. (0 ~ 59)

8. getSeconds() - 시간 중 초를 숫자로 반환함. (0 ~ 59)

9. getMilliseconds() - 시간 중 초를 밀리초(millisecond) 단위의 숫자로 반환함. (0 ~ 999)

