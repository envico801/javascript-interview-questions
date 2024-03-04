========== Question ==========  

### What is the easiest way to convert an array to an object  

========== Answer ==========  

You can convert an array to an object with the same data using spread(...)
operator.

```javascript
var fruits = ['banana', 'apple', 'orange', 'watermelon'];
var fruitsObject = { ...fruits };
console.log(fruitsObject); // {0: "banana", 1: "apple", 2: "orange", 3: "watermelon"}
```

========== Id ==========  
366

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#366-What-is-the-easiest-way-to-convert-an-arra

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
