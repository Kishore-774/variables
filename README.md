# JavaScript Scope

## 📌 Project Description

This project demonstrates **JavaScript scope** using:

* `var`
* `let`
* `const`
* Global Scope
* Block Scope
* Function Scope

The output can be viewed in the browser's **Console**.

---

## 📂 Project Structure

```text
JavaScript-Scope/
│
├── index.html
└── README.md
```

---

## 💻 Concepts Used

### 1. Global Scope

Variables declared outside a block or function can be accessed from different parts of the script.

```javascript
var Var = "outside the block";
let Let = "outside the block";
const Const = "outside the block";

console.log(Var);
console.log(Let);
console.log(Const);
```

---

### 2. Block Scope

```javascript
{
    var var1 = "inside the block";
    let let1 = "inside the block";
    const const1 = "inside the block";
}
```

* `var` is **not block-scoped**, so it can be accessed outside the block.
* `let` is **block-scoped**.
* `const` is **block-scoped**.

Example:

```javascript
console.log(var1); // Works

console.log(let1); // Error
console.log(const1); // Error
```

---

### 3. Function Scope

Variables declared inside a function cannot be accessed outside that function.

```javascript
function scope() {
    let functionscope = "function Scope";
}

scope();

console.log(functionscope); // Error
```

The variable `functionscope` exists only inside the `scope()` function.

---

## 🖥️ Expected Console Output

```text
outside the block
outside the block
outside the block

inside the block
inside the block
inside the block

inside the block

ReferenceError: functionscope is not defined
```

---

## ⚠️ Important Note

Your code contains this:

```javascript
function scope() {
    let functionscope = "function Scope";
}

functionscope();
```

This will cause an error because `functionscope` is a variable, not a function.

The correct code to call the function is:

```javascript
scope();
```

After that:

```javascript
console.log(functionscope);
```

will produce a `ReferenceError` because `functionscope` is declared inside the function and cannot be accessed outside it.

---

## 🚀 How to Run

1. Save the file as `index.html`.
2. Open the file in a web browser.
3. Right-click on the page.
4. Select **Inspect**.
5. Open the **Console** tab.
6. View the JavaScript output.

---

## 📚 What I Learned

* The difference between `var`, `let`, and `const`.
* Global scope in JavaScript.
* Block scope in JavaScript.
* Function scope in JavaScript.
* Why variables inside functions cannot be accessed outside the function.
* How to use the browser console to check JavaScript output.

---

## 👨‍💻 Author

**Ashok**

Learning JavaScript and Web Development 🚀
