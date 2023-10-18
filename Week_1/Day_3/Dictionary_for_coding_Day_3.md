### Day 3 Bootcamp Dictionary
---

### JavaScript Basics

#### Primitive Types
- **What it does:** These are the basic, immutable types in JavaScript.
- **Why:** They are the building blocks of all JS operations.
- **How:** Declare using `const`, `let`, or `var`.
    - **Number:** Any numerical value, including floating point.
      ```javascript
      const age = 30;
      ```
    - **String:** Textual data enclosed in quotes.
      ```javascript
      const name = "John";
      ```
    - **Boolean:** True or false value.
      ```javascript
      const isActive = true;
      ```
    - **Undefined:** Declared but not yet assigned a value.
      ```javascript
      let x;
      ```
    - **Null:** Intentional absence of value.
      ```javascript
      const empty = null;
      ```
    - **Symbol:** Unique and immutable primitive.
      ```javascript
      const sym = Symbol("description");
      ```
    - **BigInt:** Larger integers than `Number` can hold.
      ```javascript
      const big = 1234567890123456789012345678901234567890n;
      ```

### Operators

#### Binary Operators
- **What it does:** Combines two values to produce a new one.
- **Why:** Fundamental for computations.
- **How:** Place the operator between two operands.
  - **Arithmetic Operators:** `+, -, *, /, %, **`
    ```javascript
    const sum = 3 + 4;  // 7
    ```
  - **Comparison Operators:** `==, ===, !=, !==, <, >, <=, >=`
    ```javascript
    const isEqual = (4 === 4);  // true
    ```
  - **Logical Operators:** `&&, ||`
    ```javascript
    const isTrue = (true && true);  // true
    ```

#### Unary Operators
- **What it does:** Transforms a single value.
- **Why:** Useful for negation, type conversion, etc.
- **How:** Place the operator before the operand.
  - **Common unary operators:** `+, -, ~, !, typeof, delete`
    ```javascript
    const isTrue = !false;  // true
    ```

#### Ternary Operator
- **What it does:** A shorthand for `if-else`.
- **Why:** Makes code more concise for simple conditionals.
- **How:** Use `?` and `:`.
  ```javascript
  const beverage = (age >= 21) ? "Beer" : "Juice";
  ```

### Objects and Data Structures

#### Methods
- **What it does:** Functions tied to an object.
- **Why:** Encapsulates behavior with data.
- **How:** Declare within an object or assign to a property.
  - **Built-in methods:** `.toString(), .join(), .pop(), .push(), .slice()`
    ```javascript
    const arr = [1, 2, 3];
    arr.push(4);  // [1, 2, 3, 4]
    ```
  - **Custom methods:**
    ```javascript
    const obj = {
      greet: function() {
        console.log("Hello");
      }
    };
    obj.greet();
    ```

#### Expressions
- **What it does:** Produces a value.
- **Why:** Fundamental to writing dynamic code.
- **How:** Combine variables, values, and operators.
```javascript
const sum = 5 + 3;  // 8
```

#### Evaluation of Expressions
- **What it does:** Computes the value of an expression.
- **Why:** Required for the JavaScript engine to execute code.
- **How:** Automatic during runtime; the result is stored in memory.
```javascript
const total = 4 + 5;  // "4 + 5" is evaluated to 9
```

#### Immutable Variable
- **What it does:** Defines a variable that can't be changed once set.
- **Why:** Useful for maintaining constants.
- **How:** Use the `const` keyword.
```javascript
const pi = 3.14159;
```

#### Objects
- **What it does:** Groups related data and functions.
- **Why:** Enables complex data structures and methods.
- **How:** Use curly braces `{}` to define an object literal.
```javascript
const person = {name: "Alice", age: 30};
```

#### Null vs Undefined
- **What it does:** Represents an absence or uninitialized value.
- **Why:** Useful for checks and initializations.
- **How:** Declare a variable without assigning it, or explicitly set it to `null`.
```javascript
let x;  // undefined
let y = null;  // null
```

#### Methods
- **What it does:** Functions that are properties of objects.
- **Why:** Encapsulates behavior with data.
- **How:** Assign a function to an object property.
```javascript
const obj = {
  greet: function() {
    console.log("Hello");
  }
};
obj.greet();  // Output: Hello
```

#### Accessing Object Values
- **What it does:** Retrieves the value stored in an object property.
- **Why:** Required for utilizing or manipulating object data.
- **How:** Use dot notation or square bracket notation.
```javascript
const person = {name: "Alice", age: 30};
console.log(person.name);  // Alice
console.log(person['age']);  // 30
```

#### `this` Keyword
- **What it does:** Refers to the object it belongs to.
- **Why:** Enables reusable and modular code.
- **How:** Use `this` within methods to refer to the object the method is called on.
```javascript
const car = {
  make: 'Toyota',
  model: 'Camry',
  describe: function() {
    return `This car is a ${this.make} ${this.model}.`;
  }
};
console.log(car.describe());  // Output: This car is a Toyota Camry.
```
