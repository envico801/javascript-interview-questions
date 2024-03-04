========== Question ==========  

### How do you invoke javascript code in an iframe from parent page  

========== Answer ==========  

Initially iFrame needs to be accessed using either `document.getElementBy` or
`window.frames`. After that `contentWindow` property of iFrame gives the access
for targetFunction

```javascript
document.getElementById('targetFrame').contentWindow.targetFunction();
window.frames[0].frameElement.contentWindow.targetFunction(); // Accessing iframe this way may not work in latest versions chrome and firefox
```

========== Id ==========  
292

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#292-How-do-you-invoke-javascript-code-in-an-if

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
