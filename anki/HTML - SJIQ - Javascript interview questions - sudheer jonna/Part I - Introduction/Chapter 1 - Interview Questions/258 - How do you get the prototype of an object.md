==================== Question ====================  

### How do you get the prototype of an object  

==================== Answer ====================  

You can use the `Object.getPrototypeOf(obj)` method to return the prototype of the specified object. i.e. The value of the internal `prototype` property. If there are no inherited properties then `null` value is returned.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">const</span> newPrototype = {};
<span class="hljs-keyword">const</span> newObject = <span class="hljs-title class_">Object</span>.<span class="hljs-title function_">create</span>(newPrototype);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">getPrototypeOf</span>(newObject) === newPrototype); <span class="hljs-comment">// true</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
258

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#258-How-do-you-get-the-prototype-of-an-object

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
