# Cookbook: JavaScript

- [Basics](https://androcado.github.io/)
- [Functions](https://androcado.github.io/functions)



## **1. Variables and Constants**
```javascript
let x = 10;         // Mutable variable
const y = 20;       // Immutable variable
var z = 30;         // Legacy syntax (global or function-scoped)
```

---

## **2. Data Types**
### **Primitive Types**
```javascript
let str = "Hello";   // String
let num = 42;        // Number
let bool = true;     // Boolean
let undef;           // Undefined
let nul = null;      // Null
let sym = Symbol();  // Unique symbol
```

### **Objects**
```javascript
let obj = { name: "John", age: 30 };  // Object
let arr = [1, 2, 3];                 // Array
```

---

## **3. Operators**
### **Arithmetic Operators**
```javascript
x + y;   // Addition
x - y;   // Subtraction
x * y;   // Multiplication
x / y;   // Division
x % y;   // Modulo
x ** y;  // Exponentiation
```

### **Comparison Operators**
```javascript
x === y;  // Strict equality (type and value)
x == y;   // Loose equality (value only)
x !== y;  // Strict inequality
x > y;    // Greater than
x < y;    // Less than
```

### **Logical Operators**
```javascript
x && y;   // AND
x || y;   // OR
!x;       // NOT
```

---

## **4. Functions**
### **Regular Function**
```javascript
function add(a, b) {
  return a + b;
}
```

### **Arrow Function**
```javascript
const add = (a, b) => a + b;
```

### **Anonymous Function**
```javascript
setTimeout(function() {
  console.log("Hello!");
}, 1000);
```

---

## **5. Control Structures**
### **if / else**
```javascript
if (x > 10) {
  console.log("x is greater than 10");
} else {
  console.log("x is 10 or less");
}
```

### **Switch**
```javascript
switch (x) {
  case 1:
    console.log("One");
    break;
  case 2:
    console.log("Two");
    break;
  default:
    console.log("Other number");
}
```

### **Loops**
```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);  // Incrementing loop
}

while (x > 0) {
  x--;             // Decrementing loop
}

do {
  x--;             // Execute at least once
} while (x > 0);
```

---

## **6. Arrays**
### **Creation**
```javascript
let arr = [1, 2, 3];
```

### **Methods**
```javascript
arr.push(4);       // Add to the end
arr.pop();         // Remove from the end
arr.shift();       // Remove the first element
arr.unshift(0);    // Add to the beginning
arr.slice(1, 3);   // Extract a portion
arr.splice(1, 2);  // Add/remove elements
arr.map(x => x * 2); // Transform elements
arr.filter(x => x > 1); // Filter elements
arr.reduce((acc, val) => acc + val, 0); // Reduce to a single value
```

---

## **7. Objects**
### **Creation**
```javascript
let person = {
  name: "John",
  age: 30,
  greet: function() {
    console.log("Hello!");
  }
};
```

### **Access**
```javascript
person.name;   // Access property
person["age"]; // Alternative access
```

### **Modification**
```javascript
person.job = "Developer"; // Add a property
delete person.age;        // Remove a property
```

---

## **8. Classes**
```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
  greet() {
    console.log(`Hello, my name is ${this.name}`);
  }
}
let john = new Person("John", 30);
john.greet();
```

---

## **9. Modules**
### **Export**
```javascript
export const x = 10;
export default function() {
  console.log("Default export");
}
```

### **Import**
```javascript
import { x } from './module';
import myFunction from './module';
```

---

## **10. Asynchronous Programming**
### **Promise**
```javascript
let promise = new Promise((resolve, reject) => {
  resolve("Success!");
});
promise.then(result => console.log(result));
```

### **Async / Await**
```javascript
async function fetchData() {
  let response = await fetch("https://api.example.com/data");
  let data = await response.json();
  console.log(data);
}
fetchData();
```

---

## **11. Error Handling**
```javascript
try {
  throw new Error("Something went wrong!");
} catch (err) {
  console.log(err.message);
} finally {
  console.log("Done");
}
```

---

## **12. DOM Manipulation**
```javascript
document.getElementById("id");        // Select element by ID
document.querySelector(".class");    // Select element by CSS selector
document.createElement("div");       // Create a new element
element.textContent = "Hello!";      // Set text content
element.appendChild(newElement);     // Add a child element
```

---

## **13. Event Handling**
```javascript
element.addEventListener("click", () => {
  console.log("Clicked!");
});
```

---

## **14. Window - Global object in browser environments**
```javascript

console.log(window.document); // Access the DOM
console.log(window.location.href); // Get the URL
console.log(window.navigator.userAgent); // Get browser details
console.log(window.history.length); // Number of entries in the session history
console.log(window.screen.width); // Screen width

console.log(window.innerWidth);  // Width of the content area
console.log(window.innerHeight); // Height of the content area

console.log(window.outerWidth);  // Width including browser decorations
console.log(window.outerHeight); // Height including browser decorations

console.log(window.screenX); // Horizontal position
console.log(window.screenY); // Vertical position

console.log(window.scrollX); // Horizontal scroll offset
console.log(window.scrollY); // Vertical scroll offset


console.log(window.performance.now()); // High-resolution timestamp

setTimeout(() => console.log('Hello'), 1000); // Execute after 1 second

setInterval(() => console.log('Tick'), 1000); // Execute every 1 second


const timer = setTimeout(() => {}, 5000);
clearTimeout(timer); // Cancel timeout




window.alert('Hello, world!');

const isConfirmed = window.confirm('Are you sure?');

const name = window.prompt('What is your name?');

const newWindow = window.open('https://example.com', '_blank');

newWindow.close();













window.onload = () => console.log('Page loaded!');
window.onresize = () => console.log('Window resized!');


window.onscroll = () => console.log('User scrolled!');



window.onerror = (message, source, lineno, colno, error) => {
  console.error(`Error: ${message} at ${source}:${lineno}:${colno}`);
};













window.localStorage.setItem('key', 'value');
console.log(window.localStorage.getItem('key'));


window.sessionStorage.setItem('key', 'value');
console.log(window.sessionStorage.getItem('key'));



console.log(window.indexedDB); // Access the IndexedDB API







```
