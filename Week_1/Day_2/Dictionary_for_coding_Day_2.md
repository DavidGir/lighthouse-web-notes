### Day 2 Bootcamp Dictionary

#### Incremental Development
**Definition**: Building a project piece-by-piece, validating each piece before moving on to the next.

```javascript
// Step 1: Build and validate the function
function sayHello() {
  console.log("Hello");
}
sayHello();

// Step 2: Extend and validate
function sayHelloTo(name) {
  console.log(`Hello, ${name}`);
}
sayHelloTo("Alice");
```

#### Mock
**Definition**: A fake version of a system component used for testing.
```javascript
const mockDatabase = {
  getUser: () => ({ id: 1, name: 'Test' })
};
```

#### Recursion
**Definition**: A function that calls itself to solve a problem.
```javascript
function factorial(n) {
  if (n === 1) return 1;
  return n * factorial(n - 1);
}
```

#### Edge Case
**Definition**: An unusual or extreme use-case that you may not anticipate but should handle in your code.
```javascript
if(input === null || input === undefined) {
  console.log('This is an edge case.');
}
```

#### `process.argv`
**Definition**: In Node.js, this is an array that contains command-line arguments.
```javascript
// Run with: node script.js hello world
console.log(process.argv[2]); // Output: "hello"
console.log(process.argv[3]); // Output: "world"
```

#### Coding Thought Process
**Steps**:
1. **Hypothesis**: What do you expect to happen?
2. **Validation**: Test the hypothesis.
3. **Step-by-Step**: Break down the problem.

#### `slice()`
**Definition**: Returns a shallow copy of a portion of an array.
```javascript
const arr = [1, 2, 3, 4, 5];
const sliced = arr.slice(1, 3); // Output: [2, 3]
```

#### Conditionals
- **for...of**: Loops through values of an iterable.
```javascript
for (const val of [1, 2, 3]) {
  console.log(val);
}
```

- **forEach**: Executes a function for each item.
```javascript
[1, 2, 3].forEach(val => console.log(val));
```

- **C-style for**: Classic loop.
```javascript
for (let i = 0; i < 3; i++) {
  console.log(i);
}
```

- **for...in**: Loops through properties.
```javascript
const obj = { a: 1, b: 2 };
for (const key in obj) {
  console.log(key);
}
```

#### Type Coercion
**Definition**: Automatic conversion between data types.
```javascript
const result = '5' + 1;  // Output: "51"
```

#### Type Casting
**Definition**: Explicitly changing the data type.
```javascript
const str = "123";
const num = parseInt(str);  // Output: 123
```

#### `isNaN()`
**Definition**: Checks if a value is NaN.
```javascript
const result = isNaN("hello");  // Output: true
```

#### Return Statement
**Definition**: Sends a value back to where the function was called.
```javascript
function add(a, b) {
  return a + b;
}
```

#### `process.exit()`
**Definition**: Ends the process immediately.
```javascript
// Exit with status code 0 (success)
process.exit(0);
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
