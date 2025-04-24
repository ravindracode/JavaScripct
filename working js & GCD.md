# JavaScript Execution Context 🚀


## Execution Context in JavaScript  

### What Happens When You Run a JavaScript Program?  

Yes, you are right! **An execution context is created**. Let's see how this execution context is created with the help of a JavaScript program.  

We have this code:  

```js
var n = 2;

function square(num) {
    return num * num;
}

var square2 = square(n);
var square4 = square(4);
````
# 🌍 Global Execution Context (GEC)

When you run this code, a **Global Execution Context (GEC)** is created.

## 🔥 Components of Execution Context

The **Execution Context** consists of two main components:

1. **Memory Component** 🧠  
2. **Code Component** 🎯  

This **Execution Context** is created in two phases:

1. **Creation Phase** (Memory Creation Phase)  
2. **Code Execution Phase**  

---

## 📌 Phase 1: Memory Creation Phase  

In this phase, JavaScript allocates memory to all **variables** and **functions** before executing the code.

- As soon as JS encounters `var n = 2;`, it **allocates memory** for `n` but assigns **undefined** initially.
- When it sees the function `square(num)`, it **allocates memory** and stores the **entire function code**.
- Similarly, `square2` and `square4` are allocated memory, but their values are **undefined** initially.

So, in memory:

| Variable / Function | Memory Allocated |
|---------------------|-----------------|
| `n` | `undefined` |
| `square` | `function code` |
| `square2` | `undefined` |
| `square4` | `undefined` |

---

## 📌 Phase 2: Code Execution Phase  

In this phase, JavaScript runs through the code line by line and executes it.

### 🔹 Line 1: `n = 2;`  
- The value of `n` is updated from **undefined** to `2`.  

### 🔹 Lines 2-5: Function declaration  
- No execution happens yet.

### 🔹 Line 6: `square2 = square(n);`  
- **Function Invocation:** A new **Execution Context** is created for `square(n)`.  

---

# 🎭 Function Execution Context  

When `square(n)` is invoked, a **new Execution Context** is created.  
Just like the global context, this function execution context also has two phases:

## 📌 Phase 1: Memory Creation  
- `num` is assigned **undefined**.  
- `ans` is assigned **undefined**.  

## 📌 Phase 2: Code Execution  
- The argument `n` (which is `2`) is passed to `num`.  
- `num * num` (`2 * 2 = 4`) is calculated and assigned to `ans`.  
- The function **returns** `4`, and the function execution context is **deleted**.  

The returned value `4` replaces `undefined` in `square2`.  

---

## 🔄 Next Function Execution  

The same process repeats for `square(4)` (Line 7):

1. A new execution context is created.  
2. `num = 4`, and `ans = 4 * 4 = 16`.  
3. The function **returns** `16`, and the execution context is deleted.  
4. `square4` is now `16`.  

---

## 🗑️ Deleting Execution Context  

After both function calls finish:

- The **Function Execution Contexts** are removed one by one.  
- Finally, **Global Execution Context** is removed when the program finishes.  

---

# 🌟 Recap  

### ✅ **Global Execution Context is created with two phases:**  
1. **Memory Allocation Phase** (variables → `undefined`, functions → full code).  
2. **Code Execution Phase** (assign values, invoke functions).  

### ✅ **Function Invocation creates a new Execution Context**  
- Function Execution Context also has two phases.  
- Arguments are passed, values are assigned, calculations happen.  
- Once execution is done, the function **returns the value**, and the function execution context **is deleted**.  

### ✅ **JavaScript manages multiple execution contexts using a Call Stack.**  

---

# 🚀 What's Next?  

But don’t you think that managing all these execution contexts is too much for the JavaScript engine? 🤔  
What if a function **calls another function** inside itself?  

This leads to something called the **Call Stack**—which we will explore in the next session! 🎥  

Stay tuned! 😃✨  

---

# 🎯 Summary Table  

| Concept | Description |
|---------|------------|
| **Execution Context** | The environment in which JavaScript code runs |
| **Global Execution Context (GEC)** | The default execution context created for JS programs |
| **Function Execution Context** | A new execution context created whenever a function is called |
| **Memory Phase** | Allocates memory for variables and functions before execution |
| **Code Execution Phase** | Assigns values and executes the code line by line |
| **Call Stack** | The mechanism JavaScript uses to manage multiple execution contexts |

---

## 📝 Notes  

- **Execution context** is the backbone of JavaScript execution.  
- Each function call creates a **new execution context**.  
- **Call stack** helps in managing function calls in the right order.  
- The **GEC** is created first and removed last.  

---
![Alt Text](images/image.PNG)

  
