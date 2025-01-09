# Cookbook: JavaScript

- [Basics](https://androcado.github.io/cookbook-javascript)
- [Window Properties](https://androcado.github.io/cookbook-javascript/global-variables)

# JavaScript CookBook

## **1. Variables**

| **Keyword**         | **Description**                                   |
|---------------------|---------------------------------------------------|
| `var`               | Function-scoped variable, can be reassigned.      |
| `let`               | Block-scoped variable, can be reassigned.         |
| `const`             | Block-scoped constant, cannot be reassigned.      |

### Examples:
```javascript
var x = 10;        // Function-scoped
let y = 20;        // Block-scoped
const z = 30;      // Constant
```

---

## **2. Data Types**

| **Type**            | **Description**                                   |
|---------------------|---------------------------------------------------|
| `String`           | Represents textual data.                           |
| `Number`           | Represents numerical data, including `NaN`.        |
| `Boolean`          | Represents true/false values.                      |
| `Undefined`        | Variable not assigned a value.                     |
| `Null`             | Represents an intentional absence of value.        |
| `Symbol`           | Unique, immutable values for object properties.    |
| `BigInt`           | Represents integers larger than `Number.MAX_SAFE_INTEGER`. |

### Examples:
```javascript
let str = "Hello";  // String
def num = 42;       // Number
let bool = true;     // Boolean
let undef;           // Undefined
let nul = null;      // Null
let sym = Symbol();  // Symbol
let big = 123n;      // BigInt
```

---

## **3. Operators**
### **Arithmetic Operators**

| **Operator**        | **Description**                                   |
|---------------------|---------------------------------------------------|
| `+`                 | Addition                                          |
| `-`                 | Subtraction                                       |
| `*`                 | Multiplication                                    |
| `/`                 | Division                                          |
| `%`                 | Modulo (remainder)                                |
| `**`                | Exponentiation                                    |

### **Comparison Operators**

| **Operator**        | **Description**                                   |
|---------------------|---------------------------------------------------|
| `==`                | Equal to (loose comparison).                      |
| `===`               | Equal to (strict comparison).                     |
| `!=`                | Not equal to (loose comparison).                  |
| `!==`               | Not equal to (strict comparison).                 |
| `>`                 | Greater than.                                     |
| `<`                 | Less than.                                        |
| `>=`                | Greater than or equal to.                         |
| `<=`                | Less than or equal to.                            |

### **Logical Operators**

| **Operator**        | **Description**                                   |
|---------------------|---------------------------------------------------|
| `&&`               | Logical AND.                                       |
| `||`               | Logical OR.                                        |
| `!`                | Logical NOT.                                       |

### Examples:
```javascript
console.log(5 > 3 && 10 > 5);  // true
console.log(5 > 3 || 10 < 5);  // true
console.log(!(5 > 3));         // false
```

---

## **4. Control Structures**

| **Structure**       | **Description**                                   |
|---------------------|---------------------------------------------------|
| `if` / `else`       | Conditional execution based on boolean expressions. |
| `switch`            | Executes code blocks based on matching cases.     |
| `for`               | Iterates over a block of code a number of times.  |
| `while`             | Loops while a condition is true.                  |
| `do...while`        | Executes a block of code once, then repeats while true. |

### Examples:
```javascript
if (x > 10) {
  console.log("Greater than 10");
} else {
  console.log("10 or less");
}

switch (x) {
  case 1:
    console.log("One");
    break;
  default:
    console.log("Other");
}

for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

---

## **5. Functions**

| **Type**            | **Description**                                   |
|---------------------|---------------------------------------------------|
| `function`          | Declares a named function.                        |
| Arrow Functions     | Shorter syntax for functions, no `this` context.  |

### Examples:
```javascript
function add(a, b) {
  return a + b;
}

const multiply = (a, b) => a * b;
```





---

## **6. Arrays**

| **Method**          | **Description**                                   |
|---------------------|---------------------------------------------------|
| `push`              | Adds an element to the end of the array.          |
| `pop`               | Removes the last element.                         |
| `shift`             | Removes the first element.                        |
| `unshift`           | Adds an element to the beginning of the array.    |
| `slice`             | Returns a shallow copy of a portion of an array.  |
| `splice`            | Adds/removes elements in an array.                |
| `map`               | Creates a new array with the results of calling a provided function on every element. |
| `filter`            | Creates a new array with elements that pass the test implemented by a provided function. |
| `reduce`            | Executes a reducer function on each element, resulting in a single output value. |

### Examples:
```javascript
let arr = [1, 2, 3];
arr.push(4);       // [1, 2, 3, 4]
arr.pop();         // [1, 2, 3]
arr.slice(1, 2);   // [2]

// Using map
let doubled = arr.map(x => x * 2);  // [2, 4, 6]

// Using filter
let filtered = arr.filter(x => x > 1);  // [2, 3]

// Using reduce
let sum = arr.reduce((acc, val) => acc + val, 0);  // 6
```

---

## **7. Objects**
### **Creation**

| **Method**          | **Description**                                   |
|---------------------|---------------------------------------------------|
| Object Literal      | Creates an object using curly braces `{}`.        |
| `Object.create()`   | Creates a new object with the specified prototype. |
| Constructor Function| Creates an object using a constructor function.   |
| `class`             | Creates objects using ES6 class syntax.           |

### Examples:
```javascript
// Object Literal
const obj = { name: "Alice", age: 25 };

// Object.create
const proto = { greet: function() { console.log("Hello"); } };
const newObj = Object.create(proto);

// Constructor Function
function Person(name, age) {
  this.name = name;
  this.age = age;
}
const person = new Person("Bob", 30);

// Using Class
class Animal {
  constructor(type) {
    this.type = type;
  }
}
const dog = new Animal("Dog");
```

---

### **Access**

| **Method**          | **Description**                                   |
|---------------------|---------------------------------------------------|
| Dot Notation        | Access properties using `.` syntax.               |
| Bracket Notation    | Access properties using `[]` syntax.              |
| Destructuring       | Extract values into variables.                    |

### Examples:
```javascript
const obj = { name: "Alice", age: 25 };

// Dot Notation
console.log(obj.name);  // "Alice"

// Bracket Notation
console.log(obj["age"]);  // 25

// Destructuring
const { name, age } = obj;
console.log(name, age);  // "Alice", 25
```

---

### **Modification**

| **Method**          | **Description**                                   |
|---------------------|---------------------------------------------------|
| Add Property        | Add a new property to an object.                  |
| Modify Property     | Change the value of an existing property.         |
| Delete Property     | Remove a property from an object.                 |

### Examples:
```javascript
const obj = { name: "Alice", age: 25 };

// Add Property
obj.job = "Developer";
console.log(obj);  // { name: "Alice", age: 25, job: "Developer" }

// Modify Property
obj.age = 26;
console.log(obj);  // { name: "Alice", age: 26, job: "Developer" }

// Delete Property
delete obj.job;
console.log(obj);  // { name: "Alice", age: 26 }
```

|---------------------|---------------------------------------------------|
| `Object.keys`       | Returns an array of an object's keys.             |
| `Object.values`     | Returns an array of an object's values.           |
| `Object.entries`    | Returns an array of key-value pairs.              |
| `Object.assign`     | Copies properties from one or more objects.       |

### Examples:
```javascript
const obj = { a: 1, b: 2 };
console.log(Object.keys(obj));   // ['a', 'b']
console.log(Object.assign({}, obj)); // { a: 1, b: 2 }
```

---



## **8. Classes**
### **Definition**

| **Component**       | **Description**                                   |
|---------------------|---------------------------------------------------|
| `class`             | Declares a new class.                             |
| Constructor         | A method to initialize the class with properties. |
| Methods             | Functions defined within a class.                 |

### Examples:
```javascript
// Define a class
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hello, my name is ${this.name}.`);
  }
}

// Create an instance
const john = new Person("John", 30);
john.greet();  // "Hello, my name is John."
```

---

### **Inheritance**

| **Component**       | **Description**                                   |
|---------------------|---------------------------------------------------|
| `extends`           | Creates a subclass that inherits properties and methods. |
| `super`             | Calls the parent class's constructor or methods. |

### Examples:
```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(`${this.name} makes a noise.`);
  }
}

class Dog extends Animal {
  constructor(name, breed) {
    super(name);  // Call parent constructor
    this.breed = breed;
  }

  speak() {
    console.log(`${this.name} barks.`);
  }
}

const rex = new Dog("Rex", "Golden Retriever");
rex.speak();  // "Rex barks."
```

---

### **Static Methods and Properties**

| **Component**       | **Description**                                   |
|---------------------|---------------------------------------------------|
| `static`            | Defines methods or properties that belong to the class, not instances. |

### Examples:
```javascript
class MathUtils {
  static add(a, b) {
    return a + b;
  }
}

console.log(MathUtils.add(2, 3));  // 5
```

|---------------------|---------------------------------------------------|
| `click`             | Triggered when an element is clicked.             |
| `mousemove`         | Triggered when the mouse is moved.                |
| `mousedown`         | Triggered when a mouse button is pressed.         |

### **Keyboard Events**
| **Event**           | **Description**                                   |
|---------------------|---------------------------------------------------|
| `keydown`           | Triggered when a key is pressed.                  |
| `keyup`             | Triggered when a key is released.                 |

### **Load and Transition Events**
| **Event**           | **Description**                                   |
|---------------------|---------------------------------------------------|
| `load`              | Triggered when the page or a resource loads.      |
| `transitionend`     | Triggered when a CSS transition finishes.         |

### Examples:
```javascript
window.addEventListener("click", () => console.log("Clicked"));
window.addEventListener("load", () => console.log("Page loaded"));
```

---

## **9. Modules**
### **Exporting Modules**

| **Keyword**         | **Description**                                   |
|---------------------|---------------------------------------------------|
| `export`            | Exports variables, functions, or classes from a module. |
| `export default`    | Exports a single default variable, function, or class. |

### Examples:
```javascript
// Named Exports
export const PI = 3.14;
export function add(a, b) {
  return a + b;
}

// Default Export
export default function subtract(a, b) {
  return a - b;
}
```

---

### **Importing Modules**

| **Keyword**         | **Description**                                   |
|---------------------|---------------------------------------------------|
| `import`            | Imports variables, functions, or classes from a module. |

### Examples:
```javascript
// Importing Named Exports
import { PI, add } from './math.js';
console.log(PI);  // 3.14
console.log(add(2, 3));  // 5

// Importing Default Export
import subtract from './math.js';
console.log(subtract(5, 3));  // 2
```

---

### **Dynamic Imports**

| **Keyword**         | **Description**                                   |
|---------------------|---------------------------------------------------|
| `import()`          | Dynamically loads a module at runtime.            |

### Examples:
```javascript
// Dynamic Import
import('./math.js').then(module => {
  console.log(module.add(2, 3));  // 5
});
```

---


---

## **10. Asynchronous Programming**
### **Promises**

| **Method**          | **Description**                                   |
|---------------------|---------------------------------------------------|
| `then`              | Executes a function when the promise is resolved. |
| `catch`             | Executes a function when the promise is rejected. |
| `finally`           | Executes a function after resolution or rejection. |

### Examples:
```javascript
const promise = new Promise((resolve, reject) => {
  setTimeout(() => resolve("Success!"), 1000);
});

promise
  .then(result => console.log(result))  // "Success!"
  .catch(error => console.error(error))
  .finally(() => console.log("Done"));
```

---

### **Async/Await**

| **Keyword**         | **Description**                                   |
|---------------------|---------------------------------------------------|
| `async`             | Declares an asynchronous function.                |
| `await`             | Waits for a promise to resolve or reject.         |

### Examples:
```javascript
async function fetchData() {
  try {
    const response = await fetch("https://api.example.com/data");
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error("Error fetching data", error);
  }
}

fetchData();
```

---

### **Callbacks**

| **Concept**         | **Description**                                   |
|---------------------|---------------------------------------------------|
| Callback Function   | A function passed as an argument to another function, executed later. |

### Examples:
```javascript
function fetchData(callback) {
  setTimeout(() => {
    const data = { name: "Alice", age: 30 };
    callback(data);
  }, 1000);
}

fetchData(data => console.log(data));  // { name: "Alice", age: 30 }
```

---

## **11. Error Handling**
### **try/catch/finally**

| **Block**           | **Description**                                   |
|---------------------|---------------------------------------------------|
| `try`               | Defines a block of code to test for errors.       |
| `catch`             | Handles errors that occur in the `try` block.     |
| `finally`           | Executes code after `try` and `catch`, regardless of the outcome. |

### Examples:
```javascript
try {
  const data = JSON.parse('{"name": "Alice"}');
  console.log(data.name); // "Alice"
} catch (error) {
  console.error("Parsing error", error);
} finally {
  console.log("Execution completed");
}
```

---

### **Throwing Errors**

| **Keyword**         | **Description**                                   |
|---------------------|---------------------------------------------------|
| `throw`             | Throws a custom error.                            |

### Examples:
```javascript
function checkAge(age) {
  if (age < 18) {
    throw new Error("Age must be at least 18.");
  }
  console.log("Access granted.");
}

try {
  checkAge(15);
} catch (error) {
  console.error(error.message); // "Age must be at least 18."
}
```

---


## **12. DOM Manipulation**
### **Selecting Elements**

| **Method**                         | **Description**                                    |
|------------------------------------|----------------------------------------------------|
| `document.getElementById()`        | Selects an element by its ID.                      |
| `document.querySelector()`         | Selects the first element matching a CSS selector. |
| `document.querySelectorAll()`      | Selects all elements matching a CSS selector.      |
| `document.getElementsByClassName()`| Selects elements by class name.                    |
| `document.getElementsByTagName()`  | Selects elements by tag name.                      |

### Examples:
```javascript
const element = document.getElementById("header");
const items = document.querySelectorAll(".list-item");
console.log(items[0]);
```

---

### **Modifying Elements**

| **Property/Method**                | **Description**                                    |
|------------------------------------|----------------------------------------------------|
| `textContent`                      | Sets or gets the text content of an element.       |
| `innerHTML`                        | Sets or gets the HTML content of an element.       |
| `style`                            | Modifies the inline styles of an element.          |
| `setAttribute()`                   | Sets an attribute on an element.                   |
| `removeAttribute()`                | Removes an attribute from an element.              |

### Examples:
```javascript
const element = document.getElementById("header");
element.textContent = "Welcome!"; // Updates text

const button = document.querySelector(".btn");
button.setAttribute("disabled", "true"); // Adds 'disabled' attribute
button.removeAttribute("disabled"); // Removes 'disabled' attribute
```

---

### **Creating and Appending Elements**

| **Method**                         | **Description**                                    |
|------------------------------------|----------------------------------------------------|
| `document.createElement()`         | Creates a new element.                             |
| `appendChild()`                    | Appends a child element.                           |
| `insertBefore()`                   | Inserts an element before another element.         |
| `removeChild()`                    | Removes a child element.                           |

### Examples:
```javascript
const newDiv = document.createElement("div");
newDiv.textContent = "Hello, World!";
document.body.appendChild(newDiv);

const parent = document.getElementById("list");
const newItem = document.createElement("li");
newItem.textContent = "New Item";
parent.insertBefore(newItem, parent.firstChild);
```

---

### **Event Listeners**

| **Method**                         | **Description**                                    |
|------------------------------------|----------------------------------------------------|
| `addEventListener()`               | Attaches an event handler to an element.           |
| `removeEventListener()`            | Removes an event handler from an element.          |

### Examples:
```javascript
const button = document.querySelector(".btn");

function handleClick() {
  console.log("Button clicked!");
}

button.addEventListener("click", handleClick);
button.removeEventListener("click", handleClick);
```

---


## **13. Event Handling**
### **Common Events**

| **Event**           | **Description**                                   |
|---------------------|---------------------------------------------------|
| `click`             | Triggered when an element is clicked.             |
| `dblclick`          | Triggered when an element is double-clicked.      |
| `mouseover`         | Triggered when the mouse pointer is over an element. |
| `mouseout`          | Triggered when the mouse pointer leaves an element. |
| `keydown`           | Triggered when a key is pressed.                  |
| `keyup`             | Triggered when a key is released.                 |
| `change`            | Triggered when the value of an input element changes. |
| `submit`            | Triggered when a form is submitted.               |

### Examples:
```javascript
const button = document.querySelector(".btn");

// Click event
button.addEventListener("click", () => {
  console.log("Button clicked!");
});

// Keydown event
document.addEventListener("keydown", (event) => {
  console.log(`Key pressed: ${event.key}`);
});
```

---

### **Event Propagation**

| **Phase**           | **Description**                                   |
|---------------------|---------------------------------------------------|
| Capturing Phase     | Events propagate from the root to the target element. |
| Target Phase        | The event reaches the target element.             |
| Bubbling Phase      | Events propagate back from the target to the root. |

### Examples:
```javascript
const parent = document.getElementById("parent");
const child = document.getElementById("child");

// Event capturing
parent.addEventListener(
  "click",
  () => console.log("Parent (capturing)"),
  true // Use capturing phase
);

// Event bubbling
child.addEventListener("click", () => console.log("Child (bubbling)"));
```

---

### **Event Delegation**

| **Concept**         | **Description**                                   |
|---------------------|---------------------------------------------------|
| Delegation          | Use a parent element to handle events for its children. |

### Examples:
```javascript
const list = document.getElementById("list");

list.addEventListener("click", (event) => {
  if (event.target.tagName === "LI") {
    console.log(`Clicked on item: ${event.target.textContent}`);
  }
});
```

---

### **Preventing Default Behavior**

| **Method**               | **Description**                                   |
|--------------------------|---------------------------------------------------|
| `event.preventDefault()` | Prevents the default action of an event.          |

### Examples:
```javascript
const link = document.querySelector("a");

link.addEventListener("click", (event) => {
  event.preventDefault();
  console.log("Link click prevented.");
});
```


## **14. Window Properties and Methods**
### **Window Properties**

| **Property**        | **Description**                                   |
|---------------------|---------------------------------------------------|
| `window`            | The global window object itself.                  |
| `innerHeight`       | Height of the viewport in pixels.                 |
| `innerWidth`        | Width of the viewport in pixels.                  |
| `outerHeight`       | Height of the window including browser chrome.    |
| `outerWidth`        | Width of the window including browser chrome.     |
| `screenX`           | Horizontal position of the window relative to the screen. |
| `screenY`           | Vertical position of the window relative to the screen.   |
| `location`          | Provides information about the URL of the window. |
| `history`           | Provides access to the browser's session history. |
| `navigator`         | Provides information about the browser and device.|
| `localStorage`      | Provides access to the browser's local storage.   |
| `sessionStorage`    | Provides access to the browser's session storage. |
| `performance`       | Provides performance-related information.         |
| `document`          | The DOM document object of the current page.      |

### Examples:
```javascript
console.log(window.innerHeight); // Logs the viewport height
console.log(window.location.href); // Logs the current URL
console.log(window.navigator.userAgent); // Logs browser details
```

---

### **Window Methods**

| **Method**          | **Description**                                   |
|---------------------|---------------------------------------------------|
| `alert()`           | Displays an alert dialog.                         |
| `confirm()`         | Displays a confirmation dialog.                   |
| `prompt()`          | Displays a dialog to accept user input.           |
| `open()`            | Opens a new browser tab or window.                |
| `close()`           | Closes the current window.                        |
| `focus()`           | Brings the window to the foreground.              |
| `blur()`            | Removes focus from the window.                    |
| `scrollTo()`        | Scrolls to a specified position in the window.    |
| `setTimeout()`      | Executes a function after a specified delay.      |
| `clearTimeout()`    | Cancels a timeout set with `setTimeout()`.        |
| `setInterval()`     | Executes a function at specified intervals.       |
| `clearInterval()`   | Cancels an interval set with `setInterval()`.     |
| `requestAnimationFrame()` | Requests a frame for performing animations. |
| `cancelAnimationFrame()` | Cancels an animation frame request.          |

### Examples:
```javascript
window.alert("Hello, World!");
const timer = setTimeout(() => console.log("Executed after 2 seconds"), 2000);
clearTimeout(timer); // Cancels the timeout
```

---

### **Navigator Properties**

| **Property**        | **Description**                                   |
|---------------------|---------------------------------------------------|
| `userAgent`         | Returns the user agent string for the browser.    |
| `platform`          | Provides information about the platform (OS).     |
| `language`          | Returns the browser's language setting.           |
| `onLine`            | Indicates if the browser is online.               |

### Examples:
```javascript
console.log(window.navigator.userAgent); // Logs browser's user agent
console.log(window.navigator.language); // Logs browser language
```

---

### **Location Object**

| **Property/Method** | **Description**                                   |
|---------------------|---------------------------------------------------|
| `href`              | Gets or sets the entire URL of the window.        |
| `reload()`          | Reloads the current document.                     |
| `replace()`         | Replaces the current document with a new one.     |
| `assign()`          | Loads a new document.                             |

### Examples:
```javascript
console.log(window.location.href); // Logs current URL
window.location.reload(); // Reloads the page
```

---

## **13. Event Handling**
### **Common Events**

| **Event**           | **Description**                                   |
|---------------------|---------------------------------------------------|
| `click`             | Triggered when an element is clicked.             |
| `dblclick`          | Triggered when an element is double-clicked.      |
| `mouseover`         | Triggered when the mouse pointer is over an element. |
| `mouseout`          | Triggered when the mouse pointer leaves an element. |
| `keydown`           | Triggered when a key is pressed.                  |
| `keyup`             | Triggered when a key is released.                 |
| `change`            | Triggered when the value of an input element changes. |
| `submit`            | Triggered when a form is submitted.               |

### Examples:
```javascript
const button = document.querySelector(".btn");

// Click event
button.addEventListener("click", () => {
  console.log("Button clicked!");
});

// Keydown event
document.addEventListener("keydown", (event) => {
  console.log(`Key pressed: ${event.key}`);
});
```

---

### **Event Propagation**

| **Phase**           | **Description**                                   |
|---------------------|---------------------------------------------------|
| Capturing Phase     | Events propagate from the root to the target element. |
| Target Phase        | The event reaches the target element.             |
| Bubbling Phase      | Events propagate back from the target to the root. |

### Examples:
```javascript
const parent = document.getElementById("parent");
const child = document.getElementById("child");

// Event capturing
parent.addEventListener(
  "click",
  () => console.log("Parent (capturing)"),
  true // Use capturing phase
);

// Event bubbling
child.addEventListener("click", () => console.log("Child (bubbling)"));
```

---

### **Event Delegation**

| **Concept**         | **Description**                                   |
|---------------------|---------------------------------------------------|
| Delegation          | Use a parent element to handle events for its children. |

### Examples:
```javascript
const list = document.getElementById("list");

list.addEventListener("click", (event) => {
  if (event.target.tagName === "LI") {
    console.log(`Clicked on item: ${event.target.textContent}`);
  }
});
```

---

### **Preventing Default Behavior**

| **Method**          | **Description**                                   |
|---------------------|---------------------------------------------------|
| `event.preventDefault()` | Prevents the default action of an event.     |

### Examples:
```javascript
const link = document.querySelector("a");

link.addEventListener("click", (event) => {
  event.preventDefault();
  console.log("Link click prevented.");
});
```


---


## **14. Window Properties and Methods**

### **Window Properties**

| **Property**        | **Description**                                   |
|---------------------|---------------------------------------------------|
| `window`            | The global window object itself.                  |
| `innerHeight`       | Height of the viewport in pixels.                 |
| `innerWidth`        | Width of the viewport in pixels.                  |
| `outerHeight`       | Height of the window including browser chrome.    |
| `outerWidth`        | Width of the window including browser chrome.     |
| `screenX`           | Horizontal position of the window relative to the screen. |
| `screenY`           | Vertical position of the window relative to the screen.   |
| `location`          | Provides information about the URL of the window. |
| `history`           | Provides access to the browser's session history. |
| `navigator`         | Provides information about the browser and device.|
| `localStorage`      | Provides access to the browser's local storage.   |
| `sessionStorage`    | Provides access to the browser's session storage. |
| `performance`       | Provides performance-related information.         |
| `document`          | The DOM document object of the current page.      |

### Examples:
```javascript
console.log(window); // Logs the global window object
console.log(window.innerHeight); // Logs the viewport height in pixels
console.log(window.outerWidth); // Logs the total width of the browser window
console.log(window.screenX); // Logs the horizontal screen position of the window
console.log(window.screenY); // Logs the vertical screen position of the window
console.log(window.location.href); // Logs the current URL of the page
console.log(window.history.length); // Logs the number of entries in the session history
console.log(window.navigator.userAgent); // Logs the browser's user agent string
console.log(window.localStorage); // Logs the local storage object
console.log(window.sessionStorage); // Logs the session storage object
console.log(window.performance.now()); // Logs a high-resolution timestamp
console.log(window.document.title); // Logs the title of the document
```

---

### **Window Methods**

| **Method**          | **Description**                                   |
|---------------------|---------------------------------------------------|
| `alert()`           | Displays an alert dialog.                         |
| `confirm()`         | Displays a confirmation dialog.                   |
| `prompt()`          | Displays a dialog to accept user input.           |
| `open()`            | Opens a new browser tab or window.                |
| `close()`           | Closes the current window.                        |
| `focus()`           | Brings the window to the foreground.              |
| `blur()`            | Removes focus from the window.                    |
| `scrollTo()`        | Scrolls to a specified position in the window.    |
| `setTimeout()`      | Executes a function after a specified delay.      |
| `clearTimeout()`    | Cancels a timeout set with `setTimeout()`.        |
| `setInterval()`     | Executes a function at specified intervals.       |
| `clearInterval()`   | Cancels an interval set with `setInterval()`.     |
| `requestAnimationFrame()` | Requests a frame for performing animations. |
| `cancelAnimationFrame()` | Cancels an animation frame request.          |

### Examples:
```javascript
// Alert dialog
window.alert("Hello, World!");

// Confirmation dialog
const isConfirmed = window.confirm("Are you sure?");
console.log(isConfirmed); // Logs true or false

// Prompt dialog
const userName = window.prompt("What is your name?");
console.log(userName); // Logs the entered name

// Open and close a window
const newWindow = window.open("https://example.com", "_blank");
newWindow.close(); // Closes the new window

// Scrolling
window.scrollTo(0, 100); // Scrolls to 100px from the top

// Timer methods
const timer = setTimeout(() => console.log("Executed after 2 seconds"), 2000);
clearTimeout(timer); // Cancels the timeout

const interval = setInterval(() => console.log("Interval log"), 1000);
clearInterval(interval); // Cancels the interval

// Request animation frame
const animationId = window.requestAnimationFrame(() => console.log("Frame rendered"));
window.cancelAnimationFrame(animationId); // Cancels the animation frame
```

---

### **Navigator Properties**

| **Property**        | **Description**                                   |
|---------------------|---------------------------------------------------|
| `userAgent`         | Returns the user agent string for the browser.    |
| `platform`          | Provides information about the platform (OS).     |
| `language`          | Returns the browser's language setting.           |
| `onLine`            | Indicates if the browser is online.               |

### Examples:
```javascript
console.log(window.navigator.userAgent); // Logs the browser's user agent string
console.log(window.navigator.platform); // Logs the platform (e.g., "Win32")
console.log(window.navigator.language); // Logs the browser's language (e.g., "en-US")
console.log(window.navigator.onLine); // Logs true if the browser is online
```

---

### **Location Object**

| **Property/Method** | **Description**                                   |
|---------------------|---------------------------------------------------|
| `href`              | Gets or sets the entire URL of the window.        |
| `reload()`          | Reloads the current document.                     |
| `replace()`         | Replaces the current document with a new one.     |
| `assign()`          | Loads a new document.                             |

### Examples:
```javascript
console.log(window.location.href); // Logs the current URL
window.location.reload(); // Reloads the current page
window.location.assign("https://example.com"); // Navigates to a new URL
window.location.replace("https://example.com"); // Replaces the current URL
```

---
