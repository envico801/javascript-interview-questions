==================== Question ====================  

### How do you make first letter of the string in an uppercase  

==================== Answer ====================  

You can create a function which uses a chain of string methods such as charAt,
toUpperCase and slice methods to generate a string with the first letter in
uppercase.

```javascript
function capitalizeFirstLetter(string) {
  return string.charAt(0).toUpperCase() + string.slice(1);
}
```

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions -
sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS:
#Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#129-How-do-you-make-first-letter-of-the-string

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
