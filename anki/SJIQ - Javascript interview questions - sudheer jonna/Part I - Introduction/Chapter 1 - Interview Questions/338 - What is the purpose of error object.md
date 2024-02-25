==================== Question ====================  

### What is the purpose of Error object  

==================== Answer ====================  

The Error constructor creates an error object and the instances of error objects
are thrown when runtime errors occur. The Error object can also be used as a
base object for user-defined exceptions. The syntax of error object would be as
below,

```javascript
new Error([message[, fileName[, lineNumber]]])
```

You can throw user defined exceptions or errors using Error object in
try...catch block as below,

```javascript
try {
  if (withdraw > balance)
    throw new Error("Oops! You don't have enough balance");
} catch (e) {
  console.log(e.name + ': ' + e.message);
}
```

==================== Id ====================  
338

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#338-What-is-the-purpose-of-error-object

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
