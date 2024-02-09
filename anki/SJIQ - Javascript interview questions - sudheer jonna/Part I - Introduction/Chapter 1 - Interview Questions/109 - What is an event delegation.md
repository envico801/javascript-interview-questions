==================== Question ====================  

### What is an event delegation  

==================== Answer ====================  

Event delegation is a technique for listening to events where you delegate a
parent element as the listener for all of the events that happen inside it.  
For example, if you wanted to detect field changes in inside a specific form,
you can use event delegation technique,

```javascript
var form = document.querySelector('#registration-form');
// Listen for changes to fields inside the form
form.addEventListener(
  'input',
  function (event) {
    // Log the field that was changed
    console.log(event.target);
  },
  false,
);
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#109-What-is-an-event-delegation

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
