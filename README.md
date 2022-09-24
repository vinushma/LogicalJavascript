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
for(let i=0;i<inp.length;i++){
  if(x.indexOf(inp[i]) == -1){
    x.push(inp[i]);
  }
}
console.log(x);
</pre>
