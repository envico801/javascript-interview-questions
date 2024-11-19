========== Question ==========  

### What are default parameters  

========== Answer ==========  

In ES5, we need to depend on logical OR operators to handle default values of function parameters. Whereas in ES6, Default function parameters feature allows parameters to be initialized with default values if no value or undefined is passed. Let's compare the behavior with an examples,

```javascript
//ES5
var calculateArea = function (height, width) {
    height = height || 50;
    width = width || 60;

    return width * height;
};
console.log(calculateArea()); //300
```

The default parameters makes the initialization more simpler,

```javascript
//ES6
var calculateArea = function (height = 50, width = 60) {
    return width * height;
};

console.log(calculateArea()); //300
```

========== Id ==========  
308

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#308-What-are-default-parameters

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
