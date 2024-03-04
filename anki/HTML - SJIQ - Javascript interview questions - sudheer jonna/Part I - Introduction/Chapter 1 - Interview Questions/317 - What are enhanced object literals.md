==================== Question ====================  

### What are enhanced object literals  

==================== Answer ====================  

Object literals make it easy to quickly create objects with properties inside the curly braces. For example, it provides shorter syntax for common object property definition as below.

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">//ES6</span>
<span class="hljs-keyword">var</span> x = <span class="hljs-number">10</span>,
  y = <span class="hljs-number">20</span>;
obj = { x, y };
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(obj); <span class="hljs-comment">// {x: 10, y:20}</span>
<span class="hljs-comment">//ES5</span>
<span class="hljs-keyword">var</span> x = <span class="hljs-number">10</span>,
  y = <span class="hljs-number">20</span>;
obj = { <span class="hljs-attr">x</span>: x, <span class="hljs-attr">y</span>: y };
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(obj); <span class="hljs-comment">// {x: 10, y:20}</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
317

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#317-What-are-enhanced-object-literals

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
