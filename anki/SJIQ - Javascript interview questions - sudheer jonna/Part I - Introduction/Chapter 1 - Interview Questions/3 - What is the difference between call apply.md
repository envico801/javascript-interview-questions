========== Question ==========  

### What is the difference between Call, Apply and Bind  

========== Answer ==========  

The difference between Call, Apply and Bind can be explained with below examples,

**Call:** The call() method invokes a function with a given `this` value and arguments provided one by one

```javascript
var employee1 = { firstName: 'John', lastName: 'Rodson' };
var employee2 = { firstName: 'Jimmy', lastName: 'Baily' };
function invite(greeting1, greeting2) {
    console.log(
        greeting1 +
            ' ' +
            this.firstName +
            ' ' +
            this.lastName +
            ', ' +
            greeting2,
    );
}
invite.call(employee1, 'Hello', 'How are you?'); // Hello John Rodson, How are you?
invite.call(employee2, 'Hello', 'How are you?'); // Hello Jimmy Baily, How are you?
```

**Apply:** Invokes the function with a given `this` value and allows you to pass in arguments as an array

```javascript
var employee1 = { firstName: 'John', lastName: 'Rodson' };
var employee2 = { firstName: 'Jimmy', lastName: 'Baily' };
function invite(greeting1, greeting2) {
    console.log(
        greeting1 +
            ' ' +
            this.firstName +
            ' ' +
            this.lastName +
            ', ' +
            greeting2,
    );
}
invite.apply(employee1, ['Hello', 'How are you?']); // Hello John Rodson, How are you?
invite.apply(employee2, ['Hello', 'How are you?']); // Hello Jimmy Baily, How are you?
```

**Bind:** returns a new function, allowing you to pass any number of arguments

```javascript
var employee1 = { firstName: 'John', lastName: 'Rodson' };
var employee2 = { firstName: 'Jimmy', lastName: 'Baily' };
function invite(greeting1, greeting2) {
    console.log(
        greeting1 +
            ' ' +
            this.firstName +
            ' ' +
            this.lastName +
            ', ' +
            greeting2,
    );
}
var inviteEmployee1 = invite.bind(employee1);
var inviteEmployee2 = invite.bind(employee2);
inviteEmployee1('Hello', 'How are you?'); // Hello John Rodson, How are you?
inviteEmployee2('Hello', 'How are you?'); // Hello Jimmy Baily, How are you?
```

Call and Apply are pretty much interchangeable. Both execute the current function immediately. You need to decide whether it’s easier to send in an array or a comma separated list of arguments. You can remember by treating Call is for **comma** (separated list) and Apply is for **Array**.

Bind creates a new function that will have `this` set to the first parameter passed to bind().

========== Id ==========  
3

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#3-What-is-the-difference-between-call-apply

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
