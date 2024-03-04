==================== Question ====================  

### What happens If I pass string type for getPrototype method  

==================== Answer ====================  

In ES5, it will throw a TypeError exception if the obj parameter isn't an object. Whereas in ES2015, the parameter will be coerced to an `Object`.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">// ES5</span>
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">getPrototypeOf</span>(<span class="hljs-string">'James'</span>); <span class="hljs-comment">// TypeError: "James" is not an object</span>
<span class="hljs-comment">// ES2015</span>
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">getPrototypeOf</span>(<span class="hljs-string">'James'</span>); <span class="hljs-comment">// String.prototype</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
259

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#259-What-happens-if-i-pass-string-type-for-get

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
