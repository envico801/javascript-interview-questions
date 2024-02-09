==================== Question ====================  

### How do you detect a browser language preference  

==================== Answer ====================  

You can use navigator object to detect a browser language preference as below,

```javascript
var language =
  (navigator.languages && navigator.languages[0]) || // Chrome / Firefox
  navigator.language || // All browsers
  navigator.userLanguage; // IE <= 10
console.log(language);
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#181-How-do-you-detect-a-browser-language-prefe

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
