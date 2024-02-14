==================== Question ====================  

### What is the difference between proto and prototype  

==================== Answer ====================  

The `__proto__` object is the actual object that is used in the lookup chain to
resolve methods, etc. Whereas `prototype` is the object that is used to build
`__proto__` when you create an object with new.

```javascript
new Employee().__proto__ === Employee.prototype;
new Employee().prototype === undefined;
```

There are few more differences,

| feature    | Prototype                                                    | proto                                                      |
| ---------- | ------------------------------------------------------------ | ---------------------------------------------------------- |
| Access     | All the function constructors have prototype properties.     | All the objects have \_\_proto\_\_ property                |
| Purpose    | Used to reduce memory wastage with a single copy of function | Used in lookup chain to resolve methods, constructors etc. |
| ECMAScript | Introduced in ES6                                            | Introduced in ES5                                          |
| Usage      | Frequently used                                              | Rarely used                                                |

==================== Id ====================  
176
<!--ID: 1707879834747-->

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#176-What-is-the-difference-between-proto-and-p

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
QUESTION STATUS: Safe to store
