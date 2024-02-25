==================== Question ====================  

### Give an example usage of rangeOverflow property  

==================== Answer ====================  

If an element's value is greater than its max attribute then rangeOverflow
property returns true. For example, the below form submission throws an error if
the value is more than 100,

```html
<input id="age" type="number" max="100" />
<button onclick="myOverflowFunction()">OK</button>
```

```javascript
function myOverflowFunction() {
  if (document.getElementById('age').validity.rangeOverflow) {
    alert('The mentioned age is not allowed');
  }
}
```

==================== Id ====================  
277

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#277-Give-an-example-usage-of-rangeoverflow-pro

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
