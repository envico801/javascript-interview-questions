==================== Question ====================  

### How do you define multiple properties on an object  

==================== Answer ====================  

The `Object.defineProperties()` method is used to define new or modify existing properties directly on an object and returning the object. Let's define multiple properties on an empty object,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> newObject = {};
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">defineProperties</span>(newObject, {
  <span class="hljs-attr">newProperty1</span>: {
     <span class="hljs-attr">value</span>: <span class="hljs-string">'John'</span>,
     <span class="hljs-attr">writable</span>: <span class="hljs-literal">true</span>,
  },
  <span class="hljs-attr">newProperty2</span>: {},
});
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
264

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#264-How-do-you-define-multiple-properties-on-a

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
