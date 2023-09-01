Q: What are typed arrays  
A: Typed arrays are array-like objects from ECMAScript 6 API for handling binary data. JavaScript provides 8 Typed array types,
1. Int8Array: An array of 8-bit signed integers
2. Int16Array: An array of 16-bit signed integers
3. Int32Array: An array of 32-bit signed integers
4. Uint8Array: An array of 8-bit unsigned integers
5. Uint16Array: An array of 16-bit unsigned integers
6. Uint32Array: An array of 32-bit unsigned integers
7. Float32Array: An array of 32-bit floating point numbers
8. Float64Array: An array of 64-bit floating point numbers
   For example, you can create an array of 8-bit signed integers as below
```javascript
const a = new Int8Array();
// You can pre-allocate n bytes
const bytes = 1024;
const a = new Int8Array(bytes);
```
<!--ID: 1693596693610-->

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