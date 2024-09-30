========== Question ==========  

### How do you get the status of a checkbox  

========== Answer ==========  

You can apply the `checked` property on the selected checkbox in the DOM. If the value is `true` it means the checkbox is checked, otherwise it is unchecked. For example, the below HTML checkbox element can be access using javascript as below:

```html
<input type="checkbox" id="checkboxname" value="Agree" /> Agree the
conditions<br />
```

```javascript
console.log(document.getElementById(‘checkboxname’).checked); // true or false
```

========== Id ==========  
333

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#333-How-do-you-get-the-status-of-a-checkbox

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
