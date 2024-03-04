==================== Question ====================  

### How do you prevent an object to extend  

==================== Answer ====================  

The `Object.preventExtensions()` method is used to prevent new properties from ever being added to an object. In other words, it prevents future extensions to the object. Let's see the usage of this property,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> newObject = {};
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">preventExtensions</span>(newObject); <span class="hljs-comment">// NOT extendable</span>
<span class="hljs-keyword">try</span> {
  <span class="hljs-title class_">Object</span>.<span class="hljs-title function_">defineProperty</span>(newObject, <span class="hljs-string">'newProperty'</span>, {
     <span class="hljs-comment">// Adding new property</span>
     <span class="hljs-attr">value</span>: <span class="hljs-number">100</span>,
  });
} <span class="hljs-keyword">catch</span> (e) {
  <span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(e); <span class="hljs-comment">// TypeError: Cannot define property newProperty, object is not extensible</span>
}
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
262

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#262-How-do-you-prevent-an-object-to-extend

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
