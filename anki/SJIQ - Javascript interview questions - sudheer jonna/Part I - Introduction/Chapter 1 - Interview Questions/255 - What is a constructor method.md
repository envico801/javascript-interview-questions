Q: What is a constructor method  
A: The constructor method is a special method for creating and initializing an object created within a class. If you do not specify a constructor method, a default constructor is used. The example usage of constructor would be as below,
```javascript
class Employee {
  constructor() {
    this.name = "John";
  }
}
var employeeObject = new Employee();
console.log(employeeObject.name); // John
```
<!--ID: 1693596699888-->

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