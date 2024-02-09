==================== Question ====================  

### How to convert string to title case with javascript  

==================== Answer ====================  

Title case means that the first letter of each word is capitalized. You can
convert a string to title case using the below function,

```javascript
function toTitleCase(str) {
  return str.replace(/\w\S*/g, function (txt) {
    return txt.charAt(0).toUpperCase() + txt.substring(1).toLowerCase();
  });
}
toTitleCase('good morning john'); // Good Morning John
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#182-How-to-convert-string-to-title-case-with-j

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
