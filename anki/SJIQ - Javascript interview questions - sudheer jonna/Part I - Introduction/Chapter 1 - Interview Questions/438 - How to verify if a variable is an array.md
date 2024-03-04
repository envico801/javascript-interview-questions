========== Question ==========  

### How to verify if a variable is an array?  

========== Answer ==========  

It is possible to check if a variable is an array instance using 3 different
ways,

1. Array.isArray() method:

    The `Array.isArray(value)` utility function is used to determine whether
    value is an array or not. This function returns a true boolean value if the
    variable is an array and a false value if it is not.

    ```javascript
    const numbers = [1, 2, 3];
    const user = { name: 'John' };
    Array.isArray(numbers); // true
    Array.isArray(user); //false
    ```

2. instanceof operator:

    The instanceof operator is used to check the type of an array at run time. It
    returns true if the type of a variable is an Array other false for other
    type.

    ```javascript
    const numbers = [1, 2, 3];
    const user = { name: 'John' };
    console.log(numbers instanceof Array); // true
    console.log(user instanceof Array); // false
    ```

3. Checking constructor type:

    The constructor property of the variable is used to determine whether the
    variable Array type or not.

    ```javascript
    const numbers = [1, 2, 3];
    const user = { name: 'John' };
    console.log(numbers.constructor === Array); // true
    console.log(user.constructor === Array); // false
    ```

========== Id ==========  
438

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#438-How-to-verify-if-a-variable-is-an-array

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
