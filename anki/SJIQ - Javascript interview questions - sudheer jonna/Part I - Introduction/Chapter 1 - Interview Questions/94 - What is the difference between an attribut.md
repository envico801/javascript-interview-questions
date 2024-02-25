==================== Question ====================  

### What is the difference between an attribute and a property  

==================== Answer ====================  

Attributes are defined on the HTML markup whereas properties are defined on the
DOM. For example, the below HTML element has 2 attributes type and value,

```javascript
<input type="text" value="Name:">
```

You can retrieve the attribute value as below,

```javascript
const input = document.querySelector('input');
console.log(input.getAttribute('value')); // Good morning
console.log(input.value); // Good morning
```

And after you change the value of the text field to "Good evening", it becomes
like

```javascript
console.log(input.getAttribute('value')); // Good evening
console.log(input.value); // Good evening
```

==================== Id ====================  
94

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#94-What-is-the-difference-between-an-attribut

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
