========== Question ==========  

### How do you declare namespace  

========== Answer ==========  

Even though JavaScript lacks namespaces, we can use Objects , IIFE to create namespaces.

1. **Using Object Literal Notation:** Let's wrap variables and functions inside an Object literal which acts as a namespace. After that you can access them using object notation

```javascript
var namespaceOne = {
   function func1() {
       console.log("This is a first definition");
   }
}
var namespaceTwo = {
     function func1() {
         console.log("This is a second definition");
     }
 }
namespaceOne.func1(); // This is a first definition
namespaceTwo.func1(); // This is a second definition
```

1. **Using IIFE (Immediately invoked function expression):** The outer pair of parentheses of IIFE creates a local scope for all the code inside of it and makes the anonymous function a function expression. Due to that, you can create the same function in two different function expressions to act as a namespace.

```javascript
(function () {
    function fun1() {
        console.log('This is a first definition');
    }
    fun1();
})();

(function () {
    function fun1() {
        console.log('This is a second definition');
    }
    fun1();
})();
```

1. **Using a block and a let/const declaration:** In ECMAScript 6, you can simply use a block and a let declaration to restrict the scope of a variable to a block.

```javascript
{
    let myFunction = function fun1() {
        console.log('This is a first definition');
    };
    myFunction();
}
//myFunction(): ReferenceError: myFunction is not defined.

{
    let myFunction = function fun1() {
        console.log('This is a second definition');
    };
    myFunction();
}
//myFunction(): ReferenceError: myFunction is not defined.
```

========== Id ==========  
291

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#291-How-do-you-declare-namespace

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
