========== Question ==========  

### What is collation  

========== Answer ==========  

Collation is used for sorting a set of strings and searching within a set of strings. It is parameterized by locale and aware of Unicode. Let's take comparison and sorting features,

1. **Comparison:**

```javascript
var list = ['ä', 'a', 'z']; // In German,  "ä" sorts with "a" Whereas in Swedish, "ä" sorts after "z"
var l10nDE = new Intl.Collator('de');
var l10nSV = new Intl.Collator('sv');
console.log(l10nDE.compare('ä', 'z') === -1); // true
console.log(l10nSV.compare('ä', 'z') === +1); // true
```

1. **Sorting:**

```javascript
var list = ['ä', 'a', 'z']; // In German,  "ä" sorts with "a" Whereas in Swedish, "ä" sorts after "z"
var l10nDE = new Intl.Collator('de');
var l10nSV = new Intl.Collator('sv');
console.log(list.sort(l10nDE.compare)); // [ "a", "ä", "z" ]
console.log(list.sort(l10nSV.compare)); // [ "a", "z", "ä" ]
```

========== Id ==========  
322

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#322-What-is-collation

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
