TERMINAL ```Remove-Item (Get-PSReadLineOption).HistorySavePath -ErrorAction SilentlyContinue ```
## Contents

- [A. JavaScript Programming — Q1–Q28](#a-javascript-programming)
- [B. React Components, JSX and CSS — Q29–Q42](#b-react-components-jsx-and-css)
- [C. React Props, State, Forms and Events — Q43–Q62](#c-react-props-state-forms-and-events)
- [D. React Router and Navigation — Q63–Q71](#d-react-router-and-navigation)
- [E. Node.js and Express — Q72–Q85](#e-nodejs-and-express)
- [F. MongoDB and Database Operations — Q86–Q97](#f-mongodb-and-database-operations)
- [G. React, Express and MongoDB Integration — Q98–Q108](#g-react-express-and-mongodb-integration)

## How to use this file

- **JavaScript:** save the code with the filename shown and run it with `node filename.js`.
- **React (Vite):** run `npm run dev`, then open the local URL shown in the terminal (often `http://localhost:5173`).
- **Express:** start the backend with `node server.js` unless the question specifies another command.
- **MongoDB:** ensure MongoDB is running and the database connection string matches your local setup.
- **Postman:** for POST/PUT requests, select **Body → raw → JSON**. Replace placeholder IDs with actual document IDs.
- The listed outputs are examples; database results depend on the records in your database and React output is viewed in the browser.
- Practise each program before the exam. This document formats the supplied solutions; it does not certify that every program has been executed in your environment.

---

## A. JavaScript Programming

### Q.1 — Demonstrate use of operators and control statements in JavaScript.

**Run:** `node filename.js`

**File: `operators.js`**

```javascript
let age = 20;
let marks = 70;
let day = 2;

if (age >= 18 && marks >= 40)
    console.log("Eligible and Passed");
else
    console.log("Not Eligible or Failed");

switch (day) {
    case 1:
        console.log("Monday");
        break;
    case 2:
        console.log("Tuesday");
        break;
    default:
        console.log("Invalid Day");
}
```

**Expected output / result**

```text
Eligible and Passed
Tuesday
```

### Q.2 — Write a program in JavaScript to print even numbers from 1 to 50.

**File: `even.js`**

```javascript
for (let i = 1; i <= 50; i++) {
    if (i % 2 == 0) {
        console.log(i);
    }
}
```

**Expected output / result**

```text
2
4
6
8
10
12
14
16
18
20
22
24
26
28
30
32
34
36
38
40
42
44
46
48
50
```

### Q.3 — Declare variables and write a function to calculate the sum of two numbers and display the result.

**File: `sum.js`**

```javascript
let num1 = 10;
let num2 = 20;

function sum(a, b) {
    return a + b;
}

console.log("Sum =", sum(num1, num2));
```

**Expected output / result**

```text
Sum = 30
```

### Q.4 — Write a Node.js script demonstrating basic JavaScript commands (Arithmetic Operations).

**File: `arithmetic.js`**

```javascript
let a = 10;
let b = 3;

console.log("Addition:", a + b);
console.log("Subtraction:", a - b);
console.log("Multiplication:", a * b);
console.log("Division:", a / b);
console.log("Modulus:", a % b);
console.log("Exponentiation:", a ** b);
```

**Expected output / result**

```text
Addition: 13
Subtraction: 7
Multiplication: 30
Division: 3.3333333333333335
Modulus: 1
Exponentiation: 1000
```

### Q.5 — Write a function to find the factorial of a number with JavaScript.

**File: `factorial.js`**

```javascript
function factorial(n) {
    let fact = 1;
    for (let i = 1; i <= n; i++) {
        fact = fact * i;
    }
    return fact;
}

console.log("Factorial of 5 =", factorial(5));
```

**Expected output / result**

```text
Factorial of 5 = 120
```

### Q.6 — Write a function to find the reverse of a number using JavaScript.

**File: `reverse.js`**

```javascript
function reverseNumber(n) {
    let rev = 0;
    while (n > 0) {
        let digit = n % 10;
        rev = rev * 10 + digit;
        n = Math.floor(n / 10);
    }
    return rev;
}

console.log("Reverse of 1234 =", reverseNumber(1234));
```

**Expected output / result**

```text
Reverse of 1234 = 4321
```

### Q.7 — Implement a JavaScript program to implement arrays.

**File: `arrays.js`**

```javascript
let fruits = ["Apple", "Banana", "Mango"];

console.log("Array:", fruits);
console.log("First element:", fruits[0]);
console.log("Length:", fruits.length);

fruits.push("Orange");          // add at end
console.log("After push:", fruits);

for (let i = 0; i < fruits.length; i++) {
    console.log(i, fruits[i]);
}
```

**Expected output / result**

```text
Array: [ 'Apple', 'Banana', 'Mango' ]
First element: Apple
Length: 3
After push: [ 'Apple', 'Banana', 'Mango', 'Orange' ]
0 Apple
1 Banana
2 Mango
3 Orange
```

### Q.8 — Demonstrate use of arrow functions.

**File: `arrow.js`**

```javascript
const calculateTotal = (price, quantity) => price * quantity;
const greet = name => console.log("Hello, " + name);

console.log("Total =", calculateTotal(750, 3));
greet("Ritik");
```

**Expected output / result**

```text
Total = 2250
Hello, Ritik
```

### Q.9 — Write a JavaScript program to find the largest of three numbers.

**File: `largest.js`**

```javascript
let a = 25;
let b = 80;
let c = 45;

if (a >= b && a >= c) {
    console.log("Largest =", a);
} else if (b >= a && b >= c) {
    console.log("Largest =", b);
} else {
    console.log("Largest =", c);
}
```

**Expected output / result**

```text
Largest = 80
```

### Q.10 — Write a JavaScript program to display the factorial of a given number using a loop and template literals.

**File: `factorial_loop.js`**

```javascript
let num = 5;
let fact = 1;

for (let i = 1; i <= num; i++) {
    fact = fact * i;
}

console.log(`Factorial of ${num} is ${fact}`);
```

**Expected output / result**

```text
Factorial of 5 is 120
```

### Q.11 — Write a JavaScript program to demonstrate the use of arrays and objects.

**File: `array_object.js`**

```javascript
let fruits = ["Apple", "Mango", "Banana"];     // Array

let student = {                                // Object
    name: "Aarav",
    age: 20,
    course: "TYIT"
};

console.log("Array:", fruits);
console.log("Accessing element:", fruits[0]);
console.log("Object:", student);
console.log("Accessing property:", student.name);
console.log("Accessing property:", student.age);
```

**Expected output / result**

```text
Array: [ 'Apple', 'Mango', 'Banana' ]
Accessing element: Apple
Object: { name: 'Aarav', age: 20, course: 'TYIT' }
Accessing property: Aarav
Accessing property: 20
```

### Q.12 — Write a JavaScript program to print the multiplication table of a given number using a loop and template literals.

**File: `table.js`**

```javascript
let num = 5;

for (let i = 1; i <= 10; i++) {
    console.log(`${num} x ${i} = ${num * i}`);
}
```

**Expected output / result**

```text
5 x 1 = 5
5 x 2 = 10
5 x 3 = 15
5 x 4 = 20
5 x 5 = 25
5 x 6 = 30
5 x 7 = 35
5 x 8 = 40
5 x 9 = 45
5 x 10 = 50
```

### Q.13 — Write a JavaScript program to add two numbers using an arrow function.

**File: `add_arrow.js`**

```javascript
const add = (a, b) => a + b;

console.log("Sum =", add(10, 20));
```

**Expected output / result**

```text
Sum = 30
```

### Q.14 — Write a JavaScript program to perform map, filter, reduce using Array Methods.

**File: `array_methods.js`**

```javascript
let numbers = [1, 2, 3, 4];
let marks = [50, 65, 90, 40, 80];

// map - square of each number
let squares = numbers.map((num) => num * num);
console.log("Map:", squares);

// filter - marks greater than 60
let result = marks.filter((mark) => mark > 60);
console.log("Filter:", result);

// reduce - sum of numbers
let sum = numbers.reduce((total, num) => total + num, 0);
console.log("Reduce:", sum);
```

**Expected output / result**

```text
Map: [ 1, 4, 9, 16 ]
Filter: [ 65, 90, 80 ]
Reduce: 10
```

### Q.15 — Write a JavaScript program to create a student object and display its properties.

**File: `student_object.js`**

```javascript
let student = {
    name: "Aarav",
    rollno: 101,
    course: "TYIT",
    marks: 75
};

console.log("Name:", student.name);
console.log("Roll No:", student.rollno);
console.log("Course:", student.course);
console.log("Marks:", student.marks);
```

**Expected output / result**

```text
Name: Aarav
Roll No: 101
Course: TYIT
Marks: 75
```

### Q.16 — Write a JavaScript program to store student details in an array of objects and display them using a function.

**File: `student_array.js`**

```javascript
let students = [
    { name: "Aarav", rollno: 1, marks: 75 },
    { name: "Riya", rollno: 2, marks: 82 },
    { name: "Karan", rollno: 3, marks: 68 }
];

function displayStudents() {
    for (let i = 0; i < students.length; i++) {
        console.log(`Roll No: ${students[i].rollno}, Name: ${students[i].name}, Marks: ${students[i].marks}`);
    }
}

displayStudents();
```

**Expected output / result**

```text
Roll No: 1, Name: Aarav, Marks: 75
Roll No: 2, Name: Riya, Marks: 82
Roll No: 3, Name: Karan, Marks: 68
```

### Q.17 — Write a JavaScript program to store student marks in an array of objects and calculate the total marks using a function.

**File: `total_marks.js`**

```javascript
let students = [
    { name: "Aarav", marks: 75 },
    { name: "Riya", marks: 82 },
    { name: "Karan", marks: 68 }
];

function totalMarks() {
    let total = 0;
    for (let i = 0; i < students.length; i++) {
        total = total + students[i].marks;
    }
    return total;
}

console.log("Total Marks =", totalMarks());
```

**Expected output / result**

```text
Total Marks = 225
```

### Q.18 — Write a JavaScript program to check whether a number is even or odd using an arrow function.

**File: `evenodd_arrow.js`**

```javascript
const checkEvenOdd = (n) => (n % 2 == 0 ? "Even" : "Odd");

console.log("10 is", checkEvenOdd(10));
console.log("7 is", checkEvenOdd(7));
```

**Expected output / result**

```text
10 is Even
7 is Odd
```

### Q.19 — Accept the marks of a student in a variable. Using arithmetic, comparison and logical operators with if...else if...else, display the percentage, the grade and whether the student has passed with distinction.

Total marks obtained are stored in a variable (out of 500 marks).

**File: `grade.js`**

```javascript
let marks = 410;
let total = 500;

let percentage = (marks / total) * 100;
console.log("Percentage:", percentage + "%");

if (percentage >= 75) {
    console.log("Grade: A");
} else if (percentage >= 60) {
    console.log("Grade: B");
} else if (percentage >= 40) {
    console.log("Grade: C");
} else {
    console.log("Grade: Fail");
}

if (percentage >= 75 && marks <= total) {
    console.log("Passed with Distinction");
} else if (percentage >= 40) {
    console.log("Passed");
} else {
    console.log("Failed");
}
```

**Expected output / result**

```text
Percentage: 82%
Grade: A
Passed with Distinction
```

### Q.20 — Write a Node.js program that prints the multiplication table of a given number using a for loop and template literals.

**File: `mult_table.js`**

```javascript
let n = 7;

for (let i = 1; i <= 10; i++) {
    console.log(`${n} * ${i} = ${n * i}`);
}
```

**Expected output / result**

```text
7 * 1 = 7
7 * 2 = 14
7 * 3 = 21
7 * 4 = 28
7 * 5 = 35
7 * 6 = 42
7 * 7 = 49
7 * 8 = 56
7 * 9 = 63
7 * 10 = 70
```

### Q.21 — Create a function with parameters to calculate simple interest (principal, rate, time). Call the function with three different sets of values and display the results.

**File: `interest.js`**

```javascript
function simpleInterest(principal, rate, time) {
    return (principal * rate * time) / 100;
}

console.log("Interest 1 =", simpleInterest(1000, 5, 2));
console.log("Interest 2 =", simpleInterest(5000, 8, 3));
console.log("Interest 3 =", simpleInterest(10000, 10, 1));
```

**Expected output / result**

```text
Interest 1 = 100
Interest 2 = 1200
Interest 3 = 1000
```

### Q.22 — Create an array of five product names. Perform push, pop, shift and unshift operations on it and display the array after each operation. Also create an object for a book and display its properties.

**File: `array_ops.js`**

```javascript
let products = ["Pen", "Book", "Bag", "Bottle", "Pencil"];
console.log("Original:", products);

products.push("Eraser");         // add at end
console.log("After push:", products);

products.pop();                  // remove from end
console.log("After pop:", products);

products.shift();                // remove from start
console.log("After shift:", products);

products.unshift("Marker");      // add at start
console.log("After unshift:", products);

let book = {
    title: "Learn JavaScript",
    author: "John",
    price: 350
};

console.log("Title:", book.title);
console.log("Author:", book.author);
console.log("Price:", book.price);
```

**Expected output / result**

```text
Original: [ 'Pen', 'Book', 'Bag', 'Bottle', 'Pencil' ]
After push: [ 'Pen', 'Book', 'Bag', 'Bottle', 'Pencil', 'Eraser' ]
After pop: [ 'Pen', 'Book', 'Bag', 'Bottle', 'Pencil' ]
After shift: [ 'Book', 'Bag', 'Bottle', 'Pencil' ]
After unshift: [ 'Marker', 'Book', 'Bag', 'Bottle', 'Pencil' ]
Title: Learn JavaScript
Author: John
Price: 350
```

### Q.23 — Write functions to find the square, the cube and to check even/odd for a number. Convert all of them into arrow functions and display the output.

**File: `square_cube.js`**

```javascript
// Normal functions
function square(n) { return n * n; }
function cube(n) { return n * n * n; }
function isEven(n) { return n % 2 == 0 ? "Even" : "Odd"; }

// Arrow functions
const square2 = (n) => n * n;
const cube2 = (n) => n * n * n;
const isEven2 = (n) => (n % 2 == 0 ? "Even" : "Odd");

console.log("Square:", square2(4));
console.log("Cube:", cube2(3));
console.log("Even/Odd:", isEven2(7));
```

**Expected output / result**

```text
Square: 16
Cube: 27
Even/Odd: Odd
```

### Q.24 — Create an array of employee salaries. Using map(), increase each salary by 10%; using filter(), display salaries above 30000; using reduce(), display the total salary.

**File: `salary.js`**

```javascript
let salaries = [20000, 35000, 28000, 50000];

let increased = salaries.map((s) => s + s * 0.10);
console.log("After 10% increase:", increased);

let above = salaries.filter((s) => s > 30000);
console.log("Salaries above 30000:", above);

let total = salaries.reduce((sum, s) => sum + s, 0);
console.log("Total salary:", total);
```

**Expected output / result**

```text
After 10% increase: [ 22000, 38500, 30800, 55000 ]
Salaries above 30000: [ 35000, 50000 ]
Total salary: 133000
```

### Q.25 — Use a switch statement to display the day name for a day number (1 to 7). Use the conditional (ternary) operator to check whether a given year is a leap year. Store a list of courses in the state and display it using the map() function. Display each course in a list item with a unique key.

Part 1 and 2 (JavaScript - run with node)

**File: `day_leap.js`**

```javascript
let day = 4;

switch (day) {
    case 1: console.log("Monday"); break;
    case 2: console.log("Tuesday"); break;
    case 3: console.log("Wednesday"); break;
    case 4: console.log("Thursday"); break;
    case 5: console.log("Friday"); break;
    case 6: console.log("Saturday"); break;
    case 7: console.log("Sunday"); break;
    default: console.log("Invalid Day");
}

let year = 2024;
let result = (year % 4 == 0 && year % 100 != 0) || year % 400 == 0
    ? "Leap Year"
    : "Not a Leap Year";
console.log(year, "is", result);
```

**Expected output / result**

```text
Thursday
2024 is Leap Year

Part 3 (React - courses stored in state and displayed using map)
```

**File: `App.jsx`**

```jsx
import { useState } from "react";

function App() {
  const [courses, setCourses] = useState(["BSc IT", "BSc CS", "BCom", "BMS", "BAF"]);

  return (
    <div>
      <h1>Course List</h1>
      <ul>
        {courses.map((course, index) => (
          <li key={index}>{course}</li>
        ))}
      </ul>
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Browser shows the heading 'Course List' and each course as a bullet list item.
```

### Q.26 — Write a function with a default parameter and a return value to calculate an electricity bill from the units consumed (slab-wise). Display the bill for three consumers.

Slab rates used: first 100 units Rs.3 per unit, next 100 units Rs.5 per unit, above 200 units Rs.7 per unit.

**File: `electricity.js`**

```javascript
function calculateBill(units = 0) {
    let bill = 0;

    if (units <= 100) {
        bill = units * 3;
    } else if (units <= 200) {
        bill = 100 * 3 + (units - 100) * 5;
    } else {
        bill = 100 * 3 + 100 * 5 + (units - 200) * 7;
    }

    return bill;
}

console.log("Consumer 1 (80 units): Rs.", calculateBill(80));
console.log("Consumer 2 (150 units): Rs.", calculateBill(150));
console.log("Consumer 3 (250 units): Rs.", calculateBill(250));
console.log("No units given: Rs.", calculateBill());
```

**Expected output / result**

```text
Consumer 1 (80 units): Rs. 240
Consumer 2 (150 units): Rs. 550
Consumer 3 (250 units): Rs. 1150
No units given: Rs. 0
```

### Q.27 — Write a JavaScript program to demonstrate arithmetic, comparison, and logical operators along with control statements.

**File: `all_operators.js`**

```javascript
let a = 15;
let b = 4;

// Arithmetic operators
console.log("Addition:", a + b);
console.log("Subtraction:", a - b);
console.log("Multiplication:", a * b);
console.log("Division:", a / b);
console.log("Modulus:", a % b);

// Comparison operators
console.log("a > b:", a > b);
console.log("a == b:", a == b);
console.log("a != b:", a != b);

// Logical operators
console.log("AND:", a > 10 && b > 10);
console.log("OR:", a > 10 || b > 10);
console.log("NOT:", !(a > b));

// Control statements
if (a > b) {
    console.log("a is greater than b");
} else {
    console.log("b is greater than a");
}

for (let i = 1; i <= 3; i++) {
    console.log("Loop:", i);
}
```

**Expected output / result**

```text
Addition: 19
Subtraction: 11
Multiplication: 60
Division: 3.75
Modulus: 3
a > b: true
a == b: false
a != b: true
AND: false
OR: true
NOT: false
a is greater than b
Loop: 1
Loop: 2
Loop: 3
```

### Q.28 — Implement a small library program: keep an array of book objects (title, author, available) and write functions to add a book, search a book by title and list all available books.

**File: `library.js`**

```javascript
let books = [
    { title: "JavaScript Basics", author: "John", available: true },
    { title: "React Guide", author: "Mary", available: false }
];

function addBook(title, author, available) {
    books.push({ title: title, author: author, available: available });
    console.log("Book added:", title);
}

function searchBook(title) {
    for (let i = 0; i < books.length; i++) {
        if (books[i].title == title) {
            console.log("Found:", books[i]);
            return;
        }
    }
    console.log("Book not found");
}

function listAvailable() {
    console.log("Available books:");
    for (let i = 0; i < books.length; i++) {
        if (books[i].available) {
            console.log("-", books[i].title);
        }
    }
}

addBook("Node.js Guide", "Sam", true);
searchBook("React Guide");
searchBook("Python");
listAvailable();
```

**Expected output / result**

```text
Book added: Node.js Guide
Found: { title: 'React Guide', author: 'Mary', available: false }
Book not found
Available books:
- JavaScript Basics
- Node.js Guide
```

## B. React Components, JSX and CSS

### Q.29 — Apply basic CSS styling to a React component.

> Setup (once): open VS Code terminal and run the commands below. Replace the code of src/App.jsx with the code given in each question. Open http://localhost:5173 in the browser.

**Terminal / setup commands**

```bash
npm create vite@latest myapp
(select React -> JavaScript)
cd myapp
npm install
npm run dev
```

**File: `src/App.jsx`**

```jsx
import "./App.css";

function App() {
  return (
    <div className="container">
      <h1 className="heading">Welcome to React</h1>
      <button className="button">Click Me</button>
    </div>
  );
}

export default App;
```

**File: `src/App.css`**

```css
.container {
  text-align: center;
  background-color: lightblue;
  padding: 20px;
  border-radius: 10px;
}

.heading {
  color: darkblue;
}

.button {
  background-color: blue;
  color: white;
  padding: 10px 15px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
```

**Expected output / result**

```text
Output: a light blue box with a dark blue heading 'Welcome to React' and a blue 'Click Me' button.
```

### Q.30 — Create a simple functional component and render it in App.js.

**File: `src/Demo.jsx`**

```jsx
function Demo() {
  return <h2>I am demo Component</h2>;
}

export default Demo;
```

**File: `src/App.jsx`**

```jsx
import Demo from "./Demo";

function App() {
  return (
    <div>
      <h1>Welcome</h1>
      <Demo />
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: 'Welcome' heading followed by 'I am demo Component'.
```

### Q.31 — Create a React component that displays the current date and time dynamically using JavaScript.

**File: `src/DateTime.jsx`**

```jsx
function DateTime() {
  let today = new Date();

  return (
    <div>
      <h2>Date : {today.toLocaleDateString()}</h2>
      <h2>Time : {today.toLocaleTimeString()}</h2>
    </div>
  );
}

export default DateTime;
```

**File: `src/App.jsx`**

```jsx
import DateTime from "./DateTime";

function App() {
  return (
    <div>
      <h1>Welcome</h1>
      <DateTime />
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: the current system date and time is displayed on the page.
```

### Q.32 — Create multiple components and render them on a single page.

**File: `src/Student.jsx`**

```jsx
function Student() {
  return (
    <div>
      <h2>Student Component</h2>
      <p>Name: Neha</p>
    </div>
  );
}

export default Student;
```

**File: `src/Teacher.jsx`**

```jsx
function Teacher() {
  return (
    <div>
      <h2>Teacher Component</h2>
      <p>Name: Rahul Sir</p>
    </div>
  );
}

export default Teacher;
```

**File: `src/App.jsx`**

```jsx
import Student from "./Student";
import Teacher from "./Teacher";

function App() {
  return (
    <div>
      <h1>Multiple Components</h1>
      <Student />
      <Teacher />
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: both the Student and Teacher components are shown on one page.
```

### Q.33 — Write a React program to create a function that calculates the sum of two numbers and displays the result on the web page.

**File: `src/App.jsx`**

```jsx
function App() {
  let num1 = 10;
  let num2 = 20;

  function sum(a, b) {
    return a + b;
  }

  return (
    <div>
      <h1>Sum = {sum(num1, num2)}</h1>
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: Sum = 30
```

### Q.34 — Write a React program to create a component and apply CSS styling to it using an external CSS file.

**File: `src/Card.jsx`**

```jsx
import "./Card.css";

function Card() {
  return (
    <div className="card">
      <h2>React Card</h2>
      <p>This component is styled using an external CSS file.</p>
    </div>
  );
}

export default Card;
```

**File: `src/Card.css`**

```css
.card {
  width: 300px;
  margin: 30px auto;
  padding: 20px;
  border: 2px solid green;
  border-radius: 10px;
  background-color: #e8f5e9;
  text-align: center;
}
```

**File: `src/App.jsx`**

```jsx
import Card from "./Card";

function App() {
  return <Card />;
}

export default App;
```

**Expected output / result**

```text
Output: a green bordered card with a heading and a paragraph.
```

### Q.35 — Write a React program to create and render multiple functional components within a single React application.

**File: `src/Header.jsx`**

```jsx
function Header() {
  return <h1>My Website</h1>;
}

export default Header;
```

**File: `src/Content.jsx`**

```jsx
function Content() {
  return <p>This is the main content of the page.</p>;
}

export default Content;
```

**File: `src/Footer.jsx`**

```jsx
function Footer() {
  return <h4>Footer - All rights reserved</h4>;
}

export default Footer;
```

**File: `src/App.jsx`**

```jsx
import Header from "./Header";
import Content from "./Content";
import Footer from "./Footer";

function App() {
  return (
    <div>
      <Header />
      <Content />
      <Footer />
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: Header, Content and Footer components displayed on a single page.
```

### Q.36 — Write a React program to create a functional component that displays a heading and a paragraph and render it in App.jsx.

**File: `src/Info.jsx`**

```jsx
function Info() {
  return (
    <div>
      <h2>About React</h2>
      <p>React is a JavaScript library used to build user interfaces.</p>
    </div>
  );
}

export default Info;
```

**File: `src/App.jsx`**

```jsx
import Info from "./Info";

function App() {
  return <Info />;
}

export default App;
```

**Expected output / result**

```text
Output: heading 'About React' with a paragraph below it.
```

### Q.37 — Write a React program to create a component that dynamically displays the current date and time and updates it every second.

**File: `src/Clock.jsx`**

```jsx
import { useState, useEffect } from "react";

function Clock() {
  const [now, setNow] = useState(new Date());

  useEffect(() => {
    const timer = setInterval(() => {
      setNow(new Date());
    }, 1000);

    return () => clearInterval(timer);
  }, []);

  return (
    <div>
      <h2>Date : {now.toLocaleDateString()}</h2>
      <h2>Time : {now.toLocaleTimeString()}</h2>
    </div>
  );
}

export default Clock;
```

**File: `src/App.jsx`**

```jsx
import Clock from "./Clock";

function App() {
  return (
    <div>
      <h1>Live Clock</h1>
      <Clock />
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: the date and the time are displayed and the time changes every second.
```

### Q.38 — Write a React program to create a functional component that displays a welcome message and render it in App.jsx.

**File: `src/Welcome.jsx`**

```jsx
function Welcome() {
  return <h1>Welcome to MERN Stack Development</h1>;
}

export default Welcome;
```

**File: `src/App.jsx`**

```jsx
import Welcome from "./Welcome";

function App() {
  return <Welcome />;
}

export default App;
```

**Expected output / result**

```text
Output: Welcome to MERN Stack Development
```

### Q.39 — Write a React program to create a functional component that dynamically displays the current date and time using JavaScript and updates it every second.

The same Clock component is used (setInterval updates the state every 1000 ms = 1 second).

**File: `src/Clock.jsx`**

```jsx
import { useState, useEffect } from "react";

function Clock() {
  const [now, setNow] = useState(new Date());

  useEffect(() => {
    const timer = setInterval(() => {
      setNow(new Date());
    }, 1000);

    return () => clearInterval(timer);
  }, []);

  return (
    <div>
      <h2>Date : {now.toLocaleDateString()}</h2>
      <h2>Time : {now.toLocaleTimeString()}</h2>
    </div>
  );
}

export default Clock;
```

**File: `src/App.jsx`**

```jsx
import Clock from "./Clock";

function App() {
  return (
    <div>
      <h1>Live Clock</h1>
      <Clock />
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: the date and the time are displayed and the time changes every second.
```

### Q.40 — Write a React program to create multiple functional components and render them together on a single web page using App.jsx.

**File: `src/Student.jsx`**

```jsx
function Student() {
  return (
    <div>
      <h2>Student Component</h2>
      <p>Name: Neha</p>
    </div>
  );
}

export default Student;
```

**File: `src/Teacher.jsx`**

```jsx
function Teacher() {
  return (
    <div>
      <h2>Teacher Component</h2>
      <p>Name: Rahul Sir</p>
    </div>
  );
}

export default Teacher;
```

**File: `src/App.jsx`**

```jsx
import Student from "./Student";
import Teacher from "./Teacher";

function App() {
  return (
    <div>
      <h1>Multiple Components</h1>
      <Student />
      <Teacher />
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: both the Student and Teacher components are shown on one page.
```

### Q.41 — Create two simple functional components, Welcome and Footer, and render them in App.js. Display your name and college name in them.

**File: `src/Welcome.jsx`**

```jsx
function Welcome() {
  return <h2>Welcome, Ritik</h2>;
}

export default Welcome;
```

**File: `src/Footer.jsx`**

```jsx
function Footer() {
  return <h3>Thakur Ramnarayan College of Arts and Commerce</h3>;
}

export default Footer;
```

**File: `src/App.jsx`**

```jsx
import Welcome from "./Welcome";
import Footer from "./Footer";

function App() {
  return (
    <div>
      <Welcome />
      <Footer />
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: 'Welcome, Ritik' and the college name below it.
```

### Q.42 — Create a React application using Vite/CRA and display "Welcome to MERN Stack Development". Create a functional component Header and render it in App.js.

**Terminal / setup commands**

```bash
npm create vite@latest myapp
Select a framework: React
Select a variant: JavaScript
cd myapp
npm install
npm run dev
```

**File: `src/Header.jsx`**

```jsx
function Header() {
  return <h2>This is the Header Component</h2>;
}

export default Header;
```

**File: `src/App.jsx`**

```jsx
import Header from "./Header";

function App() {
  return (
    <div>
      <h1>Welcome to MERN Stack Development</h1>
      <Header />
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: 'Welcome to MERN Stack Development' followed by the Header component text.
```

## C. React Props, State, Forms and Events

### Q.43 — React components - Pass data between components using props.

src/Student.jsx (Child)

function Student(props) {

return (

<div>

<h2>Student Details</h2>

<p>Name: {props.name}</p>

<p>Course: {props.course}</p>

</div>

);

}

export default Student;

src/App.jsx (Parent)

import Student from "./Student";

function App() {

return (

<div>

<h1>Props Example</h1>

<Student name="Gauri" course="MERN Stack" />

<Student name="Pragati" course="MERN Stack" />

</div>

);

}

export default App;

**Expected output / result**

```text
Output: two Student blocks, one for Gauri and one for Pragati.
```

### Q.44 — React components - Use the useState hook to manage and update data.

**File: `src/App.jsx`**

```jsx
import { useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  function increase() {
    setCount(count + 1);
  }

  return (
    <div>
      <h1>{count}</h1>
      <button onClick={increase}>Increase</button>
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: the number increases by 1 every time the button is clicked.
```

### Q.45 — Create a form component to accept user input and display it dynamically.

**File: `src/Form.jsx`**

```jsx
import { useState } from "react";

function Form() {
  const [name, setName] = useState("");
  const [displayName, setDisplayName] = useState("");

  function handleSubmit() {
    setDisplayName(name);
  }

  return (
    <div>
      <h2>User Form</h2>
      <input
        type="text"
        placeholder="Enter your name"
        onChange={(e) => setName(e.target.value)}
      />
      <button onClick={handleSubmit}>Submit</button>
      <p>Hello, {displayName}</p>
    </div>
  );
}

export default Form;
```

**File: `src/App.jsx`**

```jsx
import Form from "./Form";

function App() {
  return <Form />;
}

export default App;
```

**Expected output / result**

```text
Output: type a name in the box and click Submit, 'Hello, <name>' is displayed.
```

### Q.46 — Display a list of items stored in the state using map().

**File: `src/App.jsx`**

```jsx
import { useState } from "react";

function App() {
  const [fruits, setFruits] = useState(["Apple", "Banana", "Mango", "Orange", "Grapes"]);

  return (
    <div>
      <h1>List using map()</h1>
      <ul>
        {fruits.map((fruit, index) => (
          <li key={index}>{fruit}</li>
        ))}
      </ul>
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: the five fruit names are shown as a bullet list.
```

### Q.47 — Build a counter interface using React.

**File: `src/App.jsx`**

```jsx
import { useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  return (
    <div style={{ textAlign: "center", marginTop: "50px" }}>
      <h1>Counter App</h1>
      <h2>{count}</h2>
      <button onClick={() => setCount(count + 1)}>Increment</button>
      <button onClick={() => setCount(count - 1)}>Decrement</button>
      <button onClick={() => setCount(0)}>Reset</button>
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: a counter with Increment, Decrement and Reset buttons.
```

### Q.48 — Build a To-do list interface using React.

**File: `src/App.jsx`**

```jsx
import { useState } from "react";

function App() {
  const [task, setTask] = useState("");
  const [tasks, setTasks] = useState([]);

  function addTask() {
    if (task == "") return;
    setTasks([...tasks, task]);
    setTask("");
  }

  function deleteTask(index) {
    setTasks(tasks.filter((t, i) => i != index));
  }

  return (
    <div>
      <h1>To-Do List</h1>
      <input
        type="text"
        placeholder="Enter task"
        value={task}
        onChange={(e) => setTask(e.target.value)}
      />
      <button onClick={addTask}>Add</button>

      <ul>
        {tasks.map((t, index) => (
          <li key={index}>
            {t}
            <button onClick={() => deleteTask(index)}>Delete</button>
          </li>
        ))}
      </ul>
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: type a task and click Add to list it; the Delete button removes it.
```

### Q.49 — Create a React application to display a list of names using the map() method.

**File: `src/App.jsx`**

```jsx
function App() {
  const names = ["Aarav", "Riya", "Karan", "Neha", "Rahul"];

  return (
    <div>
      <h1>Names List</h1>
      <ul>
        {names.map((name, index) => (
          <li key={index}>{name}</li>
        ))}
      </ul>
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: the five names are displayed as a list.
```

### Q.50 — Create a React component to calculate the square and cube of a given number.

**File: `src/App.jsx`**

```jsx
import { useState } from "react";

function App() {
  const [num, setNum] = useState(0);

  return (
    <div>
      <h1>Square and Cube</h1>
      <input
        type="number"
        value={num}
        onChange={(e) => setNum(Number(e.target.value))}
      />
      <p>Square = {num * num}</p>
      <p>Cube = {num * num * num}</p>
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: for input 4 it shows Square = 16 and Cube = 64.
```

### Q.51 — Write a React program to display student details dynamically using JSX.

**File: `src/App.jsx`**

```jsx
function App() {
  const name = "Aarav";
  const rollno = 101;
  const course = "TYIT";
  const marks = 75;

  return (
    <div>
      <h1>Student Details</h1>
      <p>Name: {name}</p>
      <p>Roll No: {rollno}</p>
      <p>Course: {course}</p>
      <p>Marks: {marks}</p>
      <p>Result: {marks >= 35 ? "Pass" : "Fail"}</p>
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: the student details are displayed with the result Pass.
```

### Q.52 — Create a Student component and pass student name, roll number, and course using props.

**File: `src/Student.jsx`**

```jsx
function Student(props) {
  return (
    <div>
      <h2>Student Details</h2>
      <p>Name: {props.name}</p>
      <p>Roll No: {props.rollno}</p>
      <p>Course: {props.course}</p>
    </div>
  );
}

export default Student;
```

**File: `src/App.jsx`**

```jsx
import Student from "./Student";

function App() {
  return <Student name="Aarav" rollno={101} course="TYIT" />;
}

export default App;
```

**Expected output / result**

```text
Output: Name: Aarav, Roll No: 101, Course: TYIT
```

### Q.53 — Create a React component to display and update a user's name using the useState() hook.

**File: `src/App.jsx`**

```jsx
import { useState } from "react";

function App() {
  const [name, setName] = useState("Ritik");

  return (
    <div>
      <h1>Hello, {name}</h1>
      <input
        type="text"
        value={name}
        onChange={(e) => setName(e.target.value)}
      />
      <button onClick={() => setName("Guest")}>Reset Name</button>
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: the heading changes as the name is typed in the input box.
```

### Q.54 — Create a Product component that accepts product name and price through props and displays the details.

**File: `src/Product.jsx`**

```jsx
function Product(props) {
  return (
    <div>
      <h3>Product: {props.name}</h3>
      <p>Price: Rs. {props.price}</p>
    </div>
  );
}

export default Product;
```

**File: `src/App.jsx`**

```jsx
import Product from "./Product";

function App() {
  return (
    <div>
      <h1>Products</h1>
      <Product name="Laptop" price={55000} />
      <Product name="Mobile" price={20000} />
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: details of the Laptop and Mobile products.
```

### Q.55 — Create a React application to display a list of student names stored in state using the map() method.

**File: `src/App.jsx`**

```jsx
import { useState } from "react";

function App() {
  const [students, setStudents] = useState(["Aarav", "Riya", "Karan", "Neha"]);

  return (
    <div>
      <h1>Student Names</h1>
      <ul>
        {students.map((name, index) => (
          <li key={index}>{name}</li>
        ))}
      </ul>
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: the student names are displayed as a list.
```

### Q.56 — Create a React application to implement a counter with increment and decrement by clicking the buttons.

**File: `src/App.jsx`**

```jsx
import { useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  return (
    <div style={{ textAlign: "center", marginTop: "50px" }}>
      <h1>Counter</h1>
      <h2>{count}</h2>
      <button onClick={() => setCount(count + 1)}>Increment</button>
      <button onClick={() => setCount(count - 1)}>Decrement</button>
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: the count goes up or down by 1 on every button click.
```

### Q.57 — Create a React Form Component to Accept User Details and Display the Entered Information Dynamically Upon Form Submission.

**File: `src/App.jsx`**

```jsx
import { useState } from "react";

function App() {
  const [name, setName] = useState("");
  const [email, setEmail] = useState("");
  const [city, setCity] = useState("");
  const [submitted, setSubmitted] = useState(null);

  function handleSubmit(e) {
    e.preventDefault();
    setSubmitted({ name: name, email: email, city: city });
  }

  return (
    <div>
      <h1>User Details Form</h1>
      <form onSubmit={handleSubmit}>
        <input type="text" placeholder="Name" value={name}
          onChange={(e) => setName(e.target.value)} />
        <input type="email" placeholder="Email" value={email}
          onChange={(e) => setEmail(e.target.value)} />
        <input type="text" placeholder="City" value={city}
          onChange={(e) => setCity(e.target.value)} />
        <button type="submit">Submit</button>
      </form>

      {submitted && (
        <div>
          <h2>Entered Information</h2>
          <p>Name: {submitted.name}</p>
          <p>Email: {submitted.email}</p>
          <p>City: {submitted.city}</p>
        </div>
      )}
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: after clicking Submit, the entered name, email and city are displayed below the form.
```

### Q.58 — Create a React Component to Store a List of Items in State and Display Them Dynamically Using the map() Method.

**File: `src/App.jsx`**

```jsx
import { useState } from "react";

function App() {
  const [items, setItems] = useState(["Pen", "Book"]);
  const [item, setItem] = useState("");

  function addItem() {
    if (item == "") return;
    setItems([...items, item]);
    setItem("");
  }

  return (
    <div>
      <h1>Item List</h1>
      <input type="text" value={item} onChange={(e) => setItem(e.target.value)} />
      <button onClick={addItem}>Add Item</button>
      <ul>
        {items.map((i, index) => (
          <li key={index}>{i}</li>
        ))}
      </ul>
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: new items are added to the list dynamically when Add Item is clicked.
```

### Q.59 — Create an Interactive Counter Component in React Using the useState() Hook to Increment and Decrement the Counter Value.

**File: `src/App.jsx`**

```jsx
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <h2>Count: {count}</h2>
      <button onClick={() => setCount(count + 1)}>+</button>
      <button onClick={() => setCount(count - 1)}>-</button>
    </div>
  );
}

function App() {
  return <Counter />;
}

export default App;
```

**Expected output / result**

```text
Output: '+' increases and '-' decreases the count.
```

### Q.60 — Create a React form for feedback (name, message) and send the data to an Express server using a POST request. Store the data in MongoDB.

Setup: create an empty folder (for example MERN_FEEDBACK). Make sure MongoDB is running.

**Terminal / setup commands**

```bash
mkdir SERVER
cd SERVER
npm init -y
npm install express mongoose cors
cd ..
npm create vite@latest CLIENT
cd CLIENT
npm install
npm install axios
```

**File: `SERVER/server.js`**

```javascript
const express = require("express");
const mongoose = require("mongoose");
const cors = require("cors");

const app = express();
app.use(cors());
app.use(express.json());

mongoose.connect("mongodb://127.0.0.1:27017/trcac");

const Feedback = mongoose.model("Feedback", {
  name: String,
  message: String
});

app.post("/feedback", async (req, res) => {
  const feedback = new Feedback(req.body);
  await feedback.save();
  res.json({ message: "Feedback saved" });
});

app.listen(5000, () => {
  console.log("Server running on http://localhost:5000");
});
```

**File: `CLIENT/src/App.jsx`**

```jsx
import { useState } from "react";
import axios from "axios";

function App() {
  const [name, setName] = useState("");
  const [message, setMessage] = useState("");
  const [status, setStatus] = useState("");

  function handleSubmit(e) {
    e.preventDefault();
    axios.post("http://localhost:5000/feedback", { name: name, message: message })
      .then((res) => {
        setStatus(res.data.message);
        setName("");
        setMessage("");
      });
  }

  return (
    <div>
      <h1>Feedback Form</h1>
      <form onSubmit={handleSubmit}>
        <input type="text" placeholder="Your name" value={name}
          onChange={(e) => setName(e.target.value)} />
        <br />
        <textarea placeholder="Your message" value={message}
          onChange={(e) => setMessage(e.target.value)} />
        <br />
        <button type="submit">Send Feedback</button>
      </form>
      <p>{status}</p>
    </div>
  );
}

export default App;
```

**Terminal / setup commands**

```bash
SERVER terminal:  node server.js
CLIENT terminal:  npm run dev

Output: after clicking Send Feedback the message 'Feedback saved' is shown. To check the data in MongoDB use mongosh: use trcac, then db.feedbacks.find()
```

### Q.61 — Create a counter component using the useState hook with Increment, Decrement and Reset buttons.

**File: `src/App.jsx`**

```jsx
import { useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  return (
    <div style={{ textAlign: "center", marginTop: "50px" }}>
      <h1>Counter App</h1>
      <h2>{count}</h2>
      <button onClick={() => setCount(count + 1)}>Increment</button>
      <button onClick={() => setCount(count - 1)}>Decrement</button>
      <button onClick={() => setCount(0)}>Reset</button>
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: a counter with Increment, Decrement and Reset buttons.
```

### Q.62 — Create a React page that adds a new user through a form and displays the updated list of records dynamically after each insert without reloading the page.

Setup: create an empty folder (for example MERN_FEEDBACK). Make sure MongoDB is running.

**Terminal / setup commands**

```bash
mkdir SERVER
cd SERVER
npm init -y
npm install express mongoose cors
cd ..
npm create vite@latest CLIENT
cd CLIENT
npm install
npm install axios
```

**File: `SERVER/server.js`**

```javascript
const express = require("express");
const mongoose = require("mongoose");
const cors = require("cors");

const app = express();
app.use(cors());
app.use(express.json());

mongoose.connect("mongodb://127.0.0.1:27017/trcac");

const User = mongoose.model("User", {
  name: String,
  email: String
});

// GET all users
app.get("/users", async (req, res) => {
  const users = await User.find();
  res.json(users);
});

// ADD a user
app.post("/users", async (req, res) => {
  const user = new User(req.body);
  await user.save();
  res.json(user);
});

app.listen(5000, () => {
  console.log("Server running on http://localhost:5000");
});
```

**File: `CLIENT/src/App.jsx`**

```jsx
import { useEffect, useState } from "react";
import axios from "axios";

function App() {
  const [users, setUsers] = useState([]);
  const [name, setName] = useState("");
  const [email, setEmail] = useState("");

  function fetchUsers() {
    axios.get("http://localhost:5000/users")
      .then((res) => setUsers(res.data));
  }

  function addUser(e) {
    e.preventDefault();
    axios.post("http://localhost:5000/users", { name: name, email: email })
      .then(() => {
        setName("");
        setEmail("");
        fetchUsers();
      });
  }

  useEffect(() => {
    fetchUsers();
  }, []);

  return (
    <div>
      <h1>Add User</h1>
      <form onSubmit={addUser}>
        <input type="text" placeholder="Name" value={name}
          onChange={(e) => setName(e.target.value)} />
        <input type="email" placeholder="Email" value={email}
          onChange={(e) => setEmail(e.target.value)} />
        <button type="submit">Add</button>
      </form>

      <h2>Users</h2>
      {users.map((user) => (
        <p key={user._id}>{user.name} - {user.email}</p>
      ))}
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: after clicking Add the new user appears in the list immediately without reloading the page.
```

**Terminal / setup commands**

```bash
SERVER terminal:  node server.js
CLIENT terminal:  npm run dev

```

## D. React Router and Navigation

### Q.63 — React Routing - Create multiple pages and implement navigation between them.

> Setup (once): create a Vite app and install React Router and Axios.

**Terminal / setup commands**

```bash
npm create vite@latest react-router-demo
(select React -> JavaScript)
cd react-router-demo
npm install
npm install react-router-dom axios
npm run dev
```

**File: `src/main.jsx`**

```jsx
import { StrictMode } from "react";
import { createRoot } from "react-dom/client";
import { BrowserRouter } from "react-router-dom";
import App from "./App.jsx";

createRoot(document.getElementById("root")).render(
  <StrictMode>
    <BrowserRouter>
      <App />
    </BrowserRouter>
  </StrictMode>
);

Create a folder src/pages and add the page components (file names start with a capital letter).
```

**File: `src/pages/Home.jsx`**

```jsx
function Home() {
  return <h1>Home Page</h1>;
}

export default Home;
```

**File: `src/pages/About.jsx`**

```jsx
function About() {
  return <h1>About Page</h1>;
}

export default About;
```

**File: `src/pages/Users.jsx`**

```jsx
function Users() {
  return <h1>Users Page</h1>;
}

export default Users;
```

**File: `src/App.jsx`**

```jsx
import { Routes, Route, Link } from "react-router-dom";
import Home from "./pages/Home";
import About from "./pages/About";
import Users from "./pages/Users";

function App() {
  return (
    <>
      <nav>
        <Link to="/">Home</Link>
        <br />
        <Link to="/about">About</Link>
        <br />
        <Link to="/users">Users</Link>
      </nav>
      <hr />

      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/users" element={<Users />} />
      </Routes>
    </>
  );
}

export default App;
```

**Expected output / result**

```text
Output: clicking the links Home, About and Users changes the page without reloading.
```

### Q.64 — React Routing - Use Link and Routes to move between pages.

Link changes the URL without reloading the page. Routes and Route decide which component is shown for the URL. (Setup and page files are the same as Q.63)

**File: `src/App.jsx`**

```jsx
import { Routes, Route, Link } from "react-router-dom";
import Home from "./pages/Home";
import About from "./pages/About";
import Users from "./pages/Users";

function App() {
  return (
    <>
      <nav>
        <Link to="/">Home</Link>
        <br />
        <Link to="/about">About</Link>
        <br />
        <Link to="/users">Users</Link>
      </nav>
      <hr />

      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/users" element={<Users />} />
      </Routes>
    </>
  );
}

export default App;
```

**Expected output / result**

```text
Output: clicking the links Home, About and Users changes the page without reloading.
```

### Q.65 — React Routing - Fetch sample data from a public API using Axios.

Run npm install axios if it is not installed. The Users page below fetches data from jsonplaceholder.

**File: `src/pages/Users.jsx`**

```jsx
import { useEffect, useState } from "react";
import axios from "axios";

function Users() {
  const [users, setUsers] = useState([]);

  useEffect(() => {
    axios.get("https://jsonplaceholder.typicode.com/users")
      .then((response) => {
        setUsers(response.data);
      })
      .catch((error) => {
        console.log(error);
      });
  }, []);

  return (
    <div>
      <h2>User List</h2>
      <ul>
        {users.map((user) => (
          <li key={user.id}>{user.name}</li>
        ))}
      </ul>
    </div>
  );
}

export default Users;
```

**Expected output / result**

```text
Output: the names of 10 users fetched from the public API are listed.
```

### Q.66 — React Routing - Display fetched data in table or list format.

**File: `src/pages/Users.jsx`**

```jsx
import { useEffect, useState } from "react";
import axios from "axios";

function Users() {
  const [users, setUsers] = useState([]);

  useEffect(() => {
    axios.get("https://jsonplaceholder.typicode.com/users")
      .then((response) => setUsers(response.data))
      .catch((error) => console.log(error));
  }, []);

  return (
    <div>
      <h2>User List</h2>
      <table border="1" cellPadding="10">
        <thead>
          <tr>
            <th>ID</th>
            <th>Name</th>
            <th>Email</th>
            <th>City</th>
          </tr>
        </thead>
        <tbody>
          {users.map((user) => (
            <tr key={user.id}>
              <td>{user.id}</td>
              <td>{user.name}</td>
              <td>{user.email}</td>
              <td>{user.address.city}</td>
            </tr>
          ))}
        </tbody>
      </table>
    </div>
  );
}

export default Users;
```

**Expected output / result**

```text
Output: the fetched data is displayed in a table with ID, Name, Email and City.
```

### Q.67 — React Routing - Implement filter functionality on displayed data.

**File: `src/pages/Users.jsx`**

```jsx
import { useEffect, useState } from "react";
import axios from "axios";

function Users() {
  const [users, setUsers] = useState([]);
  const [search, setSearch] = useState("");

  useEffect(() => {
    axios.get("https://jsonplaceholder.typicode.com/users")
      .then((response) => setUsers(response.data))
      .catch((error) => console.log(error));
  }, []);

  const filteredUsers = users.filter((user) =>
    user.name.toLowerCase().includes(search.toLowerCase())
  );

  return (
    <div>
      <h2>User List</h2>
      <input
        type="text"
        placeholder="Search user..."
        value={search}
        onChange={(e) => setSearch(e.target.value)}
      />
      <table border="1" cellPadding="10">
        <thead>
          <tr>
            <th>ID</th>
            <th>Name</th>
            <th>Email</th>
            <th>City</th>
          </tr>
        </thead>
        <tbody>
          {filteredUsers.map((user) => (
            <tr key={user.id}>
              <td>{user.id}</td>
              <td>{user.name}</td>
              <td>{user.email}</td>
              <td>{user.address.city}</td>
            </tr>
          ))}
        </tbody>
      </table>
    </div>
  );
}

export default Users;
```

**Expected output / result**

```text
Output: typing in the search box filters the table rows by user name.
```

### Q.68 — Create a React Application with Multiple Pages and Implement Navigation Between Them Using React Router. Note: Student has to install react-router-dom.

> Setup (once): create a Vite app and install React Router and Axios.

**Terminal / setup commands**

```bash
npm create vite@latest react-router-demo
(select React -> JavaScript)
cd react-router-demo
npm install
npm install react-router-dom axios
npm run dev
```

**File: `src/main.jsx`**

```jsx
import { StrictMode } from "react";
import { createRoot } from "react-dom/client";
import { BrowserRouter } from "react-router-dom";
import App from "./App.jsx";

createRoot(document.getElementById("root")).render(
  <StrictMode>
    <BrowserRouter>
      <App />
    </BrowserRouter>
  </StrictMode>
);
```

**File: `src/pages/Home.jsx`**

```jsx
function Home() {
  return <h1>Home Page</h1>;
}

export default Home;
```

**File: `src/pages/About.jsx`**

```jsx
function About() {
  return <h1>About Page</h1>;
}

export default About;
```

**File: `src/pages/Users.jsx`**

```jsx
function Users() {
  return <h1>Users Page</h1>;
}

export default Users;
```

**File: `src/App.jsx`**

```jsx
import { Routes, Route, Link } from "react-router-dom";
import Home from "./pages/Home";
import About from "./pages/About";
import Users from "./pages/Users";

function App() {
  return (
    <>
      <nav>
        <Link to="/">Home</Link>
        <br />
        <Link to="/about">About</Link>
        <br />
        <Link to="/users">Users</Link>
      </nav>
      <hr />

      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/users" element={<Users />} />
      </Routes>
    </>
  );
}

export default App;
```

**Expected output / result**

```text
Output: clicking the links Home, About and Users changes the page without reloading.
```

### Q.69 — Create Home, About, and Contact Components in React and Configure Routes for Each Page Using React Router. Note: Student has to install react-router-dom.

> Setup (once): create a Vite app and install React Router and Axios.

**Terminal / setup commands**

```bash
npm create vite@latest react-router-demo
(select React -> JavaScript)
cd react-router-demo
npm install
npm install react-router-dom axios
npm run dev
```

**File: `src/main.jsx`**

```jsx
import { StrictMode } from "react";
import { createRoot } from "react-dom/client";
import { BrowserRouter } from "react-router-dom";
import App from "./App.jsx";

createRoot(document.getElementById("root")).render(
  <StrictMode>
    <BrowserRouter>
      <App />
    </BrowserRouter>
  </StrictMode>
);
```

**File: `src/pages/Home.jsx`**

```jsx
function Home() {
  return <h1>Home Page</h1>;
}

export default Home;
```

**File: `src/pages/About.jsx`**

```jsx
function About() {
  return <h1>About Page</h1>;
}

export default About;
```

**File: `src/pages/Contact.jsx`**

```jsx
function Contact() {
  return <h1>Contact Page</h1>;
}

export default Contact;
```

**File: `src/App.jsx`**

```jsx
import { Routes, Route, Link } from "react-router-dom";
import Home from "./pages/Home";
import About from "./pages/About";
import Contact from "./pages/Contact";

function App() {
  return (
    <>
      <nav>
        <Link to="/">Home</Link> |{" "}
        <Link to="/about">About</Link> |{" "}
        <Link to="/contact">Contact</Link>
      </nav>
      <hr />

      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </>
  );
}

export default App;
```

**Expected output / result**

```text
Output: a navigation bar with Home | About | Contact; each link opens its own page.
```

### Q.70 — Create a React Application to Implement Navigation Between Different Pages Using the Link and Routes Components of React Router. Note: Student has to install react-router-dom.

> Setup (once): create a Vite app and install React Router and Axios.

**Terminal / setup commands**

```bash
npm create vite@latest react-router-demo
(select React -> JavaScript)
cd react-router-demo
npm install
npm install react-router-dom axios
npm run dev
```

**File: `src/main.jsx`**

```jsx
import { StrictMode } from "react";
import { createRoot } from "react-dom/client";
import { BrowserRouter } from "react-router-dom";
import App from "./App.jsx";

createRoot(document.getElementById("root")).render(
  <StrictMode>
    <BrowserRouter>
      <App />
    </BrowserRouter>
  </StrictMode>
);
```

**File: `src/pages/Home.jsx`**

```jsx
function Home() {
  return <h1>Home Page</h1>;
}

export default Home;
```

**File: `src/pages/About.jsx`**

```jsx
function About() {
  return <h1>About Page</h1>;
}

export default About;
```

**File: `src/pages/Contact.jsx`**

```jsx
function Contact() {
  return <h1>Contact Page</h1>;
}

export default Contact;
```

**File: `src/App.jsx`**

```jsx
import { Routes, Route, Link } from "react-router-dom";
import Home from "./pages/Home";
import About from "./pages/About";
import Contact from "./pages/Contact";

function App() {
  return (
    <>
      <nav>
        <Link to="/">Home</Link> |{" "}
        <Link to="/about">About</Link> |{" "}
        <Link to="/contact">Contact</Link>
      </nav>
      <hr />

      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </>
  );
}

export default App;
```

**Expected output / result**

```text
Output: a navigation bar with Home | About | Contact; each link opens its own page.
```

### Q.71 — Install and configure React Router. Create Home, About and Contact pages and implement navigation between them using a navigation bar.

> Setup (once): create a Vite app and install React Router and Axios.

**Terminal / setup commands**

```bash
npm create vite@latest react-router-demo
(select React -> JavaScript)
cd react-router-demo
npm install
npm install react-router-dom axios
npm run dev
```

**File: `src/main.jsx`**

```jsx
import { StrictMode } from "react";
import { createRoot } from "react-dom/client";
import { BrowserRouter } from "react-router-dom";
import App from "./App.jsx";

createRoot(document.getElementById("root")).render(
  <StrictMode>
    <BrowserRouter>
      <App />
    </BrowserRouter>
  </StrictMode>
);
```

**File: `src/pages/Home.jsx`**

```jsx
function Home() {
  return <h1>Home Page</h1>;
}

export default Home;
```

**File: `src/pages/About.jsx`**

```jsx
function About() {
  return <h1>About Page</h1>;
}

export default About;
```

**File: `src/pages/Contact.jsx`**

```jsx
function Contact() {
  return <h1>Contact Page</h1>;
}

export default Contact;
```

**File: `src/App.jsx`**

```jsx
import { Routes, Route, Link } from "react-router-dom";
import Home from "./pages/Home";
import About from "./pages/About";
import Contact from "./pages/Contact";

function App() {
  return (
    <>
      <nav>
        <Link to="/">Home</Link> |{" "}
        <Link to="/about">About</Link> |{" "}
        <Link to="/contact">Contact</Link>
      </nav>
      <hr />

      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
        <Route path="/contact" element={<Contact />} />
      </Routes>
    </>
  );
}

export default App;
```

**Expected output / result**

```text
Output: a navigation bar with Home | About | Contact; each link opens its own page.
```

## E. Node.js and Express

### Q.72 — Display a message on the browser using the server response.

> Setup (once): create a project folder and install Express.

**Terminal / setup commands**

```bash
mkdir express-demo
cd express-demo
npm init -y
npm install express
```

**File: `server.js`**

```javascript
const express = require("express");
const app = express();
const PORT = 3000;

app.get("/", (req, res) => {
    res.send("Welcome to Express Server");
});

app.listen(PORT, () => {
    console.log(`Server is running on http://localhost:${PORT}`);
});
```

**Terminal / setup commands**

```bash
node server.js

Output: terminal shows 'Server is running on http://localhost:3000' and the browser shows 'Welcome to Express Server'. (Add a screenshot of the VS Code terminal and the browser.)
```

### Q.73 — Express fundamentals - Create different routes in Express.

> Setup (once): create a project folder and install Express.

**Terminal / setup commands**

```bash
mkdir express-demo
cd express-demo
npm init -y
npm install express
```

**File: `server.js`**

```javascript
const express = require("express");
const app = express();
const PORT = 3000;

// Home Route
app.get("/", (req, res) => {
    console.log("Home route visited");
    res.send("Welcome to Express Server");
});

// About Route
app.get("/about", (req, res) => {
    console.log("About route visited");
    res.send("This is About Page");
});

// Contact Route
app.get("/contact", (req, res) => {
    console.log("Contact route visited");
    res.send("Contact Us");
});

app.listen(PORT, () => {
    console.log(`Server is running on http://localhost:${PORT}`);
});
```

**Terminal / setup commands**

```bash
node server.js

Output: open http://localhost:3000/, /about and /contact in the browser. The terminal prints a message each time a route is visited.
```

### Q.74 — Node.js and Express - Send a JSON response from the server.

> Setup (once): create a project folder and install Express.

**Terminal / setup commands**

```bash
mkdir express-demo
cd express-demo
npm init -y
npm install express
```

**File: `server.js`**

```javascript
const express = require("express");
const app = express();
const PORT = 3000;

app.get("/student", (req, res) => {
    res.json({
        id: 101,
        name: "John",
        course: "Node.js",
        college: "ABC College"
    });
});

app.listen(PORT, () => {
    console.log(`Server is running on http://localhost:${PORT}`);
});
```

**Terminal / setup commands**

```bash
node server.js

Output: http://localhost:3000/student shows the JSON object {id: 101, name: John, course: Node.js, college: ABC College}.
```

### Q.75 — Create a simple REST API using Express.

> Setup (once): create a project folder and install Express.

**Terminal / setup commands**

```bash
mkdir express-demo
cd express-demo
npm init -y
npm install express
```

**File: `server.js`**

```javascript
const express = require("express");
const app = express();
app.use(express.json());

let students = [
    { id: 1, name: "Aarav" },
    { id: 2, name: "Riya" }
];

// GET - read data
app.get("/students", (req, res) => {
    res.json(students);
});

// POST - add data
app.post("/students", (req, res) => {
    const student = req.body;
    students.push(student);
    res.json({ message: "Student added", student: student });
});

app.listen(3000, () => {
    console.log("Server is running on http://localhost:3000");
});
```

**Terminal / setup commands**

```bash
node server.js

Test: open http://localhost:3000/students in the browser for GET. For POST use Postman: POST http://localhost:3000/students with Body -> raw -> JSON {"id": 3, "name": "Karan"}
```

### Q.76 — Implement a GET API to retrieve data.

> Setup (once): create a project folder and install Express.

**Terminal / setup commands**

```bash
mkdir express-demo
cd express-demo
npm init -y
npm install express
```

**File: `server.js`**

```javascript
const express = require("express");
const app = express();

let students = [
    { id: 1, name: "Aarav", course: "TYIT" },
    { id: 2, name: "Riya", course: "TYCS" },
    { id: 3, name: "Karan", course: "TYIT" }
];

app.get("/students", (req, res) => {
    res.json(students);
});

app.listen(3000, () => {
    console.log("Server is running on http://localhost:3000");
});
```

**Terminal / setup commands**

```bash
node server.js

Output: http://localhost:3000/students returns the list of three students in JSON format.
```

### Q.77 — Create different routes in Express.

> Setup (once): create a project folder and install Express.

**Terminal / setup commands**

```bash
mkdir express-demo
cd express-demo
npm init -y
npm install express
```

**File: `server.js`**

```javascript
const express = require("express");
const app = express();
const PORT = 3000;

// Home Route
app.get("/", (req, res) => {
    console.log("Home route visited");
    res.send("Welcome to Express Server");
});

// About Route
app.get("/about", (req, res) => {
    console.log("About route visited");
    res.send("This is About Page");
});

// Contact Route
app.get("/contact", (req, res) => {
    console.log("Contact route visited");
    res.send("Contact Us");
});

app.listen(PORT, () => {
    console.log(`Server is running on http://localhost:${PORT}`);
});
```

**Terminal / setup commands**

```bash
node server.js

```

### Q.78 — Node.js and Express - Implement frontend form validation.

Frontend form validation is done in React before the data is sent to the server. Create a Vite React app (npm create vite@latest) and replace src/App.jsx.

**File: `src/App.jsx`**

```jsx
import { useState } from "react";

function App() {
  const [name, setName] = useState("");
  const [email, setEmail] = useState("");
  const [password, setPassword] = useState("");
  const [errors, setErrors] = useState({});
  const [success, setSuccess] = useState("");

  function handleSubmit(e) {
    e.preventDefault();
    let newErrors = {};

    if (name.trim() == "") {
      newErrors.name = "Name is required";
    }
    if (!email.includes("@")) {
      newErrors.email = "Enter a valid email";
    }
    if (password.length < 6) {
      newErrors.password = "Password must be at least 6 characters";
    }

    setErrors(newErrors);

    if (Object.keys(newErrors).length == 0) {
      setSuccess("Form submitted successfully");
    } else {
      setSuccess("");
    }
  }

  return (
    <div>
      <h1>Registration Form</h1>
      <form onSubmit={handleSubmit}>
        <input type="text" placeholder="Name" value={name}
          onChange={(e) => setName(e.target.value)} />
        <p style={{ color: "red" }}>{errors.name}</p>

        <input type="text" placeholder="Email" value={email}
          onChange={(e) => setEmail(e.target.value)} />
        <p style={{ color: "red" }}>{errors.email}</p>

        <input type="password" placeholder="Password" value={password}
          onChange={(e) => setPassword(e.target.value)} />
        <p style={{ color: "red" }}>{errors.password}</p>

        <button type="submit">Register</button>
      </form>
      <p style={{ color: "green" }}>{success}</p>
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: wrong or empty fields show red error messages; a valid form shows 'Form submitted successfully'.
```

### Q.79 — Create a REST API using Node.js and Express to display a welcome message. Create a GET API to retrieve a list of student records in JSON format. Create a GET API to retrieve a specific student record using its ID. Create a POST API to accept new student details from the client. Create a React application to fetch and display student data from an Express API using Axios.

**Terminal / setup commands**

```bash
mkdir SERVER
cd SERVER
npm init -y
npm install express cors
cd ..
npm create vite@latest CLIENT
cd CLIENT
npm install
npm install axios
```

**File: `SERVER/server.js`**

```javascript
const express = require("express");
const cors = require("cors");
const app = express();

app.use(cors());
app.use(express.json());

let students = [
    { id: 1, name: "Aarav", course: "TYIT" },
    { id: 2, name: "Riya", course: "TYCS" },
    { id: 3, name: "Karan", course: "TYIT" }
];

// Welcome message
app.get("/", (req, res) => {
    res.send("Welcome to Student API");
});

// All students
app.get("/students", (req, res) => {
    res.json(students);
});

// Student by ID
app.get("/students/:id", (req, res) => {
    const student = students.find((s) => s.id == req.params.id);
    if (student) {
        res.json(student);
    } else {
        res.status(404).json({ message: "Student not found" });
    }
});

// Add new student
app.post("/students", (req, res) => {
    const student = req.body;
    students.push(student);
    res.json(student);
});

app.listen(5000, () => {
    console.log("Server running on http://localhost:5000");
});
```

**File: `CLIENT/src/App.jsx`**

```jsx
import { useEffect, useState } from "react";
import axios from "axios";

function App() {
  const [students, setStudents] = useState([]);

  useEffect(() => {
    axios.get("http://localhost:5000/students")
      .then((res) => setStudents(res.data));
  }, []);

  return (
    <div>
      <h1>Student List</h1>
      <table border="1" cellPadding="8">
        <thead>
          <tr>
            <th>ID</th>
            <th>Name</th>
            <th>Course</th>
          </tr>
        </thead>
        <tbody>
          {students.map((s) => (
            <tr key={s.id}>
              <td>{s.id}</td>
              <td>{s.name}</td>
              <td>{s.course}</td>
            </tr>
          ))}
        </tbody>
      </table>
    </div>
  );
}

export default App;
```

**Terminal / setup commands**

```bash
SERVER terminal:  node server.js
CLIENT terminal:  npm run dev

Test in browser / Postman: GET http://localhost:5000/  |  GET /students  |  GET /students/2  |  POST /students with JSON {"id": 4, "name": "Neha", "course": "TYIT"}
```

### Q.80 — Create a simple REST API using Express with a GET route /api/books that retrieves the list of books from MongoDB. Test it in the browser and Postman.

First insert sample books in mongosh:

**Terminal / setup commands**

```bash
use trcac
db.books.insertMany([
  { title: "JavaScript Basics", author: "John", price: 350 },
  { title: "React Guide", author: "Mary", price: 450 }
])

Terminal
mkdir books-api
cd books-api
npm init -y
npm install express mongoose
```

**File: `server.js`**

```javascript
const express = require("express");
const mongoose = require("mongoose");
const app = express();

mongoose.connect("mongodb://127.0.0.1:27017/trcac");

const Book = mongoose.model("Book", {
    title: String,
    author: String,
    price: Number
});

app.get("/api/books", async (req, res) => {
    const books = await Book.find();
    res.json(books);
});

app.listen(3000, () => {
    console.log("Server running on http://localhost:3000");
});
```

**Terminal / setup commands**

```bash
node server.js

Test: browser -> http://localhost:3000/api/books. Postman -> select GET, enter the same URL and click Send. The list of books in JSON is returned.
```

### Q.81 — Verify the Node.js and npm installation by displaying their versions in the terminal. Write a program using variables and a function to calculate the area and perimeter of a rectangle.

**Terminal / setup commands**

```bash
node --version
npm --version
```

**File: `rectangle.js`**

```javascript
let length = 10;
let breadth = 5;

function area(l, b) {
    return l * b;
}

function perimeter(l, b) {
    return 2 * (l + b);
}

console.log("Area =", area(length, breadth));
console.log("Perimeter =", perimeter(length, breadth));
```

**Expected output / result**

```text
Area = 50
Perimeter = 30
```

### Q.82 — Create an Express GET API for students and fetch the data from it in a React application using Axios. Display the students in a list.

**Terminal / setup commands**

```bash
mkdir SERVER
cd SERVER
npm init -y
npm install express cors
cd ..
npm create vite@latest CLIENT
cd CLIENT
npm install
npm install axios
```

**File: `SERVER/server.js`**

```javascript
const express = require("express");
const cors = require("cors");
const app = express();
app.use(cors());

let students = [
    { id: 1, name: "Aarav" },
    { id: 2, name: "Riya" },
    { id: 3, name: "Karan" }
];

app.get("/students", (req, res) => {
    res.json(students);
});

app.listen(5000, () => {
    console.log("Server running on http://localhost:5000");
});
```

**File: `CLIENT/src/App.jsx`**

```jsx
import { useEffect, useState } from "react";
import axios from "axios";

function App() {
  const [students, setStudents] = useState([]);

  useEffect(() => {
    axios.get("http://localhost:5000/students")
      .then((res) => setStudents(res.data));
  }, []);

  return (
    <div>
      <h1>Students</h1>
      <ul>
        {students.map((s) => (
          <li key={s.id}>{s.name}</li>
        ))}
      </ul>
    </div>
  );
}

export default App;
```

**Terminal / setup commands**

```bash
SERVER terminal:  node server.js
CLIENT terminal:  npm run dev

```

### Q.83 — Create an Express route GET /api/books that returns a list of books. Test the route using the browser and Postman.

> Setup (once): create a project folder and install Express.

**Terminal / setup commands**

```bash
mkdir express-demo
cd express-demo
npm init -y
npm install express
```

**File: `server.js`**

```javascript
const express = require("express");
const app = express();

let books = [
    { id: 1, title: "JavaScript Basics", author: "John" },
    { id: 2, title: "React Guide", author: "Mary" },
    { id: 3, title: "Node.js Guide", author: "Sam" }
];

app.get("/api/books", (req, res) => {
    res.json(books);
});

app.listen(3000, () => {
    console.log("Server running on http://localhost:3000");
});
```

**Terminal / setup commands**

```bash
node server.js

Test: browser -> http://localhost:3000/api/books. Postman -> GET method, same URL, click Send. The list of books in JSON is displayed.
```

### Q.84 — Create an Express server with a middleware that logs the request method and URL in the console. Create two routes and run the server.

> Setup (once): create a project folder and install Express.

**Terminal / setup commands**

```bash
mkdir express-demo
cd express-demo
npm init -y
npm install express
```

**File: `server.js`**

```javascript
const express = require("express");
const app = express();

// Middleware - runs for every request
app.use((req, res, next) => {
    console.log(req.method, req.url);
    next();
});

app.get("/", (req, res) => {
    res.send("Home Page");
});

app.get("/about", (req, res) => {
    res.send("About Page");
});

app.listen(3000, () => {
    console.log("Server running on http://localhost:3000");
});
```

**Terminal / setup commands**

```bash
node server.js

Output: visiting / and /about prints 'GET /' and 'GET /about' in the terminal.
```

### Q.85 — Create an Express server for a library with the routes /books and /members that display different messages. Run the server and observe the output in the console.

> Setup (once): create a project folder and install Express.

**Terminal / setup commands**

```bash
mkdir express-demo
cd express-demo
npm init -y
npm install express
```

**File: `server.js`**

```javascript
const express = require("express");
const app = express();

app.get("/books", (req, res) => {
    console.log("Books route visited");
    res.send("List of library books");
});

app.get("/members", (req, res) => {
    console.log("Members route visited");
    res.send("List of library members");
});

app.listen(3000, () => {
    console.log("Library server running on http://localhost:3000");
});
```

**Terminal / setup commands**

```bash
node server.js

Output: /books shows 'List of library books', /members shows 'List of library members' and the console prints a message for each visit.
```

## F. MongoDB and Database Operations

### Q.86 — MongoDB - Create a database and collection and insert records.

Start MongoDB and open mongosh in the terminal, then type the commands below.

**Terminal / setup commands**

```bash
use trcac
db.createCollection("tyit")
show collections

db.tyit.insertOne({ rollno: 1, name: "Gauri", age: 20, city: "Mumbai" })

db.tyit.insertMany([
  { rollno: 2, name: "Priya", age: 21, city: "Pune" },
  { rollno: 3, name: "Aman", age: 22, city: "Delhi" }
])

db.tyit.find()

```

### Q.87 — Express and MongoDB - Retrieve and display user data from MongoDB.

**Terminal / setup commands**

```bash
mkdir SERVER
cd SERVER
npm init -y
npm install express mongoose cors
```

**File: `SERVER/server.js`**

```javascript
const express = require("express");
const mongoose = require("mongoose");
const cors = require("cors");

const app = express();
app.use(cors());
app.use(express.json());

mongoose.connect("mongodb://127.0.0.1:27017/trcac");

const User = mongoose.model("User", {
  name: String,
  email: String
});

// Retrieve all users
app.get("/users", async (req, res) => {
  const users = await User.find();
  res.json(users);
});

app.listen(5000, () => {
  console.log("Server running on http://localhost:5000");
});
```

**Terminal / setup commands**

```bash
node server.js

Output: open http://localhost:5000/users in the browser to see the user records from MongoDB in JSON format.
```

### Q.88 — Express and MongoDB - Implement an update operation for existing records.

**Terminal / setup commands**

```bash
mkdir SERVER
cd SERVER
npm init -y
npm install express mongoose cors
```

**File: `SERVER/server.js`**

```javascript
const express = require("express");
const mongoose = require("mongoose");
const cors = require("cors");

const app = express();
app.use(cors());
app.use(express.json());

mongoose.connect("mongodb://127.0.0.1:27017/trcac");

const User = mongoose.model("User", {
  name: String,
  email: String
});

// Update a user using its id
app.put("/users/:id", async (req, res) => {
  const user = await User.findByIdAndUpdate(
    req.params.id,
    req.body,
    { new: true }
  );
  res.json(user);
});

app.listen(5000, () => {
  console.log("Server running on http://localhost:5000");
});

Test in Postman: PUT http://localhost:5000/users/<id>  Body -> raw -> JSON: {"name": "Gauri Shah", "email": "gauri@gmail.com"}  (copy the _id from the MongoDB record).
```

### Q.89 — Express and MongoDB - Implement the delete operation for selected records.

**Terminal / setup commands**

```bash
mkdir SERVER
cd SERVER
npm init -y
npm install express mongoose cors
```

**File: `SERVER/server.js`**

```javascript
const express = require("express");
const mongoose = require("mongoose");
const cors = require("cors");

const app = express();
app.use(cors());
app.use(express.json());

mongoose.connect("mongodb://127.0.0.1:27017/trcac");

const User = mongoose.model("User", {
  name: String,
  email: String
});

// Delete a user using its id
app.delete("/users/:id", async (req, res) => {
  await User.findByIdAndDelete(req.params.id);
  res.json({ message: "Deleted" });
});

app.listen(5000, () => {
  console.log("Server running on http://localhost:5000");
});

Test in Postman: DELETE http://localhost:5000/users/<id>  The response is {"message": "Deleted"}.
```

### Q.90 — Insert and update records in MongoDB.

Start MongoDB and open mongosh in the terminal, then type the commands below.

**Terminal / setup commands**

```bash
use trcac
db.tyit.insertOne({ rollno: 4, name: "Neha", age: 20, city: "Thane" })

db.tyit.updateOne(
  { name: "Neha" },
  { $set: { age: 25 } }
)

db.tyit.find({ name: "Neha" })

```

### Q.91 — Insert and delete records in MongoDB.

Start MongoDB and open mongosh in the terminal, then type the commands below.

**Terminal / setup commands**

```bash
use trcac
db.tyit.insertOne({ rollno: 5, name: "Rahul", age: 22, city: "Pune" })

db.tyit.deleteOne({ rollno: 5 })

db.tyit.find()

```

### Q.92 — Connect MongoDB with Node.js.

**Terminal / setup commands**

```bash
mkdir mongo-demo
cd mongo-demo
npm init -y
npm install mongodb
```

**File: `demo.js`**

```javascript
const mongodb = require("mongodb");
const url = "mongodb://127.0.0.1:27017";
const client = new mongodb.MongoClient(url);

async function main() {
    try {
        await client.connect();
        console.log("Connected Successfully");

        const db = client.db("trcac");
        const collection = db.collection("tyit");

        const data = await collection.find().toArray();
        console.log("Records in Collection:");
        console.table(data);
    } catch (error) {
        console.error("Error:", error);
    } finally {
        await client.close();
        console.log("Connection Closed");
    }
}

main();
```

**Terminal / setup commands**

```bash
node demo.js

Output: 'Connected Successfully', then the records of the tyit collection in table format, then 'Connection Closed'.
```

### Q.93 — Store data in MongoDB.

Use the same mongo-demo project as Q.92 (mongodb package installed).

**File: `store.js`**

```javascript
const mongodb = require("mongodb");
const client = new mongodb.MongoClient("mongodb://127.0.0.1:27017");

async function main() {
    try {
        await client.connect();
        const collection = client.db("trcac").collection("tyit");

        // Insert one record
        const result = await collection.insertOne({
            rollno: 10,
            name: "Rahul",
            age: 20,
            city: "Mumbai"
        });
        console.log("Inserted ID:", result.insertedId);

        // Insert many records
        await collection.insertMany([
            { rollno: 11, name: "Sneha", age: 21, city: "Pune" },
            { rollno: 12, name: "Amit", age: 22, city: "Nashik" }
        ]);
        console.log("Multiple records inserted");
    } catch (error) {
        console.error("Error:", error);
    } finally {
        await client.close();
    }
}

main();
```

**Terminal / setup commands**

```bash
node store.js

```

### Q.94 — Create a collection named Students in the CollegeDB database. Insert a single student document into the Students collection. Insert multiple student documents into the Students collection. Display all student records using the find() method. Retrieve a student record based on a specific roll number. Retrieve students whose marks are greater than 75. Delete a student record using deleteOne().

Start MongoDB and open mongosh in the terminal, then type the commands below.

**Terminal / setup commands**

```bash
use CollegeDB
db.createCollection("Students")

// insert single document
db.Students.insertOne({ rollno: 1, name: "Aarav", marks: 80 })

// insert multiple documents
db.Students.insertMany([
  { rollno: 2, name: "Riya", marks: 72 },
  { rollno: 3, name: "Karan", marks: 90 },
  { rollno: 4, name: "Neha", marks: 65 }
])

// display all records
db.Students.find()

// record of a specific roll number
db.Students.find({ rollno: 3 })

// students whose marks are greater than 75
db.Students.find({ marks: { $gt: 75 } })

// delete a record
db.Students.deleteOne({ rollno: 4 })

```

### Q.95 — (a) Install and start MongoDB. Create a database named college and a collection named students using mongosh (b) Design a React registration form that sends the user data (name, e-mail, city) to the backend API. Show a success message after submission.

(a) Install MongoDB Community Server from https://www.mongodb.com/try/download/community and start it. Then open mongosh:

**Terminal / setup commands**

```bash
use college
db.createCollection("students")
show collections

(b) Backend and React form
Terminal
mkdir SERVER
cd SERVER
npm init -y
npm install express mongoose cors
cd ..
npm create vite@latest CLIENT
cd CLIENT
npm install
npm install axios
```

**File: `SERVER/server.js`**

```javascript
const express = require("express");
const mongoose = require("mongoose");
const cors = require("cors");

const app = express();
app.use(cors());
app.use(express.json());

mongoose.connect("mongodb://127.0.0.1:27017/college");

const Student = mongoose.model("Student", {
  name: String,
  email: String,
  city: String
});

app.post("/register", async (req, res) => {
  const student = new Student(req.body);
  await student.save();
  res.json({ message: "Registration successful" });
});

app.listen(5000, () => {
  console.log("Server running on http://localhost:5000");
});
```

**File: `CLIENT/src/App.jsx`**

```jsx
import { useState } from "react";
import axios from "axios";

function App() {
  const [name, setName] = useState("");
  const [email, setEmail] = useState("");
  const [city, setCity] = useState("");
  const [message, setMessage] = useState("");

  function handleSubmit(e) {
    e.preventDefault();
    axios.post("http://localhost:5000/register", {
      name: name,
      email: email,
      city: city
    }).then((res) => {
      setMessage(res.data.message);
      setName("");
      setEmail("");
      setCity("");
    });
  }

  return (
    <div>
      <h1>Registration Form</h1>
      <form onSubmit={handleSubmit}>
        <input type="text" placeholder="Name" value={name}
          onChange={(e) => setName(e.target.value)} />
        <br />
        <input type="email" placeholder="E-mail" value={email}
          onChange={(e) => setEmail(e.target.value)} />
        <br />
        <input type="text" placeholder="City" value={city}
          onChange={(e) => setCity(e.target.value)} />
        <br />
        <button type="submit">Register</button>
      </form>
      <p style={{ color: "green" }}>{message}</p>
    </div>
  );
}

export default App;
```

**Terminal / setup commands**

```bash
SERVER terminal:  node server.js
CLIENT terminal:  npm run dev

Output: after clicking Register the message 'Registration successful' is displayed and the data is stored in the college database (db.students.find()).
```

### Q.96 — Write a Node.js script that connects to MongoDB using Mongoose, inserts a document in the students collection and displays it in the console.

**Terminal / setup commands**

```bash
mkdir mongoose-demo
cd mongoose-demo
npm init -y
npm install mongoose
```

**File: `app.js`**

```javascript
const mongoose = require("mongoose");

async function main() {
    await mongoose.connect("mongodb://127.0.0.1:27017/college");
    console.log("Connected to MongoDB");

    const Student = mongoose.model("Student", {
        name: String,
        rollno: Number,
        course: String
    });

    const student = await Student.create({
        name: "Aarav",
        rollno: 101,
        course: "TYIT"
    });

    console.log("Inserted document:", student);

    await mongoose.disconnect();
}

main();
```

**Terminal / setup commands**

```bash
node app.js

Output: 'Connected to MongoDB' followed by the inserted document with its _id.
```

### Q.97 — In an employees collection, increase the salary of all employees of a given department and delete the record of a resigned employee.

Start MongoDB and open mongosh in the terminal, then type the commands below.

**Terminal / setup commands**

```bash
use company
db.employees.insertMany([
  { name: "Amit", department: "IT", salary: 30000 },
  { name: "Sneha", department: "IT", salary: 35000 },
  { name: "Ravi", department: "HR", salary: 28000 }
])

// increase salary of all employees of the IT department by 5000
db.employees.updateMany(
  { department: "IT" },
  { $inc: { salary: 5000 } }
)

// delete the record of a resigned employee
db.employees.deleteOne({ name: "Ravi" })

db.employees.find()

```

## G. React, Express and MongoDB Integration

### Q.98 — Create an API to add user details using Express and MongoDB.

> Setup (once): create a folder MERN_USERS with two folders - SERVER (backend) and CLIENT (frontend). MongoDB must be running.

**Terminal / setup commands**

```bash
mkdir SERVER
cd SERVER
npm init -y
npm install express mongoose cors
```

**File: `SERVER/server.js`**

```javascript
const express = require("express");
const mongoose = require("mongoose");
const cors = require("cors");

const app = express();
app.use(cors());
app.use(express.json());

mongoose.connect("mongodb://127.0.0.1:27017/trcac");

const User = mongoose.model("User", {
  name: String,
  email: String
});

// GET all users
app.get("/users", async (req, res) => {
  const users = await User.find();
  res.json(users);
});

// ADD a user
app.post("/users", async (req, res) => {
  const user = new User(req.body);
  await user.save();
  res.json(user);
});

app.listen(5000, () => {
  console.log("Server running on http://localhost:5000");
});
```

**Terminal / setup commands**

```bash
node server.js

Test in Postman: POST http://localhost:5000/users  Body -> raw -> JSON: {"name": "Gauri", "email": "gauri@gmail.com"}. The saved user is returned.
```

### Q.99 — Design a React form to send user data to the backend.

The backend of Q.98 must be running (node server.js).

**Terminal / setup commands**

```bash
cd ..
npm create vite@latest CLIENT
cd CLIENT
npm install
npm install axios
npm run dev
```

**File: `CLIENT/src/App.jsx`**

```jsx
import { useState } from "react";
import axios from "axios";

function App() {
  const [name, setName] = useState("");
  const [email, setEmail] = useState("");

  function addUser(e) {
    e.preventDefault();
    axios.post("http://localhost:5000/users", { name: name, email: email })
      .then(() => {
        alert("User added");
        setName("");
        setEmail("");
      });
  }

  return (
    <div>
      <h1>User Form</h1>
      <form onSubmit={addUser}>
        <input type="text" placeholder="Name" value={name}
          onChange={(e) => setName(e.target.value)} />
        <input type="email" placeholder="Email" value={email}
          onChange={(e) => setEmail(e.target.value)} />
        <button type="submit">Add User</button>
      </form>
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: after clicking Add User an alert 'User added' is shown and the user is saved in MongoDB.
```

### Q.100 — Display database records dynamically in React.

The backend of Q.98 must be running (it has the GET /users route).

**File: `CLIENT/src/App.jsx`**

```jsx
import { useEffect, useState } from "react";
import axios from "axios";

function App() {
  const [users, setUsers] = useState([]);

  useEffect(() => {
    axios.get("http://localhost:5000/users")
      .then((res) => setUsers(res.data));
  }, []);

  return (
    <div>
      <h1>Users</h1>
      {users.map((user) => (
        <p key={user._id}>{user.name} - {user.email}</p>
      ))}
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: all the users stored in MongoDB are displayed on the page.
```

### Q.101 — Perform insert using UI.

The form adds the user to MongoDB and the list refreshes automatically. Backend: same as Q.98.

**File: `CLIENT/src/App.jsx`**

```jsx
import { useEffect, useState } from "react";
import axios from "axios";

function App() {
  const [users, setUsers] = useState([]);
  const [name, setName] = useState("");
  const [email, setEmail] = useState("");

  function fetchUsers() {
    axios.get("http://localhost:5000/users")
      .then((res) => setUsers(res.data));
  }

  function addUser(e) {
    e.preventDefault();
    axios.post("http://localhost:5000/users", { name: name, email: email })
      .then(() => {
        setName("");
        setEmail("");
        fetchUsers();
      });
  }

  useEffect(() => {
    fetchUsers();
  }, []);

  return (
    <div>
      <h1>Add User</h1>
      <form onSubmit={addUser}>
        <input type="text" placeholder="Name" value={name}
          onChange={(e) => setName(e.target.value)} />
        <input type="email" placeholder="Email" value={email}
          onChange={(e) => setEmail(e.target.value)} />
        <button type="submit">Add</button>
      </form>

      <h2>Users</h2>
      {users.map((user) => (
        <p key={user._id}>{user.name} - {user.email}</p>
      ))}
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: after clicking Add the new user appears in the list immediately without reloading the page.
```

### Q.102 — Perform Update using UI.

Step 1: add the PUT route in the backend (after the POST route).

SERVER/server.js (add this route)

// UPDATE a user

app.put("/users/:id", async (req, res) => {

const user = await User.findByIdAndUpdate(

req.params.id,

req.body,

{ new: true }

);

res.json(user);

});

Step 2: in the React page, add an Edit button against each user. It fills the form and the form then sends a PUT request. The complete page is given in Q.104.

CLIENT/src/App.jsx (edit/update part)

const [id, setId] = useState("");      // id of the user being edited

function editUser(user) {              // called by the Edit button

setId(user._id);

setName(user.name);

setEmail(user.email);

}

function saveUser(e) {

e.preventDefault();

if (id) {

axios.put(`http://localhost:5000/users/${id}`, { name: name, email: email })

.then(() => {

setId("");

setName("");

setEmail("");

fetchUsers();          // show updated records

});

}

}

// Button against each user:

<button onClick={() => editUser(user)}>Edit</button>

### Q.103 — Perform Delete using UI.

Step 1: add the DELETE route in the backend.

SERVER/server.js (add this route)

// DELETE a user

app.delete("/users/:id", async (req, res) => {

await User.findByIdAndDelete(req.params.id);

res.json({ message: "Deleted" });

});

Step 2: add a Delete button against each user in the React page. The complete page is given in Q.104.

CLIENT/src/App.jsx (delete part)

function deleteUser(userId) {

axios.delete(`http://localhost:5000/users/${userId}`)

.then(() => fetchUsers());     // refresh the list after delete

}

// Button against each user:

<button onClick={() => deleteUser(user._id)}>Delete</button>

### Q.104 — Integrate React frontend with Node and Express backend.

> Setup (once): create a folder MERN_USERS with two folders - SERVER (backend) and CLIENT (frontend). MongoDB must be running.

**Terminal / setup commands**

```bash
mkdir SERVER
cd SERVER
npm init -y
npm install express mongoose cors
cd ..
npm create vite@latest CLIENT
cd CLIENT
npm install
npm install axios
```

**File: `SERVER/server.js`**

```javascript
const express = require("express");
const mongoose = require("mongoose");
const cors = require("cors");

const app = express();
app.use(cors());
app.use(express.json());

mongoose.connect("mongodb://127.0.0.1:27017/trcac");

const User = mongoose.model("User", {
    name: String,
    email: String
});

// GET all users
app.get("/users", async (req, res) => {
    const users = await User.find();
    res.json(users);
});

// ADD user
app.post("/users", async (req, res) => {
    const user = new User(req.body);
    await user.save();
    res.json(user);
});

// UPDATE user
app.put("/users/:id", async (req, res) => {
    const user = await User.findByIdAndUpdate(
        req.params.id,
        req.body,
        { new: true }
    );
    res.json(user);
});

// DELETE user
app.delete("/users/:id", async (req, res) => {
    await User.findByIdAndDelete(req.params.id);
    res.json({ message: "Deleted" });
});

app.listen(5000, () => {
    console.log("Server running on http://localhost:5000");
});
```

**File: `CLIENT/src/App.jsx`**

```jsx
import { useEffect, useState } from "react";
import axios from "axios";

function App() {
    const [users, setUsers] = useState([]);
    const [name, setName] = useState("");
    const [email, setEmail] = useState("");
    const [id, setId] = useState("");

    function fetchUsers() {
        axios.get("http://localhost:5000/users")
            .then((res) => setUsers(res.data));
    }

    function saveUser(e) {
        e.preventDefault();

        if (id) {
            // UPDATE
            axios.put(`http://localhost:5000/users/${id}`, { name: name, email: email })
                .then(() => {
                    setId("");
                    setName("");
                    setEmail("");
                    fetchUsers();
                });
        } else {
            // INSERT
            axios.post("http://localhost:5000/users", { name: name, email: email })
                .then(() => {
                    setName("");
                    setEmail("");
                    fetchUsers();
                });
        }
    }

    function editUser(user) {
        setId(user._id);
        setName(user.name);
        setEmail(user.email);
    }

    function deleteUser(userId) {
        axios.delete(`http://localhost:5000/users/${userId}`)
            .then(() => fetchUsers());
    }

    useEffect(() => {
        fetchUsers();
    }, []);

    return (
        <div>
            <h1>User Management</h1>

            <form onSubmit={saveUser}>
                <input type="text" placeholder="Name" value={name}
                    onChange={(e) => setName(e.target.value)} />
                <input type="email" placeholder="Email" value={email}
                    onChange={(e) => setEmail(e.target.value)} />
                <button type="submit">{id ? "Update User" : "Add User"}</button>
            </form>

            <h2>Users</h2>
            <table border="1" cellPadding="8">
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Email</th>
                        <th>Action</th>
                    </tr>
                </thead>
                <tbody>
                    {users.map((user) => (
                        <tr key={user._id}>
                            <td>{user.name}</td>
                            <td>{user.email}</td>
                            <td>
                                <button onClick={() => editUser(user)}>Edit</button>
                                <button onClick={() => deleteUser(user._id)}>Delete</button>
                            </td>
                        </tr>
                    ))}
                </tbody>
            </table>
        </div>
    );
}

export default App;
```

**Expected output / result**

```text
Output: a form and a table of users. Edit loads the user into the form (button changes to Update User), Delete removes the user, and the table refreshes dynamically.
```

**Terminal / setup commands**

```bash
SERVER terminal:  node server.js
CLIENT terminal:  npm run dev

```

### Q.105 — Create an API to add users and an API to retrieve them from MongoDB. Display the users in a table in a React page.

> Setup (once): create a folder MERN_USERS with two folders - SERVER (backend) and CLIENT (frontend). MongoDB must be running.

**Terminal / setup commands**

```bash
mkdir SERVER
cd SERVER
npm init -y
npm install express mongoose cors
cd ..
npm create vite@latest CLIENT
cd CLIENT
npm install
npm install axios
```

**File: `SERVER/server.js`**

```javascript
const express = require("express");
const mongoose = require("mongoose");
const cors = require("cors");

const app = express();
app.use(cors());
app.use(express.json());

mongoose.connect("mongodb://127.0.0.1:27017/trcac");

const User = mongoose.model("User", {
  name: String,
  email: String
});

// GET all users
app.get("/users", async (req, res) => {
  const users = await User.find();
  res.json(users);
});

// ADD a user
app.post("/users", async (req, res) => {
  const user = new User(req.body);
  await user.save();
  res.json(user);
});

app.listen(5000, () => {
  console.log("Server running on http://localhost:5000");
});
```

**File: `CLIENT/src/App.jsx`**

```jsx
import { useEffect, useState } from "react";
import axios from "axios";

function App() {
  const [users, setUsers] = useState([]);
  const [name, setName] = useState("");
  const [email, setEmail] = useState("");

  function fetchUsers() {
    axios.get("http://localhost:5000/users")
      .then((res) => setUsers(res.data));
  }

  function addUser(e) {
    e.preventDefault();
    axios.post("http://localhost:5000/users", { name: name, email: email })
      .then(() => {
        setName("");
        setEmail("");
        fetchUsers();
      });
  }

  useEffect(() => {
    fetchUsers();
  }, []);

  return (
    <div>
      <h1>Add User</h1>
      <form onSubmit={addUser}>
        <input type="text" placeholder="Name" value={name}
          onChange={(e) => setName(e.target.value)} />
        <input type="email" placeholder="Email" value={email}
          onChange={(e) => setEmail(e.target.value)} />
        <button type="submit">Add</button>
      </form>

      <h2>User Table</h2>
      <table border="1" cellPadding="8">
        <thead>
          <tr>
            <th>Name</th>
            <th>Email</th>
          </tr>
        </thead>
        <tbody>
          {users.map((user) => (
            <tr key={user._id}>
              <td>{user.name}</td>
              <td>{user.email}</td>
            </tr>
          ))}
        </tbody>
      </table>
    </div>
  );
}

export default App;
```

**Expected output / result**

```text
Output: users are added using the form and displayed in a table.
```

**Terminal / setup commands**

```bash
SERVER terminal:  node server.js
CLIENT terminal:  npm run dev

```

### Q.106 — Implement an update operation: create a PUT API in Express to update a user's details in MongoDB and an edit form in React to update an existing record.

Backend (add to the server of Q.98):

SERVER/server.js (add this route)

// UPDATE a user

app.put("/users/:id", async (req, res) => {

const user = await User.findByIdAndUpdate(

req.params.id,

req.body,

{ new: true }

);

res.json(user);

});

Frontend: the Edit button fills the same form with the selected user's data and the form sends the PUT request. Full code is in Q.104.

CLIENT/src/App.jsx (edit/update part)

const [id, setId] = useState("");      // id of the user being edited

function editUser(user) {              // called by the Edit button

setId(user._id);

setName(user.name);

setEmail(user.email);

}

function saveUser(e) {

e.preventDefault();

if (id) {

axios.put(`http://localhost:5000/users/${id}`, { name: name, email: email })

.then(() => {

setId("");

setName("");

setEmail("");

fetchUsers();          // show updated records

});

}

}

// Button against each user:

<button onClick={() => editUser(user)}>Edit</button>

### Q.107 — Implement a delete operation: create a DELETE API in Express and a Delete button against each user in the React table to delete the selected record.

Backend (add to the server of Q.98):

SERVER/server.js (add this route)

// DELETE a user

app.delete("/users/:id", async (req, res) => {

await User.findByIdAndDelete(req.params.id);

res.json({ message: "Deleted" });

});

Frontend: a Delete button is placed in every table row. Full code is in Q.104.

CLIENT/src/App.jsx (delete part)

function deleteUser(userId) {

axios.delete(`http://localhost:5000/users/${userId}`)

.then(() => fetchUsers());     // refresh the list after delete

}

// Button against each user:

<button onClick={() => deleteUser(user._id)}>Delete</button>

### Q.108 — Create the APIs (GET, POST, PUT and DELETE) for a books collection using Express and MongoDB, and test all of them using Postman.

**Terminal / setup commands**

```bash
mkdir books-api
cd books-api
npm init -y
npm install express mongoose
```

**File: `server.js`**

```javascript
const express = require("express");
const mongoose = require("mongoose");

const app = express();
app.use(express.json());

mongoose.connect("mongodb://127.0.0.1:27017/trcac");

const Book = mongoose.model("Book", {
    title: String,
    author: String,
    price: Number
});

// GET - all books
app.get("/books", async (req, res) => {
    const books = await Book.find();
    res.json(books);
});

// POST - add a book
app.post("/books", async (req, res) => {
    const book = new Book(req.body);
    await book.save();
    res.json(book);
});

// PUT - update a book
app.put("/books/:id", async (req, res) => {
    const book = await Book.findByIdAndUpdate(req.params.id, req.body, { new: true });
    res.json(book);
});

// DELETE - delete a book
app.delete("/books/:id", async (req, res) => {
    await Book.findByIdAndDelete(req.params.id);
    res.json({ message: "Book deleted" });
});

app.listen(3000, () => {
    console.log("Server running on http://localhost:3000");
});
```

**Terminal / setup commands**

```bash
node server.js

Testing in Postman (Body -> raw -> JSON for POST and PUT):
Method
URL
Body (JSON)
GET
http://localhost:3000/books
-
POST
http://localhost:3000/books
{"title":"React Guide","author":"Mary","price":450}
PUT
http://localhost:3000/books/<id>
{"price":500}
DELETE
http://localhost:3000/books/<id>
-
```
