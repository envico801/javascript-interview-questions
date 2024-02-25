==================== Question ====================  

### How do I modify the url without reloading the page  

==================== Answer ====================  

The `window.location.href` property will be helpful to modify the url but it
reloads the page. HTML5 introduced the `history.pushState()` and
`history.replaceState()` methods, which allow you to add and modify history
entries, respectively. For example, you can use pushState as below,

```javascript
window.history.pushState('page2', 'Title', '/page2.html');
```

==================== Id ====================  
284

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#284-How-do-i-modify-the-url-without-reloading

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
