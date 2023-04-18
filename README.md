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

let x = [[1,2],[3,4],[[5,7]]];
let y = x.flat();
console.log(y.flat(Infinity));


Output:

[ 'Sameer', 'Sagar', 'Rahul', 'Vinushma', 'Sachin' ]

[ 1, 2, 3, 4, 5, 7 ]

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
# Question 24  - Remove Duplicates from the String using IndexOf

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
# Question 25  - Find Unique & dupliactes from the string

<pre>
var x = "onecompiler";
var y = x.split('');
var z = [];
var unique = [];
var duplicates = [];
for (let i=0; i < y.length; i++){
  if(z[y[i]]){
    z[y[i]] = z[y[i]] + 1;
    duplicates.push(y[i]);
  }else{
    z[y[i]] = 1;
    unique.push(y[i]);
  }
}
console.log(z);
console.log(duplicates);
console.log(unique.join(''));
console.log(duplicates.join(''));

Output:

[
  o: 2, n: 1, e: 2,
  c: 1, m: 1, p: 1,
  i: 1, l: 1, r: 1
]
[ 'o', 'e' ]
onecmpilr
oe
</pre>
# Question 26  - sum(2)(3) and sum(2, 3) what is the common solution for both

<pre>
console.log(sum(1)(2));
console.log(sum(1,2));
function sum(a,b){
  if(b == undefined)
  {
     return function (b)
     {
      return a+b;
     }
  }
  return a+b;
}

Output:

3
3
</pre>
# Question 27  - Two Strings Are Anagrams of Each Other, Input: SILENT, LISTEN
//Create a function that takes in two strings as two parameters and returns a boolean that indicates whether or not the first string is an anagram of the second string.

<pre>
let x = "SILENT";
let y = "LISTEN";
let a = x.split('').sort();
let b = y.split('').sort();
checkAnagram(a,b);
function checkAnagram(a,b){
  if(a.length == b.length){
    for(let i=0;i< a.length;i++){
      if(a[i] != b[i]){
        return console.log("Not Anagram");
      }
    }
   return console.log("String is Anagram");
  }else{
    console.log("Not Anagram");
  }
}


Output:
String is Anagram
</pre>
# Question 28  - eval- Javascript

<pre>
var x = 10;
var y = 20;
var res = eval("x+y");
console.log(res);

Output:
30
</pre>
# Question 29  - Object related Logical question

<pre>
var myObject = {
  price : 20,
  get_Price : function (){
    return this.price;
  }
}
var custObj = Object.create(myObject);
custObj.price = 19;
delete custObj.price;
console.log(custObj.get_Price());

Output:
20
</pre>
# Question 30  - How will you pass numbers to function with elements of array numbers?   
function sum(x,y,z) {
  return x + y + z;
}

const numbers = [1, 2, 3];
<pre>
let otp = sum.apply(null,numbers);
console.log(otp);

Output:
6
</pre>
# Question 31  - Extract values of first name and lastname to variables name1 and name2?   

<pre>
let employee = {
    id: 1001,
    name: {
        firstName: 'John',
        lastName: 'Doe'
    }
 };

Answer:
  let {firstName: name1,lastName: name2} = employee.name;
  
  console.log(name1);
  console.log(name2);
  
Output:
John
Doe
</pre>
# Question 32  - TypeScript - Interfaces with Optional Properties?   
https://www.logicbig.com/tutorials/misc/typescript/interface-to-describe-object-with-optional-properties.html
<pre>
export interface test {
  id:any;
  name:any;
  age:any;
  nickname:any;
}

Answer:

export interface test {
  id:any;
  name:any;
  age:any;
  nickname?:any;
}
</pre>
# Question 33  - let x='123' parse to number;  

<pre>
parseInt(x);
  
Output:
123
</pre>
# Question 34  - Remove negative numbers from array

<pre>
let numbers = [-23,-20,-17, -12, -5, 0, 1, 5, 12, 19, 20]; 
let otp = numbers.filter((x,y)=> x > -1);

console.log(otp);
  
Output:
[ 0, 1, 5, 12, 19, 20 ]
</pre>

# Question 35  - The number of positive integers and negative integers may not be equal.In such cases, add the extra integers at the end.

<pre>

For Example: 
For array {4, -9, -2, 6, -8}, the output will be {-9, 4, -2, 6, -8} 
For array {1, 2, 3, -5}, the output will be {-5, 1, 2, 3}
</pre>
<pre>
let x = [4, -9, -2, 6, -8];
console.log("Given Array = "+x);
let y = x.sort((a,b)=> a-b);
console.log("After Sorting = "+ y);

let neg = [];
let pos = [];
let newArr = [];
for(let i= 0; i< x.length; i++){
  if(x[i] >= 0){
    pos.push(x[i]);
  }else{
    neg.push(x[i]);
  }
}
console.log(neg);
console.log(pos);
for(let i=0;i< neg.length;i++){
  if(pos[i] && neg[i]){
     newArr.push(neg[i]);
     newArr.push(pos[i]);
  }else if(neg[i] || pos[i]){
    if(pos[i]){
       newArr.push(pos[i]);
    }
     if(neg[i]){
       newArr.push(neg[i]);
    }
  }
}
console.log("expected Array"+ newArr);
  
Output:
Given Array = 4,-9,-2,6,-8
After Sorting = -9,-8,-2,4,6
[ -9, -8, -2 ]
[ 4, 6 ]
expected Array-9,4,-8,6,-2
</pre>
# Question 36  - In JavaScript, how would you count the number of each item in an array, such as ["A", "B", "C", "A", "A"].
  
<pre>
let x = ["A", "B", "C", "A", "A"];
let y = [];
for(let i=0; i< x.length;i++){
  if(y[x[i]]){
    y[x[i]] = y[x[i]] + 1;
  }else{
    y[x[i]] = 1;
  }
}
console.log(y);

  
Output:

[ A: 3, B: 1, C: 1 ]
</pre>
# Question 37  - Merge Arrays in JavaScript
<pre>
1. Immutable merge of arrays

1.1 Merge using the spread operator

// merge array1 and array2
const mergeResult = [...array1, ...array2];

1.2 Merge using array.concat() method

// merge array1 and array2
const mergeResult = array1.concat(array2);

2. Mutable merge of arrays
The merge performed using the spread operator or array.concat() creates a new array. However, sometimes you don't want to create a new array, but rather merge it into some existing array.

2.1 Merge using array.push() method

const heroes = ['Batman'];
heroes.push('Superman');
heroes; // ['Batman', 'Superman']
  

</pre>
# Question 38  - In JavaScript
  
<pre>
var a = "HELLO";
var b = "llo";
console.log(a-b); //NaN

x = 10;
y = "10";
console.log(x === y); //false
</pre>
# Question 39  - How to add a property at the beginning of an object in javascript

<pre>
1. Using Object.assign:

let obj = {'b': 2, 'c': 3};
const returnedTarget = Object.assign({a: 1}, obj);

// Object {a: 1, b: 2, c: 3}

2. Using Spread Operator:
const obj = {'b': 2, 'c': 3};
const startAdded = {'a':1 , ...obj};
console.log(startAdded);

const endAdded = {...obj, 'd':4};
console.log(endAdded);

</pre>
# Question 40 - Logical - Immediately Invoked Function
<pre>
var x = { foo : 1};
var output = (function() {
  delete x.foo;
  return x.foo;
})();
console.log(output);

Output:

undefined
</pre>
# Question 41 - Remove Duplicates from the Array using filter
<pre>
const numbers = [1, 2, 3, 2, 4, 5, 5, 6];
const duplicates = numbers.filter((item, index) => index !== numbers.indexOf(item));
console.log(duplicates);

Output:

[ 2, 5 ]
</pre>
# Question 42 - Find the count of substrings in the given string
<pre>
let x = "Appleman manvinu man vinu";
let y = "vinu";

findString(x,y);

function findString(x,y){
    let z = x.split(' ');
  var count = 0;
  for(let i=0; i < z.length;i++){
    if(z[i].includes(y)){
      z[i].includes(y)
      count ++;
    }

  }
 console.log(count);
 }
 
 Output:

2
</pre>
# Question 43 - SIEMENS Logical
<pre>
 var func = function func() { 
    console.log(func === func); 
 }; 
 func();
Ans : true

Number("1") - 1 == 0; // true

(true + false) > 2 + true;   // false
</pre>
# Question 44 - Get the count of elements with difference 2 in an array of numbers in Javascript
let x = [1,2,4,6,2,5,8,6];
//otp = [no of elements with difference 2]
<pre>
let x = [1,2,3,4,6,8,10];
var count= 0;
var newArr = [];
function compareNumbers(arr){
  for(let i=0 ; i < arr.length; i++){
    for(let j=i+1; j < arr.length; j++){
      if(arr[i] - arr[j] == 2 || arr[j] - arr[i] == 2){
        newArr.push([arr[i],arr[j]])
        count++;
      }
    }
  }
};

compareNumbers(x);
console.log(count);
console.log(newArr);


Output:

5
[ [ 1, 3 ], [ 2, 4 ], [ 4, 6 ], [ 6, 8 ], [ 8, 10 ] ]
</pre>
