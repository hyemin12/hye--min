# Javascript 함수

## \* 산술 연산자(arithmetic operator)

```javascript
console.log(1 + 2);
console.log(5 - 7);
console.log(3 * 4);
console.log(10 / 2);
console.log(7 % 5); //나머지 값
```

---

## \* 할당 연산자(assignment operator)

```javascript
let a = 2;
a = a + 1;
a += 1;

console.log(a);
```

---

## \* 비교 연산자(comparison operator)

```javascript
const a = 1;
const b = 1;

console.log(a <= b);
```

- == 일치 연산자(같은 것을 확인해주는 연산자)
- !== 불일치 연산자(다른 것을 확인해주는 연산자)
- < , > , >= , <= 비교 연산자(크기 비교하는 연산자)  
  → true false로 출력됨

---

## \* 논리 연산자(logical operator)

```javascript
const a = 1 === 1;
const b = "AB" === "AB";
const c = true;

console.log("&&: ", a && b && c);
console.log("||: ", a || b || c);
console.log("!: ", !a);
```

- \*&& : 그리고, and 연산자 "모두" 같은 값인지 확인하는 연산자
- || : 또는 or 연산자 하나만 true 여도 true로 나옴
- ! : 부정 연산자 not 연산자

---

## \* 삼항 연산자(ternary operator)

```javascript
const a = 1 < 2;

if (a) {
  console.log("참");
} else {
  console.log("거짓");
}

console.log(a ? "참" : "거짓");
```

? 앞 값이 true 인지 아닌지 | true면 : 앞 / 거짓이면 : 뒤 실행

---

## \* 조건문 If

```javascript
import random from "./getRandom";
//따로 작성한 getRandom.js 파일 연결

const a = random();

if (a === 0) {
  console.log("a is 0");
} else if (a === 2) {
  //추가적인 조건
  console.log("a is 2");
} else if (a === 4) {
  //추가적인 조건
  console.log("a is 4");
} else {
  console.log("rest...");
}
```

---

## \* 조건문 switch

```javascript
import random from "./getRandom";

const a = random();

switch (a) {
  case 0:
    console.log("a is 0");
    break;
  case 2:
    console.log("a is 2");
    break;
  case 4:
    console.log("a is 4");
    break;
  default: //나머지인 경우
    console.log("rest...");
}
```

---

## \* 반복문 For

for (시작조건; 종료조건; 변화조건) {}

```javascript
const ulEl = document.querySelector("ul");

for (let i = 0; i < 10; i += 1) {
  const li = document.createElement("li");
  li.textContent = `list-${i + 1}`;
  if ((i + 1) % 2 === 0) {
    li.addEventListener("click", function () {
      console.log(li.textContent);
    });
  }
  ulEl.appendChild(li);
}
```

---

### \* 변수 유효범위(variable Scope)

```javascript
 var 함수 레벨의 유효 범위를 가진다.
 let, const 블록 레벨의 유효 범위를 가진다.

 function scope() {
   if (true) {
     const a = 123
     console.log(a)
   }
 }
 scope()
```

---

## \* 형 변환(Type conversion)

```javascript
const a = 1
const b = '1'

console.log(a == b)

== 동등 연산자 / 형 변환이 이루어짐

* Truthy(참 같은 값)
true, {}, [], 1, 2, 'false', -12, '3.14' ...

* Falsy(거짓 같은 값)
false, '', null, undefined, 0 ,-0, NaN(숫자아닐 때)

if ('false') {
  console.log(123)
}
```

---

## \* 함수복습

```javascript
function sum(x, y) {
  return x + y;
}
const a = sum(1, 3);
const b = sum(4, 12);

console.log(sum(1, 3));
console.log(sum(4, 12));
console.log(sum(1, 3) + sum(4, 22));

function sum() {
  console.log(arguments); //함수 안에서 언제든지 사용할 수 있도록 설계
  return arguments[0] + arguments[1];
}

console.log(sum(7, 3));
```

---

## \* 화살표 함수

() => {} vs function () {}
일부 생략해서 축약해서 사용 할 수 있음

```javascript
const double = function (x) {
  return x * 2
}
console.log('double:', double(7))

const doubleArrow = (x) => {
  return x * 2
}
const doubleArrow = x => {
  return x * 2
}
const doubleArrow = x => x * 2
//매개변수 1개면 소괄호도 생략 가능
console.log('doubleArrow', doubleArrow(7))

ex)
const doubleArrow = x => ({name:'hyemin'})
const doubleArrow = x => 123
const doubleArrow = x => null
const doubleArrow = x => undefined
```

---

## \*즉시실행함수

IIFE/Immediately-Invoked Function Expression
즉시 실행함수 문법

1. (function () {})()
2. (function(){}()) \* 권장

```javascript
const a = 7;
function double() {
  console.log(a * 7);
}
double();

(function () {
  console.log(a * 2);
})();

(function () {
  console.log(a * 2);
})();
```

---

## \* 호이스팅(Hoistiong)

함수 선언부가 유효범위 최상단으로 끌어올려지는 현상

```javascript
const a = 7

const double = function () {
  console.log(a * 2)
}
double()

-- hoisting --
double()
function double() {
  console.log(a * 2)
}
```

---

## \* 타이머함수

- setTimeout(함수, 시간): 일정 시간 후 함수 실행
- setInterval(함수, 시간): 시간 간격마다 함수 실행
- clearTimeout(): 설정된 Timeout 함수를 종료
- clearInterval(): 설정된 Interval 함수를 종료

```javascript
setTimeout(() => {
  console.log("hyemin");
}, 3000);

const timer = setInterval(() => {
  console.log("hyemin");
}, 3000);

const h1El = document.querySelector("h1");
h1El.addEventListener("click", () => {
  clearInterval(timer);
});
//h1 태그 클릭시 clearInterval 함수 종료
```

---

## \* 콜백(callback)

함수의 인수로 사용되는 함수

```javascript
setTimeout(함수, 시간);

function timeOut(cb) {
  setTimeout(() => {
    console.log("hyemin");
    cb();
  }, 3000);
}
timeOut(() => {
  //화살표 함수
  console.log("Done!");
});
//콜백함수
```

---

# JS 클래스

## \* 생성자 함수

```javascript
function user(first, last) {
  this.firstName = first
  this.lastName = last
}
user.prototype.getFullName = function () {
  return `${this.firstName} ${this.lastName}`
}
//통일화 해서 메모리 관리를 편리하게 할 수 있음

const hyemin = new user('Hyemin', 'Ko')
const amy = new user('Amy', 'Kim')
const neo = new user('Neo', 'City')
// user :생성자 함수 / 하나의 객체 데이터가 생성

console.log(hyemin.getFullName())
console.log(amy.getFullName())
console.log(neo.getFullName())

const hyemin = {} , [] //리터럴 방식
```

---

## \* this

일반(Normal) 함수는 호출 위치에서 따라 this 정의!
화살표(Arrow) 함수는 자신이 선언된 함수 범위에서 this 정의!

```javascript
const hyemin = {
  name: 'Hyemin',
  normal: function () {
    console.log(this.name)
  },
  arrow: () => {
    console.log(this.name)
  }
}
hyemin.normal()  //출력: hyemin
hyemin.arrow() //출력: undefined

const amy = {
  name: 'Amy',
  normal: hyemin.normal,
  arrow: hyemin.arrow
}
amy.normal()  //출력: amy
amy.arrow() //출력: undefined

--------------------------------------------------

function User(name) { //생성자함수(대문자로 시작)
  this.name = name
}
User.prototype.normal = function () {
  console.log(this.name)
}
User.prototype.arrow = () => {
  console.log(this.name)
}

const neo = new User ('Neo city')

neo.normal() //출력: Neo city
neo.arrow() //출력: undefined

const timer = {
  name: 'time',
  timeout: function () {
    setTimeout(() => {
      console.log(this.name)
    }, 2000)
  }
}

timer.timeout() //출력: time

//화살표 함수를 감싸고 있는 메소드 정의할 때 사용한 함수가 있어서 this가 정의 되어 화살표 함수 결과값이 출력됨
//timer 함수 사용할 때는 콜백함수보다 화살표 함수를 사용하는 것이 더 좋음

------------------------------------------------

const jeno = {
  name: 'jeno',
  normal() {
    console.log(this.name)
  },
  //normal: function (){} -> 객체데이터 내부에서 일반 함수를 사용할때는 normal 부분에서는 콜론, function 생략 가능
  arrow: () => {
    console.log(this.name)
  }
}

jeno.normal()
jeno.arrow()
```

---

## \* ES6 Classes

javascript에서 사용하는 class

```javascript
function User(first, last) {
  this.firstName = first;
  this.lastName = last;
}
User.prototype.getFullName = function () {
  return `${this.firstName} ${this.lastName}`;
};

// 클래스 키워드 문법으로 변경
class User {
  constructor(first, last) {
    this.firstName = first;
    this.lastName = last;
  }
  getFullName() {
    return `${this.firstName} ${this.lastName}`;
  }
}

const jisung = new User("Jisung", "Park");
const lele = new User("Chenle", "Zhong");
const jeddong = new User("Jeddong", "Lee");

console.log(jisung);
console.log(lele.getFullName());
console.log(jeddong.getFullName());
```

---

## \* 상속(확장)

```javascript
class Vehicle {
  constructor(name, wheel) {
    this.name = name;
    this.wheel = wheel;
  }
}
const myVehicle = new Vehicle("운송수단", 2);
console.log(myVehicle);

class Bicycle extends Vehicle {
  constructor(name, wheel) {
    super(name, wheel);
    //확장된 클래스 Vehicle
  }
}
const myBicycle = new Bicycle("삼천리", 2);
const daughterBicycle = new Bicycle("세발", 3);

console.log(myBicycle);
console.log(daughterBicycle);

class Car extends Vehicle {
  constructor(name, wheel, license) {
    super(name, wheel);
    this.license = license;
    //확장 (추가적인 내용 일부만 작성)
  }
}
const myCar = new Car("벤츠", 4, true);
const daughterCar = new Car("벤틀리", 4, false);

console.log(myCar);
console.log(daughterCar);
```
