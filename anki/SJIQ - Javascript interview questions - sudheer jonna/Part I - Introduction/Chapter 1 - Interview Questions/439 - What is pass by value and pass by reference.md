Q: What is pass by value and pass by reference?  
A: Pass-by-value creates a new space in memory and makes a copy of a value. Primitives such as string, number, boolean etc will actually create a new copy. Hence, updating one value doesn't impact the other value. i.e, The values are independent of each other.
```javascript
let a = 5;
let b = a;
b++;
console.log(a, b); //5, 6
```
In the above code snippet, the value of `a` is assigned to `b` and the variable `b` has been incremented. Since there is a new space created for variable `b`, any update on this variable doesn't impact the variable `a`.
Pass by reference doesn't create a new space in memory but the new variable adopts a memory address of an initial variable. Non-primitives such as objects, arrays and functions gets the reference of the initiable variable. i.e, updating one value will impact the other variable.
```javascript
let user1 = {
  name: "John",
  age: 27,
};
let user2 = user1;
user2.age = 30;
console.log(user1.age, user2.age); // 30, 30
```
In the above code snippet, updating the `age` property of one object will impact the other property due to the same reference.
<!--ID: 1693596682037-->

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