# JAVASCRIPT-HOISTING — Condensed Cheat Sheet**

## **Hoisting**
- JavaScript moves **declarations** (not values) to the top of their scope during compilation.
---
## **How It Works**
- **Compilation phase:** JS sets up memory for variables & functions.
- **Execution phase:** Code runs line‑by‑line and values get assigned.
---
## **Variables**
### **`var`**
- Declaration hoisted.
- Initialization **not** hoisted.
- If access before declaration → `undefined`.

### **`let` / `const`**
- Hoisted but **not initialized**.
- If access before declaration → **ReferenceError** (Temporal Dead Zone).
---
## **Functions**
### **Function Declarations**
- Entire function (name + body) is hoisted.
- Can be called before it appears.

### **Function Expressions / Arrow Functions**
- Behave like variables.
- Only the variable name is hoisted.
- Access before initialization → **TypeError**.
---
## **Summary Table**

| Feature | Hoisted? | Initialized? | Access Before Declaration |
|--------|----------|--------------|---------------------------|
| `var` | Yes | No | `undefined` |
| `let` | Yes | No | ReferenceError (TDZ) |
| `const` | Yes | No | ReferenceError (TDZ) |
| Function Declaration | Yes (full body) | Yes | Works |
| Function Expression (`var`) | Yes (name only) | No | TypeError |

---
## **Best Practices**
- Declare variables at the top of their scope.
- Prefer `let` and `const`.
- Define functions before using them.

