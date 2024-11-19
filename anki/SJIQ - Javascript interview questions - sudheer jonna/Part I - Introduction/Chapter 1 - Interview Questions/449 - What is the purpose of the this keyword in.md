========== Question ==========  

### What is the purpose of the this keyword in JavaScript?  

========== Answer ==========  

-   The `this` keyword in JavaScript is a special variable that is used within a function to refer to the object on which the function is invoked. The value of this depends on how the function is called. It allows functions to access and interact with the object they are bound to.

-   The this keyword in JavaScript is a reference to the object that owns or invokes the current function. Its value is determined by the calling context.

    **Example 1: this in a Global Context**

```javascript
console.log(this);
```

-   In a global context, this refers to the global object (e.g., window in a browser).

**Example 2: this in a Function**

```javascript
function displayThis() {
    console.log(this);
}

displayThis();
```

-   In a regular function, this refers to the global object.

**Example 3: this in a Method**

```javascript
const person = {
    name: 'John',
    greet: function () {
        console.log('Hello, ' + this.name);
    },
};

person.greet();
```

-   In a method, this refers to the object that owns the method (person in the case).

**Example 4: this in an Event Handler**

```javascript
document.getElementById('myButton').addEventListener('click', function () {
    console.log(this);
});
```

-   In an event handler, this refers to the element that triggered the event (the button in this case).

========== Id ==========  
449

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#449-What-is-the-purpose-of-the-this-keyword-in

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
