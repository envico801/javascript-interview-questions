==================== Question ====================  

### How do you convert date to another timezone in javascript  

==================== Answer ====================  

You can use the toLocaleString() method to convert dates in one timezone to
another. For example, let's convert current date to British English timezone as
below,

```javascript
console.log(event.toLocaleString('en-GB', { timeZone: 'UTC' })); //29/06/2019, 09:56:00
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#171-How-do-you-convert-date-to-another-timezon

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
