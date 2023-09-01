Q: What is ArrayBuffer  
A: An ArrayBuffer object is used to represent a generic, fixed-length raw binary data buffer. You can create it as below,
```javascript
let buffer = new ArrayBuffer(16); // create a buffer of length 16
alert(buffer.byteLength); // 16
```
To manipulate an ArrayBuffer, we need to use a “view” object.
```javascript
//Create a DataView referring to the buffer
let view = new DataView(buffer);
```
<!--ID: 1693596692074-->

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