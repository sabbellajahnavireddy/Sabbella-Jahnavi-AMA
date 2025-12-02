# Questions
## 1. What is nested scope in JS?
- A function written inside another function can access variables of the outer function but the outer function cannot access variables of the inner function.
- Example:
```js
function outer() {
    let x = 10;   // Outer scope variable

    function inner() {
        let y = 20;   // Inner scope variable
        console.log(x); // INNER can access OUTER
        console.log(y); // INNER can access its own variable
    }

    inner();

    console.log(x); // OK
    console.log(y); // ❌ ERROR: y is not defined
}

outer();
```
## 2. What is the difference between undefined and null?
#### Undefined
- A variable exists but has no value assigned
- Example:
```js
let x;
console.log(x); // undefined
```
#### Null
- A variable has an empty value because you intentionally cleared it
- Example:
```js
let user = "Jahnavi";
user = null;        // we cleared the value intentionally
console.log(user);  // null
```

## 3. What are the types of Naming Convention?
1. camelCase

- First word lowercase
- Every next word starts with Capital letter
- Common in JavaScript variable & function names
- Example:
```js
firstName
totalAmount
getUserData()
```

2. PascalCase

- Every word starts with Capital letter
- Used for Classes, Constructors, Components
- Example:
```js
StudentData
UserProfile
CarModel
```

3. snake_case

- Words are separated by underscores
- Common in Python and file names
- Example:
```js
first_name
total_amount
user_profile
```

4. kebab-case

- Words separated by hyphens
- Mostly used in URLs, CSS class names, HTML file names
- Example:
```js
main-container
nav-bar
user-profile-card
```

## 4. What are tags in HTML?
- HTML tags are special keywords enclosed in angle brackets < > that tell the browser how to structure and display content on a webpage.
- Example:
```html
<p>This is a paragraph</p>
```

## 5. How to use async and await in JS and where the keyword async is written?
- **async**
- async is a keyword used before a function to make it return a Promise automatically.
- Example:
```js
async function myFunction() {
    return "Hello";
}
```
- myFunction() now returns a promise.

- **await**
- await is used inside an async function to wait for a Promise to finish.
- Example:
```js
let result = await somePromise;
```
- It pauses the function until the promise resolves.

## 6. What is semantic html tag?
- Semantic HTML tags are tags that clearly describe the meaning and purpose of the content they contain.
- Examples:
1. <header> → top section
2. <nav> → navigation links
3. <main> → main content area
4. <article> → independent piece of content
5. <section> → grouped content
6. <footer> → bottom section

- These tags tell both the browser and developers what the content represents.

## 7. Different ways to declare a function?

- There are three different ways we can define a function:
1. Function Declaration (Named Function)
- Most common, hoisted.
```js
function greet() {
    console.log("Hello");
}
```
2. Function Expression
- Function stored in a variable. Not hoisted.
```js
const greet = function() {
    console.log("Hello");
};
```
3. Arrow Function
- Shorter syntax, commonly used.
```js
const greet = () => {
    console.log("Hello");
};
```

## 8. What is the difference between an array and object?
| Feature                  | Array                                | Object                                   |
|-------------------------|----------------------------------------|-------------------------------------------|
| What it stores          | Ordered list of values                | Key–value pairs                           |
| How items are accessed  | By numeric index                      | By property name (keys)                   |
| Index starts at         | 0                                      | No index — uses keys                      |
| Best used for           | Lists, sequences, collections         | Structured data with named properties     |
| Syntax                  | []                                     | {}                                        |
| Example                 | [10, 20, 30]                          | { name: "Jahnavi", age: 22 }              |
| Access example          | numbers[0]                            | person.name                               |

## 9. What is the use of flexbox?
- Flexbox is a CSS layout system used to arrange items in a row or column, with flexible spacing, alignment, and sizing.
- Example:
```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

## 10. What is nested loop?
- A nested loop means a loop inside another loop.
- The inner loop runs completely for every single iteration of the outer loop.
- Example:
```js
for (let i = 1; i <= 3; i++) {
    for (let j = 1; j <= 2; j++) {
        console.log(i, j);
    }
}
```
## 11. What does Array.join() do in JS?
- join() converts all elements of an array into a single string, with a separator between them.
```js
array.join(separator)
```
## 12. What is the use of alter keyword in SQL?
- ALTER is used to change or modify an existing database table.
```sql
ALTER TABLE students
ADD age INT;
```