==================== Question ====================  

### How do you define property on Object constructor  

==================== Answer ====================  

The Object.defineProperty() static method is used to define a new property directly on an object, or modify an existing property on an object, and returns the object. Let's see an example to know how to define property,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> newObject = {};
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">defineProperty</span>(newObject, <span class="hljs-string">'newProperty'</span>, {
  <span class="hljs-attr">value</span>: <span class="hljs-number">100</span>,
  <span class="hljs-attr">writable</span>: <span class="hljs-literal">false</span>,
});
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(newObject.<span class="hljs-property">newProperty</span>); <span class="hljs-comment">// 100</span>
newObject.<span class="hljs-property">newProperty</span> = <span class="hljs-number">200</span>; <span class="hljs-comment">// It throws an error in strict mode due to writable setting</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
217

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#217-How-do-you-define-property-on-object-const

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
