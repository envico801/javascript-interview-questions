==================== Question ====================  

### What happens if you write constructor more than once in a class  

==================== Answer ====================  

The "constructor" in a class is a special method and it should be defined only
once in a class. i.e, If you write a constructor method more than once in a
class it will throw a `SyntaxError` error.

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

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#256-What-happens-if-you-write-constructor-more

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
