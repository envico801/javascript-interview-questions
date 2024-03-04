==================== Question ====================  

### What are javascript accessors  

==================== Answer ====================  

ECMAScript 5 introduced javascript object accessors or computed properties through getters and setters. Getters uses the `get` keyword whereas Setters uses the `set` keyword.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> user = {
  <span class="hljs-attr">firstName</span>: <span class="hljs-string">'John'</span>,
  <span class="hljs-attr">lastName</span>: <span class="hljs-string">'Abraham'</span>,
  <span class="hljs-attr">language</span>: <span class="hljs-string">'en'</span>,
  <span class="hljs-keyword">get</span> <span class="hljs-title function_">lang</span>() {
     <span class="hljs-keyword">return</span> <span class="hljs-variable language_">this</span>.<span class="hljs-property">language</span>;
  },
  <span class="hljs-keyword">set</span> <span class="hljs-title function_">lang</span>(<span class="hljs-params">lang</span>) {
     <span class="hljs-variable language_">this</span>.<span class="hljs-property">language</span> = lang;
  },
};
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(user.<span class="hljs-property">lang</span>); <span class="hljs-comment">// getter access lang as en</span>
user.<span class="hljs-property">lang</span> = <span class="hljs-string">'fr'</span>;
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(user.<span class="hljs-property">lang</span>); <span class="hljs-comment">// setter used to set lang as fr</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
216

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#216-What-are-javascript-accessors

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
