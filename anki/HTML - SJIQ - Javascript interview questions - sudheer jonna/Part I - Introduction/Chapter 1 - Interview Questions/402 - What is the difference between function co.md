==================== Question ====================  

### What is the difference between Function constructor and function declaration  

==================== Answer ====================  

The functions which are created with `Function constructor` do not create closures to their creation contexts but they are always created in the global scope. i.e, the function can access its own local variables and global scope variables only. Whereas function declarations can access outer function variables(closures) too.

Let's see this difference with an example,

**Function Constructor:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> a = <span class="hljs-number">100</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">createFunction</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">var</span> a = <span class="hljs-number">200</span>;
  <span class="hljs-keyword">return</span> <span class="hljs-keyword">new</span> <span class="hljs-title class_">Function</span>(<span class="hljs-string">'return a;'</span>);
}
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">createFunction</span>()()); <span class="hljs-comment">// 100</span>
</code></pre>
<!-- codeblock-end -->

**Function declaration:**

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> a = <span class="hljs-number">100</span>;
<span class="hljs-keyword">function</span> <span class="hljs-title function_">createFunction</span>(<span class="hljs-params"></span>) {
  <span class="hljs-keyword">var</span> a = <span class="hljs-number">200</span>;
  <span class="hljs-keyword">return</span> <span class="hljs-keyword">function</span> <span class="hljs-title function_">func</span>(<span class="hljs-params"></span>) {
     <span class="hljs-keyword">return</span> a;
  };
}
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">createFunction</span>()()); <span class="hljs-comment">// 200</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
402

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#402-What-is-the-difference-between-function-co

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
