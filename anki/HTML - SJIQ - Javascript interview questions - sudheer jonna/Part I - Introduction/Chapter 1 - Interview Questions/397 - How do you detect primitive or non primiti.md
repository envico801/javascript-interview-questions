==================== Question ====================  

### How do you detect primitive or non primitive value type  

==================== Answer ====================  

In JavaScript, primitive types include boolean, string, number, BigInt, null, Symbol and undefined. Whereas non-primitive types include the Objects. But you can easily identify them with the below function,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> myPrimitive = <span class="hljs-number">30</span>;
<span class="hljs-keyword">var</span> myNonPrimitive = {};
<span class="hljs-keyword">function</span> <span class="hljs-title function_">isPrimitive</span>(<span class="hljs-params">val</span>) {
  <span class="hljs-keyword">return</span> <span class="hljs-title class_">Object</span>(val) !== val;
}
<span class="hljs-title function_">isPrimitive</span>(myPrimitive);
<span class="hljs-title function_">isPrimitive</span>(myNonPrimitive);
</code></pre>
<!-- codeblock-end -->

If the value is a primitive data type, the Object constructor creates a new wrapper object for the value. But If the value is a non-primitive data type (an object), the Object constructor will give the same object.

==================== Id ====================  
397

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#397-How-do-you-detect-primitive-or-non-primiti

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
