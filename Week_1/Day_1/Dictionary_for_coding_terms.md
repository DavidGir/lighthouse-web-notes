### Callback Function
**Definition**: A function you give to another function to be run later. Used often in JavaScript to handle things like events or asynchronous operations.

**Code Snippet**:
```javascript
function greet(name, callback) {
  console.log(`Hello, ${name}`);
  callback();
}

greet('John', function() {
  console.log('Callback executed.');
});
```

### Refactor
**Definition**: The art of changing code without messing with its behavior. Great for making code more efficient, readable, or understandable.

**Code Snippet**:
```javascript
// Before Refactoring
function add(x, y) { return x + y; }
function sub(x, y) { return x - y; }

// After Refactoring
const add = (x, y) => x + y;
const sub = (x, y) => x - y;
```

### Interpolation
**Definition**: Putting variables right inside your strings to make them more dynamic. You usually do this with special syntax like `${variable}` in JavaScript.

**Code Snippet**:
```javascript
const name = 'John';
console.log(`Hello, ${name}`);
```

### Function Definition vs Function Call
**Definition**: A function definition lays out the blueprint: what the function needs (parameters) and what it does. A function call is like putting that blueprint to work by giving it actual values.

**Code Snippet**:
```javascript
// Definition
function greet(name) {
  console.log(`Hello, ${name}`);
}

// Call
greet('Jane');
```

### String Literal
**Definition**: It's just a string, but we call it a "literal" to specify that it's a fixed value and not a variable. Wrap it in quotes and you're good to go.

**Code Snippet**:
```javascript
const greeting = 'Hello, World!';
```

### Expression
**Definition**: A snippet of code that calculates a value. Could be as simple as 1+1 or as complex as a function that returns the square root of pi.

**Code Snippet**:
```javascript
const result = 1 + 1; // Simple expression
```

### String Template
**Definition**: Think of it as a fancier string. You wrap it in backticks and can drop in variables or even whole expressions using `${}`.

**Code Snippet**:
```javascript
const age = 30;
console.log(`I am ${age} years old.`);
```

### Promises
**Definition**: A way to handle things that might not happen immediately. It promises to return a value at some point in the future, letting you plan what to do if it works out or if it doesn't.

**Code Snippet**:
```javascript
const fetchData = new Promise((resolve, reject) => {
  // Simulate data fetch
  setTimeout(() => resolve('Data fetched'), 2000);
});

fetchData.then(data => console.log(data));
```

### Self-Documenting Code
**Definition**: Writing code so clear that anyone can understand what it's doing without needing a ton of comments.

**Code Snippet**:
```javascript
// Clear variable name
const daysInWeek = 7;
```

### Parameter
**Definition**: It's the variable listed inside the parentheses in the function definition. When you call the function, you replace this with an actual value, letting the function do something specific with it.

**Code Snippet**:
```javascript
function greet(name) {
  console.log(`Hello, ${name}`);
}

greet('Alice');
```

### Asynchronous Code or Operations
**Definition**: Code that allows you to start a task, move on to another one, and then come back to the initial task once it's completed. It helps to prevent blocking, or holding up, the rest of your application.

**Code Snippet**:
```javascript
setTimeout(() => {
  console.log('This happens later');
}, 2000);

console.log('This happens first');
```

