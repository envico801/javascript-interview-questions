==================== Question ====================  

### What is a constructor method  

==================== Answer ====================  

The constructor method is a special method for creating and initializing an
object created within a class. If you do not specify a constructor method, a
default constructor is used. The example usage of constructor would be as below,

```javascript
class Employee {
  constructor() {
    this.name = 'John';
  }
}
var employeeObject = new Employee();
console.log(employeeObject.name); // John
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#255-What-is-a-constructor-method

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
