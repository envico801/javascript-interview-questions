========== Question ==========  

### What is a proxy object  

========== Answer ==========  

The Proxy object is used to define custom behavior for fundamental operations
such as property lookup, assignment, enumeration, function invocation, etc. The
syntax would be as follows,

```javascript
var p = new Proxy(target, handler);
```

Let's take an example of proxy object,

```javascript
var handler = {
  get: function (obj, prop) {
     return prop in obj ? obj[prop] : 100;
  },
};
var p = new Proxy({}, handler);
p.a = 10;
p.b = null;
console.log(p.a, p.b); // 10, null
console.log('c' in p, p.c); // false, 100
```

In the above code, it uses `get` handler which define the behavior of the proxy
when an operation is performed on it

========== Id ==========  
194

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#194-What-is-a-proxy-object

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
