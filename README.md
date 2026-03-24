# js_interview-question

Q1. What is javascript?<br>
JavaScript (JS) is a programming language used to make websites interactive and dynamic.

Q2. What is logical operator in js?<br>
Logical operators in JavaScript are used to combine or check conditions and return true or false.

i. AND (&&)<br>
👉 Returns true only if both conditions are true

ii. OR (||)<br>
👉 Returns true if at least one condition is true

iii. NOT (!)<br>
👉 Reverses the result (true → false, false → true)

🧠 Easy way to remember:<br>
&& → All conditions must be true<br>
|| → Any one condition is enough<br>
! → Reverse the result<br>

Q3. What is ternary operator?<br>
The ternary operator in JavaScript is a short way to write an if-else condition in one line.<br>

🧠 Syntax:<br>
condition ? value_if_true : value_if_false;

Q4. What is hoisting?<br>
Hoisting in JavaScript means that variable and function declarations are moved to the top of their scope before the code runs.

🧠 Simple words:<br>
👉 JavaScript “lifts” (hoists) declarations to the top<br>
👉 So you can use them before declaring them<br>

Q5. Define for while and do-while loop.<br>

🔁 for loop<br>
👉 A for loop is used when the number of iterations (repetitions) is known in advance.<br>

Definition:<br>
A loop that runs a block of code a specific number of times using initialization, condition, and update.<br>

Example:<br>
for (let i = 1; i <= 5; i++) {<br>
  console.log(i);<br>
}<br><br>

🔁 while loop<br>
👉 A while loop is used when the number of iterations is not known and depends on a condition.

Definition:<br>
A loop that executes code as long as the condition is true.<br>

Example:<br>
let i = 1;<br>
while (i <= 5) {<br>
  console.log(i);<br>
  i++;<br>
}<br>

🔁 do-while loop<br>
👉 A do-while loop is used when you want the code to run at least once, even if the condition is false.

Definition:<br>
A loop that executes code first, then checks the condition.<br>

Example:<br>
let i = 1;<br>
do {<br>
  console.log(i);<br>
  i++;<br>
} while (i <= 5);<br><br>

🧠 Short summary:<br>
-> for loop → when count is known<br>
-> while loop → runs while condition is true<br>
-> do-while loop → runs at least once<br>

Q6. What is clouser?Give an example.<br>
👉 A closure is when a function remembers and can use variables from its outer (parent) function, even after the outer function has finished running.

🧠 Simple definition:<br>
👉 Closure = function + its outer variables (memory)<br>

Example:<br>

function outer() {<br>
  let count = 0;<br>
  function inner() {<br>
    count++;<br>
    console.log(count);<br>
  }<br>
  return inner;<br>
}<br>
const result = outer();<br>
result(); // 1<br>
result(); // 2<br>
result(); // 3<br><br>

🧠 Easy way to remember:<br>
👉 Closure = inner function remembers outer function’s variables

⚠️ Note:<br>
Closures are very important in JavaScript and often asked in interviews.

Q7. What is difference between let, var and cost?<br>

🔑 var<br>
Definition:<br>
👉 var is used to declare variables with function scope, and it allows re-declaration and updates.<br>

Example:<br>
var a = 10;<br>
var a = 20; // ✅ allowed<br>
a = 30;     // ✅ allowed<br><br>

🔑 let<br>
Definition:<br>
👉 let is used to declare variables with block scope, and it allows updates but not re-declaration.

Example:<br>
let b = 10;<br>
// let b = 20; ❌ error<br>
b = 30;       // ✅ allowed<br><br>

🔑 const<br>
Definition:<br>
👉 const is used to declare variables with block scope, whose value cannot be changed after initialization.<br>

Example:<br>
const c = 10;<br>
// c = 20; ❌ error<br><br>

🧠 Easy trick to remember:<br>
var → old & flexible<br>
let → changeable<br>
const → fixed<br>

Q8. Difference between function and arrow function?<br>

🔑 1. Normal Function<br>
Definition:<br>
👉 A function is declared using the function keyword and has its own this value.<br>

Example:<br>
function greet() {<br>
  console.log("Hello");<br>
}<br>
greet();<br><br>

🔑 2. Arrow Function<br>
Definition:<br>
👉 An arrow function is a shorter way to write functions using => and it does not have its own this (it uses parent this).<br>

Example:<br>
const greet = () => {<br>
  console.log("Hello");<br>
};<br>
greet();<br><br>


🧠 Easy way to remember:<br>
Normal function → full features<br>
Arrow function → short & simple<br>

📌 One-line:<br>
👉 Arrow functions are shorter but behave differently (especially with this).

Q9. What is the difference between null and undefined?<br>

🔑 undefined<br>
Definition:<br>
👉 undefined means a variable is declared but not assigned any value.<br>
👉 JavaScript automatically assigns undefined.<br>

Example:<br>
let a;<br>
console.log(a); // undefined<br><br>

🔑 null<br>
Definition:<br>
👉 null means intentional empty value (you assign it yourself).<br>
👉 Developer sets it to show “no value”.<br>

Example:<br>
let b = null;<br>
console.log(b); // null<br><br>

🧠 Easy trick:<br>
undefined → not given yet<br>
null → given but empty<br>

📌 One-line:<br>
👉 undefined = no value assigned, null = intentionally empty value.<br>

Q10. What is the spread operator? Difference between callback and callback hell?<br>
🔹 1. Spread Operator (...)<br>
Definition:<br>
👉 The spread operator (...) is used to expand elements of an array or object into individual elements.

🧠 Uses:<br>
-> Copy arrays/objects<br>
-> Merge data<br>
-> Pass values in functions<br>

📌 One-line:<br>
Spread operator expands values.<br>

🔹 2. Callback vs Callback Hell<br>
🔑 Callback<br>
Definition:<br>
👉 A callback is a function that is passed as an argument to another function and executed later.<br><br>

🔑 Callback Hell<br>
Definition:<br>
👉 Callback hell is a situation where multiple callbacks are nested inside each other, making code difficult to read and maintain.<br>

🧠 Easy trick:<br>
Callback → normal use<br>
Callback Hell → too many nested functions<br>

Q11. What is the use of charAt(), subString(), and includes() in a string?<br><br>

🔹 1. charAt()<br>
Definition:<br>
👉 charAt() is used to get a character at a specific index in a string.<br>

Example:<br>
let str = "Hello";<br>
console.log(str.charAt(1)); // e<br><br>

👉 Index starts from 0<br>
👉 "H e l l o" → (0 1 2 3 4)<br><br>

🔹 2. substring()<br>
Definition:<br>
👉 substring() is used to extract a part of a string between two indexes.<br>

Syntax:<br>
string.substring(start, end)<br>
Example:<br>
let str = "Hello World";<br>
console.log(str.substring(0, 5)); // Hello<br>
👉 It extracts from index 0 to 4 (end is not included)<br><br>

🔹 3. includes()<br>
Definition:<br>
👉 includes() is used to check if a string contains a specific value.<br>

Example:<br>
let str = "Hello World";<br>
console.log(str.includes("World")); // true<br>
console.log(str.includes("Hi"));    // false<br><br>

🧠 Easy trick:<br>
charAt → single character<br>
substring → part of string<br>
includes → check true/false<br>

📌 One-line:<br>
👉 These methods help you access, extract, and check data in strings<br>

Q12. What are string methods?<br>
Definition:<br>
👉 String methods are built-in functions in JavaScript that are used to perform operations on strings (text).<br><br>

🧠 Simple words:<br>
👉 String methods help you manipulate, check, and modify text.<br><br>

📌 Common String Methods:<br><br>

1. charAt()<br>
👉 Gets character at a position.<br><br>

2. substring()<br>
👉 Extracts part of a string<br><br>

3. includes()<br>
👉 Checks if text exists<br><br>

4. toUpperCase()<br>
👉 Converts to uppercase<br>
Example:<br>
"hello".toUpperCase(); // HELLO<br><br>

5. toLowerCase()<br>
👉 Converts to lowercase<br>
Example:<br>
"HELLO".toLowerCase(); // hello<br><br>

6. trim()<br>
👉 Removes extra spaces<br>
Example:<br>
"  hi  ".trim(); // "hi"<br><br>

7. replace()<br>
👉 Replaces text<br>
Example:<br>
"Hello".replace("H", "Y"); // Yello<br><br>

📌 One-line:<br>
👉 String methods are functions used to manipulate and work with strings<br><br>

Q13. What is a Palindrome and how does it work??<br>
Definition:<br>
👉 A palindrome is a word, number, or string that reads the same forward and backward.<br><br>

📌 Examples:<br>
"madam" ✅<br>
"racecar" ✅<br>
"121" ✅<br>
"hello" ❌ (not same backward)<br><br>

🧠 How does it work?<br>
👉 You reverse the string and compare it with the original:<br>
If both are same → Palindrome ✅<br>
If not → Not a palindrome ❌<br>

Q14. What is an array?<br>
Definition:<br>
👉 An array is a special variable used to store multiple values in a single variable.<br><br>

🧠 Simple words:<br>
👉 Instead of creating many variables, you store everything in one list<br><br>

📌 Key points:<br>
Stores multiple values<br>
Values can be any type (number, string, etc.)<br>
Uses square brackets [ ]<br>
Access using index<br><br>

📌 One-line:<br>
👉 An array is a collection of multiple values stored in one variable<br>

Q15. Difference between slice() and splice()?
🔹 slice()<br>
Definition:<br>
👉 slice() is used to extract a part of an array and returns a new array without changing the original<br>
Example:<br>
let arr = [1, 2, 3, 4, 5];<br>
let result = arr.slice(1, 4);<br>
console.log(result); // [2, 3, 4]<br>
console.log(arr);    // [1, 2, 3, 4, 5] (unchanged)<br><br>

🔹 splice()<br>
Definition:<br>
👉 splice() is used to add, remove, or replace elements in an array and changes the original array.<br>
Example:<br>
let arr = [1, 2, 3, 4, 5];<br>
arr.splice(1, 2); <br>
console.log(arr); // [1, 4, 5]<br><br>

🧠 Easy trick:<br>
slice → cut and copy ✂️ (no change)<br>
splice → cut and change 🔧 (modifies array)<br><br>

📌 One-line:<br>
👉 slice() copies part of array, splice() modifies the array<br>

Q16. How to remove duplicate element from an array?<br><br>

🔹 1. Using Set (Best & easiest)<br>
👉 Set automatically stores unique values only<br>
Example:<br>
let arr = [1, 2, 2, 3, 4, 4];<br>
let unique = [...new Set(arr)];<br>
console.log(unique); // [1, 2, 3, 4]<br><br>

🔹 2. Using filter()<br>
👉 Check if element appears first time<br>
Example:<br>
let arr = [1, 2, 2, 3, 4, 4];<br>
let unique = arr.filter((value, index) => {<br>
  return arr.indexOf(value) === index;<br>
});<br>
console.log(unique); // [1, 2, 3, 4]<br><br>

🔹 3. Using loop<br>
👉 Manually check and store unique values<br>
Example:<br>
let arr = [1, 2, 2, 3, 4, 4];<br>
let unique = [];<br>
for (let i = 0; i < arr.length; i++) {<br>
  if (!unique.includes(arr[i])) {<br>
    unique.push(arr[i]);<br>
  }<br>
}<br>
console.log(unique); // [1, 2, 3, 4]<br><br>

📌 Best choice:<br>
👉 Use Set method (short + fast)<br>

Q17. How to find first/last/highest number in an array?<br><br>

🔹 1. First Element<br><br>
👉 Access using index 0<br>
Example:<br>
let arr = [10, 20, 30, 40];<br>
console.log(arr[0]); // 10<br><br>

🔹 2. Last Element<br><br>
👉 Use length - 1<br>
Example:<br>
let arr = [10, 20, 30, 40];<br>
console.log(arr[arr.length - 1]); // 40<br><br>

🔹 3. Highest Number (Maximum)<br><br>
✅ Method 1: Using Math.max()<br>
Example:<br>
let arr = [10, 20, 30, 40];<br>
let max = Math.max(...arr);<br>
console.log(max); // 40<br><br>

🧠 Easy trick:<br>
First → 0 index<br>
Last → length - 1<br>
Max → Math.max(...)<br>

Q18. How to find index of a number in an array?<br><br>
🔹 1. Using indexOf() (Most common)<br>
👉 Returns the first index of the element<br>
👉 If not found → returns -1<br>
Example:<br>
let arr = [10, 20, 30, 40];<br>
console.log(arr.indexOf(30)); // 2<br>
console.log(arr.indexOf(50)); // -1<br><br>

🔹 2. Using findIndex()<br>
👉 Useful when working with conditions<br>
Example:<br>
let arr = [10, 20, 30, 40];<br>
let index = arr.findIndex(num => num > 25);<br>
console.log(index); // 2<br><br>

🔹 3. Using loop (basic way)<br>
Example:<br>
let arr = [10, 20, 30, 40];<br>
let target = 30;<br>
for (let i = 0; i < arr.length; i++) {<br>
  if (arr[i] === target) {<br>
    console.log(i); // 2<br>
  }<br>
}<br><br>

🧠 Easy trick:<br>
👉 indexOf = direct search<br>
👉 findIndex = condition search<br>

Q19. How to print array element into two array alternately?<br>
Concept:<br>
👉 Put elements at:<br>
even index (0,2,4...) → first array<br>
odd index (1,3,5...) → second array<br><br>

Example:<br>
let arr = [1, 2, 3, 4, 5, 6];<br>
let arr1 = [];<br>
let arr2 = [];<br>
for (let i = 0; i < arr.length; i++) {<br>
  if (i % 2 === 0) {<br>
    arr1.push(arr[i]); // even index<br>
  } else {<br>
    arr2.push(arr[i]); // odd index<br>
  }<br>
}<br>
console.log(arr1); // [1, 3, 5]<br>
console.log(arr2); // [2, 4, 6]<br><br>

🧠 Easy understanding:<br>
👉 Alternate means:<br>
1st → array1<br>
2nd → array2<br>
3rd → array1<br>
4th → array2<br>

Q20. What is currying in javascript?<br>
Definition:<br>
👉 Currying is a technique where a function with multiple arguments is converted into a sequence of functions, each taking one argument at a time.<br><br>

🧠 Simple words:<br>
👉 Instead of:<br>
add(a, b, c)<br>
👉 We write:<br>
add(a)(b)(c)<br><br>

📌 Example:<br>
function add(a) {<br>
  return function(b) {<br>
    return function(c) {<br>
      return a + b + c;<br>
    };<br>
  };<br>
}<br>
console.log(add(2)(3)(4)); // 9<br><br>

💡 Arrow function version:<br>
const add = a => b => c => a + b + c;<br>
console.log(add(2)(3)(4)); // 9<br><br>

📌 Why use currying?<br>
Reuse functions<br>
Create more flexible code<br>
Functional programming style<br><br>

📌 One-line:<br>
👉 Currying converts a function into multiple functions with one argument each<br><br>
