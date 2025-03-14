# **How JavaScript Works & Execution Context 🔥**  
**Source:** [Namaste JavaScript Ep.1 - YouTube](https://www.youtube.com/watch?v=ZvbzSrg0afE)  

## **Introduction**  
JavaScript is widely used for web development, but have you ever wondered how it works internally?  
- How is JavaScript code executed?  
- Is JavaScript **synchronous** or **asynchronous**?  
- Is JavaScript **single-threaded** or **multi-threaded**?  

In this documentation, we will break down these concepts in a clear and understandable way.  

---

## **What is an Execution Context?**  
Everything in JavaScript happens inside an **Execution Context**.  
Think of it as a **container or a big box** where JavaScript code is executed.  

An execution context consists of **two main components:**  

### 1️⃣ **Memory Component (Variable Environment)**  
- Stores all **variables and functions** as **key-value pairs**.  
- Example:  

  ```js
  var a = 10; 

### **Memory Component (Variable Environment)**
- Here, the variable `a` is stored with the value `10`.  
- Functions are also stored in this memory section.  
- Another term for the **Memory Component** is **Variable Environment**.  

---

### **2️⃣ Code Component (Thread of Execution)**
- Executes JavaScript code **line by line**.  
- Once a line is executed, the next line is picked up for execution.  
- This **Code Component** is also known as the **Thread of Execution**.  

---

### **Understanding JavaScript's Nature**
#### ✅ **Synchronous & Single-Threaded**
- JavaScript can execute **only one command at a time**.  
- The execution happens **sequentially**, meaning the next line executes **only after** the current line finishes.  

#### Example:  

```js
console.log("Hello");
console.log("World");

 ---
### ❓ **Common Confusion: What About Asynchronous JavaScript?**  
Many developers are familiar with **AJAX** (Asynchronous JavaScript and XML), which involves **asynchronous execution**.  

This topic will be covered in detail in later sections, but for now, just remember:  

- JavaScript **by default** is **synchronous and single-threaded**.  
- Asynchronous operations like **AJAX calls, Promises, and `setTimeout`** are handled differently.  

---

### 🔥 **Recap**  

✅ **JavaScript execution happens inside an Execution Context.**  
✅ **Execution Context has two parts:**  
   - **Memory Component (Variable Environment)** – Stores **variables** and **functions**.  
   - **Code Component (Thread of Execution)** – Executes the code **line by line**.  

✅ **JavaScript is a synchronous and single-threaded language.**  

