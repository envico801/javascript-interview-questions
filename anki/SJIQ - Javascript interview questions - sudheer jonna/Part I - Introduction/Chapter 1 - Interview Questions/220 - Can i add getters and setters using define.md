========== Question ==========  

### Can I add getters and setters using defineProperty method  

========== Answer ==========  

Yes, You can use the `Object.defineProperty()` method to add Getters and Setters. For example, the below counter object uses increment, decrement, add and subtract properties,

```javascript
var obj = { counter: 0 };

// Define getters
Object.defineProperty(obj, 'increment', {
    get: function () {
        this.counter++;
    },
});
Object.defineProperty(obj, 'decrement', {
    get: function () {
        this.counter--;
    },
});

// Define setters
Object.defineProperty(obj, 'add', {
    set: function (value) {
        this.counter += value;
    },
});
Object.defineProperty(obj, 'subtract', {
    set: function (value) {
        this.counter -= value;
    },
});

obj.add = 10;
obj.subtract = 5;
console.log(obj.increment); //6
console.log(obj.decrement); //5
```

========== Id ==========  
220

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#220-Can-i-add-getters-and-setters-using-define

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
