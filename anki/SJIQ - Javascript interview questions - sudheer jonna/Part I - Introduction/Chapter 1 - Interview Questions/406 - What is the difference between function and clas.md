Q: What is the difference between function and class declarations  
A: The main difference between function declarations and class declarations is `hoisting`. The function declarations are hoisted but not class declarations.  
**Classes:**
```javascript
const user = new User(); // ReferenceError
class User {}
```
**Constructor Function:**
```javascript
const user = new User(); // No error
function User() {}
```
<!--ID: 1693596685267-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript #Interview

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store