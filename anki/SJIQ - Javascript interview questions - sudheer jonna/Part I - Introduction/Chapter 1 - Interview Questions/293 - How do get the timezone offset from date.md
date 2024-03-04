========== Question ==========  

### How do get the timezone offset from date  

========== Answer ==========  

You can use the `getTimezoneOffset` method of the date object. This method
returns the time zone difference, in minutes, from current locale (host system
settings) to UTC

```javascript
var offset = new Date().getTimezoneOffset();
console.log(offset); // -480
```

========== Id ==========  
293

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#293-How-do-get-the-timezone-offset-from-date

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
