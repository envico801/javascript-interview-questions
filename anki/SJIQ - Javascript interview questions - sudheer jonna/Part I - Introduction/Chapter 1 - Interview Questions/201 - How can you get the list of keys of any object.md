Q: How can you get the list of keys of any object  
A: You can use the `Object.keys()` method which is used to return an array of a given object's own property names, in the same order as we get with a normal loop. For example, you can get the keys of a user object,
```javascript
const user = {
  name: "John",
  gender: "male",
  age: 40,
};
console.log(Object.keys(user)); //['name', 'gender', 'age']
```
<!--ID: 1693596705004-->

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