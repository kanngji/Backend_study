# 프론트엔드 CSS 라이브러리 비교
- Bootstrap
- Material
- TailwindCSS (인기 많아지고 있음)

# React
- 자바스크립트 라이브러리로 사용자 인터페이스를 만드는데 사용됨
- ex) netflix 서비스
- 전통적인 웹사이트는 무겁다 => request와 html page가 상호작용

# let & const
- let & const는 변수를 생성하는 방법
- let & const를 사용할 것을 권장
- let -> variable values const -> constant values

# Arrow Functions
- const myFnc = () => {

}

# Exports & Imports (Modules)
- 

# Classes
- class Person {
    name = 'Max'
    call =() =>{...}
}
- class Person extends Master

# Classes , Properties & Methods
- 프로퍼티는 클래스와 객체에 추가되는 변수 같은 것
- 메소드는 클래스와 객체에 추가되는 함수

# Spread & Rest Operators
const numbers = [1,2,3];
const newNumbers = [...numbers,4];

console.log(newNumbers) => [1,2,3,4]

const filter = (...args) => {
    return args.filter(el=> el===1);
}

console.log(filter(1,2,3)); => [1]

# Destructuring
- 배열의 원소나 객체의 프로퍼티를 추출해서 변수에 저장할 수 있도록 해줌
const numbers = [1,2,3];
[num1,num2] = numbers;
console.log(num1,num2) => [1,2]

# 참조형 및 원시형 데이터 타입
const number = 1;
const num2 = number;

console.log(num2); => 1

복사하고 싶다면 프로퍼티를 복사해야한다

# 배열 함수 새로 고침
const numbers = [1,2,3];

const doubleNumArray = numbers.map((num)=>{
    return num*2;
});

console.log(doubleNumArray) => [2,4,6]
