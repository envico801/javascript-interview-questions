==================== Question ====================  

### What are the different ways to make an object non-extensible  

==================== Answer ====================  

You can mark an object non-extensible in 3 ways,

1. Object.preventExtensions

2. Object.seal

3. Object.freeze

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> newObject = {};
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">preventExtensions</span>(newObject); <span class="hljs-comment">// Prevent objects are non-extensible</span>
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">isExtensible</span>(newObject); <span class="hljs-comment">// false</span>
<span class="hljs-keyword">var</span> sealedObject = <span class="hljs-title class_">Object</span>.<span class="hljs-title function_">seal</span>({}); <span class="hljs-comment">// Sealed objects are non-extensible</span>
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">isExtensible</span>(sealedObject); <span class="hljs-comment">// false</span>
<span class="hljs-keyword">var</span> frozenObject = <span class="hljs-title class_">Object</span>.<span class="hljs-title function_">freeze</span>({}); <span class="hljs-comment">// Frozen objects are non-extensible</span>
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">isExtensible</span>(frozenObject); <span class="hljs-comment">// false</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
263

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#263-What-are-the-different-ways-to-make-an-obj

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
