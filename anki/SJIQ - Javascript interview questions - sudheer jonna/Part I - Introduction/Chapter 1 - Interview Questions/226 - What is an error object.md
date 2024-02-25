==================== Question ====================  

### What is an error object  

==================== Answer ====================  

An error object is a built in error object that provides error information when
an error occurs. It has two properties: name and message. For example, the below
function logs error details,

```javascript
try {
  greeting('Welcome');
} catch (err) {
  console.log(err.name + '<br>' + err.message);
}
```

==================== Id ====================  
226

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#226-What-is-an-error-object

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
