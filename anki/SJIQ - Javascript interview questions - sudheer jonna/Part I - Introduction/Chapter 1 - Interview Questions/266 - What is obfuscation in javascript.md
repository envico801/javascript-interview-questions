==================== Question ====================  

### What Is Obfuscation in javascript  

==================== Answer ====================  

Obfuscation is the deliberate act of creating obfuscated javascript code(i.e,
source or machine code) that is difficult for humans to understand. It is
something similar to encryption, but a machine can understand the code and
execute it.  
Let's see the below function before Obfuscation,

```javascript
function greeting() {
  console.log('Hello, welcome to JS world');
}
```

And after the code Obfuscation, it would be appeared as below,

```javascript
eval(
  (function (p, a, c, k, e, d) {
    e = function (c) {
      return c;
    };
    if (!''.replace(/^/, String)) {
      while (c--) {
        d[c] = k[c] || c;
      }
      k = [
        function (e) {
          return d[e];
        },
      ];
      e = function () {
        return '\\w+';
      };
      c = 1;
    }
    while (c--) {
      if (k[c]) {
        p = p.replace(new RegExp('\\b' + e(c) + '\\b', 'g'), k[c]);
      }
    }
    return p;
  })(
    "2 1(){0.3('4, 7 6 5 8')}",
    9,
    9,
    'console|greeting|function|log|Hello|JS|to|welcome|world'.split('|'),
    0,
    {},
  ),
);
```

==================== Id ====================  
266

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#266-What-is-obfuscation-in-javascript

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
