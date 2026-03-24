# js_interview-question

Q1. What is javascript?
JavaScript (JS) is a programming language used to make websites interactive and dynamic.

Q2. What is logical operator in js?
Logical operators in JavaScript are used to combine or check conditions and return true or false.

i. AND (&&)
👉 Returns true only if both conditions are true

ii. OR (||)
👉 Returns true if at least one condition is true

iii. NOT (!)
👉 Reverses the result (true → false, false → true)

🧠 Easy way to remember:
&& → All conditions must be true
|| → Any one condition is enough
! → Reverse the result

Q3. What is ternary operator?
The ternary operator in JavaScript is a short way to write an if-else condition in one line.

🧠 Syntax:
condition ? value_if_true : value_if_false;

Q4. What is hoisting?
Hoisting in JavaScript means that variable and function declarations are moved to the top of their scope before the code runs.

🧠 Simple words:
👉 JavaScript “lifts” (hoists) declarations to the top
👉 So you can use them before declaring them

Q5. Define for while and do-while loop.

🔁 for loop
👉 A for loop is used when the number of iterations (repetitions) is known in advance.

Definition:
A loop that runs a block of code a specific number of times using initialization, condition, and update.

Example:
for (let i = 1; i <= 5; i++) {
  console.log(i);
}

🔁 while loop
👉 A while loop is used when the number of iterations is not known and depends on a condition.

Definition:
A loop that executes code as long as the condition is true.

Example:
let i = 1;
while (i <= 5) {
  console.log(i);
  i++;
}

🔁 do-while loop
👉 A do-while loop is used when you want the code to run at least once, even if the condition is false.

Definition:
A loop that executes code first, then checks the condition.

Example:
let i = 1;
do {
  console.log(i);
  i++;
} while (i <= 5);

🧠 Short summary:
-> for loop → when count is known
-> while loop → runs while condition is true
-> do-while loop → runs at least once

Q6. What is clouser?Give an example.
👉 A closure is when a function remembers and can use variables from its outer (parent) function, even after the outer function has finished running.

🧠 Simple definition:
👉 Closure = function + its outer variables (memory)

Example:

function outer() {
  let count = 0;
  function inner() {
    count++;
    console.log(count);
  }
  return inner;
}
const result = outer();
result(); // 1
result(); // 2
result(); // 3

🧠 Easy way to remember:
👉 Closure = inner function remembers outer function’s variables

⚠️ Note:
Closures are very important in JavaScript and often asked in interviews.

Q7. What is difference between let, var and cost?

🔑 var
Definition:
👉 var is used to declare variables with function scope, and it allows re-declaration and updates.

Example:
var a = 10;
var a = 20; // ✅ allowed
a = 30;     // ✅ allowed

🔑 let
Definition:
👉 let is used to declare variables with block scope, and it allows updates but not re-declaration.

Example:
let b = 10;
// let b = 20; ❌ error
b = 30;       // ✅ allowed

🔑 const
Definition:
👉 const is used to declare variables with block scope, whose value cannot be changed after initialization.

Example:
const c = 10;
// c = 20; ❌ error

🧠 Easy trick to remember:
var → old & flexible
let → changeable
const → fixed

Q8. Difference between function and arrow function?

🔑 1. Normal Function
Definition:
👉 A function is declared using the function keyword and has its own this value.

Example:
function greet() {
  console.log("Hello");
}
greet();

🔑 2. Arrow Function
Definition:
👉 An arrow function is a shorter way to write functions using => and it does not have its own this (it uses parent this).

Example:
const greet = () => {
  console.log("Hello");
};
greet();


🧠 Easy way to remember:
Normal function → full features
Arrow function → short & simple

📌 One-line:
👉 Arrow functions are shorter but behave differently (especially with this).

Q9. What is the difference between null and undefined?

🔑 undefined
Definition:
👉 undefined means a variable is declared but not assigned any value.
👉 JavaScript automatically assigns undefined.

Example:
let a;
console.log(a); // undefined

🔑 null
Definition:
👉 null means intentional empty value (you assign it yourself).
👉 Developer sets it to show “no value”.

Example:
let b = null;
console.log(b); // null

🧠 Easy trick:
undefined → not given yet
null → given but empty

📌 One-line:
👉 undefined = no value assigned, null = intentionally empty value.
