~~~html
function f() {
	console.log(a); // undefined -> 끌어올리지 않는다면 Reference Error 발생
	var a = "local";
	console.log(a); // -> local 
	return a;
} 
~~~
