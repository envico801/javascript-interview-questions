========== Question ==========  

### How do you print numbers with commas as thousand separators  

========== Answer ==========  

You can use the `Number.prototype.toLocaleString()` method which returns a
string with a language-sensitive representation such as thousand
separator,currency etc of this number.

```javascript
function convertToThousandFormat(x) {
  return x.toLocaleString(); // 12,345.679
}
console.log(convertToThousandFormat(12345.6789));
```

========== Id ==========  
288

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#288-How-do-you-print-numbers-with-commas-as-th

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
