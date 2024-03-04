==================== Question ====================  

### Can I add getters and setters using defineProperty method  

==================== Answer ====================  

Yes, You can use the `Object.defineProperty()` method to add Getters and Setters. For example, the below counter object uses increment, decrement, add and subtract properties,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> obj = { <span class="hljs-attr">counter</span>: <span class="hljs-number">0</span> };
<span class="hljs-comment">// Define getters</span>
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">defineProperty</span>(obj, <span class="hljs-string">'increment'</span>, {
  <span class="hljs-attr">get</span>: <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">this</span>.<span class="hljs-property">counter</span>++;
  },
});
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">defineProperty</span>(obj, <span class="hljs-string">'decrement'</span>, {
  <span class="hljs-attr">get</span>: <span class="hljs-keyword">function</span> (<span class="hljs-params"></span>) {
     <span class="hljs-variable language_">this</span>.<span class="hljs-property">counter</span>--;
  },
});
<span class="hljs-comment">// Define setters</span>
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">defineProperty</span>(obj, <span class="hljs-string">'add'</span>, {
  <span class="hljs-attr">set</span>: <span class="hljs-keyword">function</span> (<span class="hljs-params">value</span>) {
     <span class="hljs-variable language_">this</span>.<span class="hljs-property">counter</span> += value;
  },
});
<span class="hljs-title class_">Object</span>.<span class="hljs-title function_">defineProperty</span>(obj, <span class="hljs-string">'subtract'</span>, {
  <span class="hljs-attr">set</span>: <span class="hljs-keyword">function</span> (<span class="hljs-params">value</span>) {
     <span class="hljs-variable language_">this</span>.<span class="hljs-property">counter</span> -= value;
  },
});
obj.<span class="hljs-property">add</span> = <span class="hljs-number">10</span>;
obj.<span class="hljs-property">subtract</span> = <span class="hljs-number">5</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(obj.<span class="hljs-property">increment</span>); <span class="hljs-comment">//6</span>
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(obj.<span class="hljs-property">decrement</span>); <span class="hljs-comment">//5</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
220

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#220-Can-i-add-getters-and-setters-using-define

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
