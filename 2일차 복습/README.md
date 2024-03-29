# 객체 

* 객체는 관련된 데이터와 함수(일반적으로 여러 데이터와 함수로 이루어지는데, 객체 안에 있을 때는 보통 프로퍼티와 메소드라고 부릅니다)의 집합 
* 객체를 생성하는 방법 2가지 : 객체 리터럴 사용, 생성자 함수 사용

## 객체 리터럴로 객체 생성하기

* { ... } 부분이 객체 리터럴
* 프로퍼티 값은 suit : “하트” 처럼 콜론(:)을 사용
* 중괄호({})안에 있는 프로퍼티들은 쉼표(,)로 구분
* 변수에 대입된 객체 안의 프로퍼티 값을 읽거나 쓸 때에는 마침표(.) 연산자 또는
* 대괄호 ([]) 연산자를 사용
* 객체 리터럴 안에 어떠한 프로퍼티도 작성하지 않으면 빈 객체가 생성됨

~~~html
var student = { name  : "민재", age : "25" };
undefined

student;
{name: '민재', age: '25'}
~~~



## delete 연산자를 사용하여 프로퍼티 삭제

~~~html
delete student.age;
console.log(student); // Object { suit : “하트”, value : 15 }
VM200:2 {name: '민재'}
~~~

## in 연산자

프로퍼티가 객체에 포함 >> true

프로퍼티가 객체에 포함X >> false

~~~html
console.log("name" in student); 
//true

console.log("age" in student); 
//true

console.log("grade" in student); 
//false
~~~

# 함수

~~~html 
function 함수명 (인수) {   
	처리 로직 
 
   return 출력 반환값
}
~~~

~~~html
function square(x) {    
	var result = x * x; 
	
	return result; 
}  
* 1일차 참조) 함수명 캐멀 표기법 
~~~

인수 

~~~html
function add(a, b) {   
	var c = a + b;
	return c;
}
~~~

* 인수가 여러개면 쉼표로 구분

인수를 받지 않는 함수

~~~html
function animal() {    
	console.log(”동물”); 
};

animal(); // 멍멍 
console.log(animal()); // undefined - 반환값이 없음
~~~

## 변수의 유효범위

### 전역 유효 범위와 지역 유효범위

#### 전역변수

* 함수 바깥에서 선언된 변수
* 유효 범위는 전체 프로그램

### 지역변수

* 함수 안에서 선언된 변수
* 함수 인자
* 유효범위는 변수가 선언된 함수 내부
