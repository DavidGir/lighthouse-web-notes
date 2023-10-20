### Day 2 Bootcamp Dictionary
---
### JavaScript Basics

#### Incremental Development
**What Is It?**: The practice of building your code piece by piece, testing each part as you go.  
**Example**: When creating a calculator app, you might first implement the addition feature, test it, then move on to subtraction, and so on.

```javascript
// First, we add two numbers
function add(a, b) {
  return a + b;
}

// Test the function
console.log(add(2, 3)); // Output: 5
```

#### Mock
**What Is It?**: Creating a fake or stand-in piece of code to simulate something real, like a database or API call.  
**Example**:

```javascript
// Mocking a database call
function getUserFromDatabase() {
  return { name: 'John', age: 28 };
}

// Using the mock
const user = getUserFromDatabase();
console.log(user.name); // Output: John
```

#### Recursion
**What Is It?**: A function calling itself to solve a bigger problem by breaking it into smaller problems.  
**Example**:

```javascript
// Calculating factorial recursively
function factorial(n) {
  if (n === 0) return 1;
  return n * factorial(n - 1);
}

console.log(factorial(5)); // Output: 120
```

#### Edge Case
**What Is It?**: A rare or extreme use case that might not be immediately obvious but needs to be accounted for.  
**Example**: When sorting an array of numbers, an edge case might be an array with only one element.

```javascript
// Handling an edge case in sorting
function sortArray(arr) {
  if (arr.length <= 1) return arr;
  // Sorting logic here
}
```

#### Process.argv
**What Is It?**: In Node.js, this is how you access arguments passed in the command line.  
**Example**:

```javascript
// Accessing command line arguments in Node.js
console.log(process.argv);
```

#### Slice()
**What Is It?**: A method to extract part of an array or string without modifying the original.  
**Example**:

```javascript
const arr = [1, 2, 3, 4, 5];
const newArr = arr.slice(1, 4);
console.log(newArr); // Output: [2, 3, 4]
```

#### Conditionals: for-of, forEach, c-style for, for-in
**What Is It?**: Different ways to loop through arrays or objects to perform operations on each element.  
**Example**:

```javascript
// for-of loop
for (const element of [1, 2, 3]) {
  console.log(element);
}

// forEach loop
[1, 2, 3].forEach(element => console.log(element));

// c-style for loop
for (let i = 0; i < 3; i++) {
  console.log(i);
}

// for-in loop
for (const key in {a: 1, b: 2}) {
  console.log(key);
}
```

### Ternary Operator
**What Is It?**: It's a shortcut for making quick decisions in your code. Instead of writing a full-blown `if-else` statement, you can use the ternary operator to do the same thing but in a shorter way.

**How It Works**: You have a condition, something you want to do if that condition is true, and something you want to do if it's false. Put them all together like this: `condition ? doIfTrue : doIfFalse`.

**Example**: Let's say you want to know if a number is even or odd.

```javascript
const number = 5;
const isEvenOrOdd = (number % 2 === 0) ? 'Even' : 'Odd';
console.log(isEvenOrOdd);  // This will print 'Odd'
```

In this example, the `condition` is `(number % 2 === 0)`. If this condition is true, `isEvenOrOdd` will be `'Even'`. If it's false, `isEvenOrOdd` will be `'Odd'`.


#### Type Coercion
**What Is It?**: When JavaScript automatically converts one type of data to another.  
**Example**:

```javascript
const num = '5' + 10;  // Output will be the string '510', not the number 15.
```

#### Type Casting
**What Is It?**: Manually converting one type of data to another.  
**Example**:

```javascript
const num = Number('5') + 10;  // Output will be the number 15.
```

#### isNaN()
**What Is It?**: A function to check if a value is NaN (Not a Number).  
**Example**:

```javascript
console.log(isNaN(5));  // Output: false
console.log(isNaN('five'));  // Output: true
```

#### Return Statement
**What Is It?**: Used to send a value back from a function.  
**Example**:

```javascript
function add(a, b) {
  return a + b;
}
console.log(add(5, 10)); // Output: 15
```

#### Process.exit()
**What Is It?**: A way to stop a Node.js program.  
**Example**:

```javascript
if (someCondition) {
  process.exit();  // This will stop the program
}
```

---

## Git Commands

### `git init`
**Definition**: Initializes a new Git repository.
```bash
git init
```

### `git clone`
**Definition**: Copies an existing repository.
```bash
git clone <repository-url>
```

### `git add`
**Definition**: Stages changes for commit.
```bash
git add .
```

### `git commit`
**Definition**: Saves staged changes along with a message.
```bash
git commit -m "Commit message"
```

### `git push`
**Definition**: Uploads commits to a remote repository.
```bash
git push origin main
```

### `git pull`
**Definition**: Downloads changes from a remote repository.
```bash
git pull origin main
```

### `git log`
**Definition**: Displays the commit history.
```bash
git log
```

### `git remote -v`
**Definition**: Shows remote repositories.
```bash
git remote -v
```

### `git remote add origin`
**Definition**: Adds a remote repository.
```bash
git remote add origin <SSH>
```

### `git branch -M main`
**Definition**: Renames the branch to "main."
```bash
git branch -M main
```

### `git branch`
**Definition**: Lists local branches.
```bash
git branch
```

### `git checkout -b`
**Definition**: Creates and checks out a new branch.
```bash
git checkout -b <new-branch-name>
```

---

### Function Best Practices

#### 1. Precise Verb/Action-Based Names
**What Is It?**: Naming your functions in a way that clearly indicates what they do.  
**Example**: 

```javascript
// Good
function calculateTotalPrice() {}

// Bad
function doStuff() {}
```

#### 2. Use Camel Case
**What Is It?**: The practice of writing variable and function names with no spaces, and capitalizing each word after the first.  
**Example**: 

```javascript
// Good
let userAge = 28;

// Bad
let userage = 28;
```

#### 3. Proper Indentation
**What Is It?**: Using indentation to make the code within functions more readable.  
**Example**: 

```javascript
// Good
function add(a, b) {
  return a + b;
}

// Bad
function add(a,b){return a+b;}
```

#### 4. Single Responsibility Principle
**What Is It?**: Each function should focus on a single task. If a function is doing multiple things, consider breaking it into smaller functions.  
**Example**: 

```javascript
// Good
function printMessage() {
  console.log("Message printed.");
}

function calculateTotal() {
  return 5 + 10;
}

// Bad
function doEverything() {
  console.log("Message printed.");
  return 5 + 10;
}
```

#### 5. Use Parameters and Arguments
**What Is It?**: Functions should get their data from parameters rather than directly accessing variables. This makes the function more reusable and easier to test.  
**Example**: 

```javascript
// Good
function add(a, b) {
  return a + b;
}

// Bad
let a = 5;
let b = 10;

function add() {
  return a + b;
}
```
