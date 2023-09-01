Q: What are default values in destructuring assignment  
A: A variable can be assigned a default value when the value unpacked from the array or object is undefined during destructuring assignment. It helps to avoid setting default values separately for each assignment. Let's take an example for both arrays and object use cases,  
**Arrays destructuring:**
```javascript
var x, y, z;
[x = 2, y = 4, z = 6] = [10];
console.log(x); // 10
console.log(y); // 4
console.log(z); // 6
```
**Objects destructuring:**
```javascript
var { x = 2, y = 4, z = 6 } = { x: 10 };
console.log(x); // 10
console.log(y); // 4
console.log(z); // 6
```
<!--ID: 1693596694023-->

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