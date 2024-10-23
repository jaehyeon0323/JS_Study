# ES6 (2015) 주요 문법

## let과 const
var 대신에 변수를 선언하는 방법.
`let`: 값이 변경될 수 있는 변수를 선언.
`const`: 값이 변경되지 않는 상수를 선언.
```javascript
`let age` = 25;
`const name` = "Jaehyeon";
console.log(age); // 25
console.log(name); // "Jaehyeon"
```

## 화살표 함수 (Arrow Functions)
더 짧고 간결하게 함수를 작성할 수 있는 방법.
```javascript
//기존 방법_함수 선언문
function add(a, b) {
  return a + b;
}

//기존 방법_함수 표현식
const add = function(a, b) {
  return a + b;
};

//화살표 함수
const add = (a, b) => a + b;

console.log(add(2, 3)); // 5
```

## 템플릿 리터럴 (Template Literals)
백틱(`)을 사용하여 문자열을 쉽게 작성하고 변수나 표현식을 포함할 수 있음.
```javascript
const name = "Jaehyeon";
const greeting = `Hello, ${name}!`;
console.log(greeting);
//Hello, Jaejyeon!
```

## 디스트럭처링 (Destructuring)
배열이나 객체의 값을 쉽게 추출할 수 있는 방법
```javascript
// 배열 디스트럭처링
const [x, y] = [1, 2];
console.log(x); // 1
console.log(y); // 2

// 객체 디스트럭처링
const person = { name: "Jaehyeon", age: 30 };
const { name, age } = person;
console.log(name); // "Jaehyeon"
console.log(age); // 25
```

## 기본 매개변수 (Default Parameters)
함수의 매개변수에 기본값을 설정할 수 있음
```javascript
function greet(name = "jaehyeon") {
  return `Hello, ${name}`;
}
console.log(greet()); // "Hello, jaehyeon"
console.log(greet("myoung")); // "Hello, myoung"
```

## import와 export
모듈 시스템을 통해 코드 파일 간에 기능을 공유하는 방법.
```javascript
// 파일1 (모듈 내보내기)
export const pi = 3.14;

// 파일2 (모듈 가져오기)
import { pi } from './math.js';

console.log(pi); // 3.14
```

# ES7 (2016) 주요 문법

## 지수 연산자 (Exponentiation Operator)
Math.pow() 대신 ** 연산자를 사용하여 지수를 계산할 수 있음
```javascript
const square = 2 ** 3; // 8
console.log(square); // 8
```

## Array.prototype.includes
배열에 특정 값이 포함되어 있는지 확인할 수 있는 메서드.
```javascript
const arr = [1, 2, 3];
arr.includes(2); // true
console.log(arr.includes(2)); // true
console.log(arr.includes(4)); // false
```
# ES8 (2017) 주요 문법
## async와 await
비동기 코드를 동기적으로 작성할 수 있게 해주는 문법. async 함수는 자동으로 프로미스를 반환하고, await은 프로미스가 해결될 때까지 기다림.
```javascript
코드 복사
async function fetchData() {
  const response = await fetch('https://api.example.com');
  const data = await response.json();
  return data;

fetchData().then(data => console.log(data)); // "Data loaded!"
}
```
## Object.entries()와 Object.values()
객체의 키-값 쌍 또는 값만 배열로 반환하는 메서드.
```javascript
const person = { name: "Jaehyeon", age: 25 };
// Object.entries: [['name', 'Jaehyeon'], ['age', 25]]
console.log(Object.entries(person));
// Object.values: ['Jaehyeon', 25]
console.log(Object.values(person));
```

## 문자열 패딩 (String Padding)
padStart()와 padEnd()로 문자열의 시작 또는 끝에 원하는 만큼의 공백이나 문자를 추가할 수 있음.
```javascript
'5'.padStart(2, '0'); // '05'
'5'.padEnd(2, '0');   // '50'
```