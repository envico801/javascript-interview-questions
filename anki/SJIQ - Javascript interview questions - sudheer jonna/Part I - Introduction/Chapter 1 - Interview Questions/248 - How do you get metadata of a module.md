==================== Question ====================  

### How do you get metadata of a module  

==================== Answer ====================  

You can use the `import.meta` object which is a meta-property exposing
context-specific meta data to a JavaScript module. It contains information about
the current module, such as the module's URL. In browsers, you might get
different meta data than NodeJS.

```javascript
<script type='module' src='welcome-module.js'></script>;
console.log(import.meta); // { url: "file:///home/user/welcome-module.js" }
```

==================== Id ====================  
248

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#248-How-do-you-get-metadata-of-a-module

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
