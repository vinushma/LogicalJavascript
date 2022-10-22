# LogicalJavascript
# Question 1
<pre class="highlight plaintext"><code>for (var i=0; i &lt; 10; i++){
    setTimeout(function(){
        console.log(i);
    }, 1000);
}
</code></pre>
<div>
 # Output <pre>10
10
10
10
10
10
10
10
10
10
</pre></div>

# Question 2

<pre class="highlight plaintext"><code>for (let i=0; i &lt; 10; i++){
    setTimeout(function(){
        console.log(i);
    }, 1000);
}
</code></pre>
<div>
 # Output <pre>
0
1
2
3
4
5
6
7
8
9
</pre></div>

# Question 3
 <pre> 
null == undefined
// true
null === undefined
// false
null > 0
// false
null >= 0
// true
1+2+"3"+2+1
// '3321'
0.1 + 0.2 === 0.3 // => ???
false
0.1 + 0.2 == 0.3 // => ???
false
</pre>

# Question 4
 <pre> 
function foo() {
  let a = b = 0;
  a++;
  return a;
}
foo();
typeof a; // => ???
typeof b; // => ???

Output:

undefined
number
 </pre> 
 
 # Question 5
 <pre>
const clothes = ['jacket', 't-shirt'];
clothes.length = 0;
clothes[0]; // => ???

Output:
undefined
</pre>
 # Question 6 Eagle eye test
  <pre>
 const length = 4;
const numbers = [];
for (var i = 0; i < length; i++);{
  numbers.push(i + 1);
}
numbers; // => ???

Output:
[5]
</pre>
 # Question 7 Eagle eye test
  <pre>
function arrayFromValue(item) {
  return
    [item];
}
arrayFromValue(10); // => ???
Output:
// => undefined
</pre>
 # Question 8 tricky closure
  <pre>
let i;
for (i = 0; i < 3; i++) {
  const log = () => {
    console.log(i);
  }
  setTimeout(log, 100);
}

Output:
3
3
3
</pre>
 # Question 9 Hoisting
  <pre>
myVar;   // => ???
myConst; // => ???
var myVar = 'value';
const myConst = 3.14;

Output:
Undefined
Reference Error
</pre>
 # Question 10  - Remove duplicates from array
  <pre>
//input = [1,2,3,2]
//output = [1,2,3]
var inp = [1,2,3,2];
var x = [];
for(let i = 0; i < inp.length; i++){
  if(x.indexOf(inp[i]) == -1){
    x.push(inp[i]);
  }
}
console.log(x);
</pre>
 # Question 11  
  <pre>
method();
function method(){
console.log(abc);
abc = 5;
console.log(abc);
}
console.log(abc);
var abc;

Output:

undefined
5
5
</pre>
 # Question 12  - Sorting Numbers - Array
  <pre>
let numbers = [85, 83, 29, 70, 4, 0, 17, 8, 55];
let x = numbers.sort((a, b) => a - b);
console.log(x);

Output:

[
   0,  4,  8, 17, 29,
  55, 70, 83, 85
]
</pre>
 <pre>
let numbers = [85, 83, 29, 70, 4, 0, 17, 8, 55];
let x = numbers.sort((a, b) => b - a);
console.log(x);

Output:

[
  85, 83, 70, 55, 29,
  17,  8,  4,  0
]

The sort method, fortunately, can sort negative, zero, and positive values in the correct order. When the sort( ) method compares two values, it sends the values to our compare function and sorts the values according to the returned value.

If the result is negative, a is sorted before b.
If the result is positive, b is sorted before a.
If the result is 0, nothing changes.

</pre>
# Question 13  - Find Max & Min number in an Array
  <pre>
let numbers = [85, 83, 29, 70, 4, 0, 17, 8, 55];
let x = Math.max.apply(null, numbers);
console.log(x);

Output:
85
</pre>
 <pre>
let numbers = [85, 83, 29, 70, 4, 1, 17, 8, 55];
let x = Math.min.apply(null, numbers);
console.log(x);

Output:

1
</pre>
# Question 14  - Sorting Objects
  <pre>
const cars = [
  {type:"Volvo", year:2016},
  {type:"Saab", year:2001},
  {type:"BMW", year:2010}
];
let x = cars.sort((a,b)=> a.year - b.year);
console.log(x);

Output:
[
  { type: 'Volvo', year: 2016 },
  { type: 'BMW', year: 2010 },
  { type: 'Saab', year: 2001 }
]
</pre>
 <pre>
const cars = [
  {type:"Volvo", year:2016},
  {type:"Saab", year:2001},
  {type:"BMW", year:2010}
];
let x = cars.sort((a,b)=> b.year - a.year);
console.log(x);

Output:
[
  { type: 'Volvo', year: 2016 },
  { type: 'BMW', year: 2010 },
  { type: 'Saab', year: 2001 }
]
</pre>
# Question 15  - Array Slice
  <pre>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
var x = fruits.slice(1,2);
console.log(x);

Output:
[ 'Orange']
</pre>
# Question 16  - Array Splice 
  <pre>
-  At position 2, add new items, and remove 1 item:
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 1, "Lemon", "Kiwi");
console.log(fruits);

Output:
[ 'Banana', 'Orange', 'Lemon', 'Kiwi', 'Mango' ]
</pre>
  <pre>
At position 2, add 2 elements:
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 0, "Lemon", "Kiwi");
console.log(fruits);

Output:
[ 'Banana', 'Orange', 'Lemon', 'Kiwi', 'Apple', 'Mango' ]
</pre>
  <pre>
At position 2, remove 2 elements:
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 2);
console.log(fruits);

Output:
[ 'Banana', 'Orange' ]
</pre>
# Question 17  - Arrays FLAT
<pre>
let x = ["Sameer","Sagar", "Rahul", ["Vinushma"] ,"Sachin"]
console.log(x.flat());

Output:

[ 'Sameer', 'Sagar', 'Rahul', 'Vinushma', 'Sachin' ]
</pre>
# Question 18  - Let - logical (Hoisting not applicable for Let & Const)
<pre>
a = 5;
console.log(a); 
let a

Output:

Error 
</pre>
# Question 19  - Comparing two objects can be done by stringify
<pre>
const k1 = { fruit: '🥝' };
const k2 = { fruit: '🥝' };

// Using JavaScript
JSON.stringify(k1) === JSON.stringify(k2); // true

</pre>

# Question 20  - Program
// my name is vinushma
// myNameIsVinusha
<pre>
let x = "my name is vinushma";
let y = x.split(' ');
let z = [y[0]];
console.log(y);
for(let i=1;i < y.length; i++){
  let otp = y[i].charAt(0).toUpperCase();
  let otp1 = otp + y[i].slice(1);
  z.push(otp1);
}
console.log(z.join(''));

Output:

[ 'my', 'name', 'is', 'vinushma' ]
myNameIsVinushma
</pre>
# Question 21  - Program to find the 2nd lagest number in the Array

<pre>
var x = [1,2,3,5,6,2,10,11,11,0];
var y = [];
for (let i=0; i < x.length; i++){
	if(y.indexOf(x[i]) == -1){
  y.push(x[i]);
  }
}
//console.log(y);
let z = y.sort((x,y) => x-y);
let otp = z[z.length - 1]
console.log(otp);

Output:

11
</pre>
# Question 22  - Remove Duplicates from the Array using Set Operator

<pre>
let x = [1,2,3,1,0,3,5,2];
let z = new Set(x);
let otp = Array.from(z);
console.log(z);
console.log(otp);

Output:

Set(5) { 1, 2, 3, 0, 5 }
[ 1, 2, 3, 0, 5 ]
</pre>
# Question 23  - Remove Duplicates from the Array using IndexOf

<pre>
let x = [1,2,3,1,0,3,5,2];
let y = [];
for (let i=0; i < x.length; i++){
  if(y.indexOf(x[i]) == -1){
    y.push(x[i]);
  }
}
console.log(y);

Output:

[ 1, 2, 3, 0, 5 ]
</pre>
# Question 23  - Remove Duplicates from the String using IndexOf

<pre>
var x = "onecompiler";
var y = x.split('');
var z = [];
for (let i=0; i < x.length; i++){
  if(z.indexOf(x[i]) == -1){
    z.push(x[i]);
  }
}
console.log(z.join(''));

Output:

onecmpilr
</pre>
