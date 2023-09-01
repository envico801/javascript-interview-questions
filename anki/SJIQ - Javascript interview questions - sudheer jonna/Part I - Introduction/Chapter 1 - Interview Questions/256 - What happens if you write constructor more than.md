Q: What happens if you write constructor more than once in a class  
A: The "constructor" in a class is a special method and it should be defined only once in a class. i.e, If you write a constructor method more than once in a class it will throw a `SyntaxError` error.
```javascript
class Employee {
constructor() {
this.name = "John";
}
constructor() {   //  Uncaught SyntaxError: A class may only have one constructor
this.age = 30;
}
}
var employeeObject = new Employee();
console.log(employeeObject.name);
```
<!--ID: 1693596699789-->

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