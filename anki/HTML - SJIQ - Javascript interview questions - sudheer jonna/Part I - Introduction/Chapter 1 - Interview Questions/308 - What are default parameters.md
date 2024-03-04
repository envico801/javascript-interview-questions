==================== Question ====================  

### What are default parameters  

==================== Answer ====================  

In ES5, we need to depend on logical OR operators to handle default values of function parameters. Whereas in ES6, Default function parameters feature allows parameters to be initialized with default values if no value or undefined is passed. Let's compare the behavior with an examples,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">//ES5</span>
<span class="hljs-keyword">var</span> calculateArea = <span class="hljs-keyword">function</span> (<span class="hljs-params">height, width</span>) {
  height = height || <span class="hljs-number">50</span>;
  width = width || <span class="hljs-number">60</span>;
  <span class="hljs-keyword">return</span> width * height;
};
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">calculateArea</span>()); <span class="hljs-comment">//300</span>
</code></pre>
<!-- codeblock-end -->

The default parameters makes the initialization more simpler,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-comment">//ES6</span>
<span class="hljs-keyword">var</span> calculateArea = <span class="hljs-keyword">function</span> (<span class="hljs-params">height = <span class="hljs-number">50</span>, width = <span class="hljs-number">60</span></span>) {
  <span class="hljs-keyword">return</span> width * height;
};
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(<span class="hljs-title function_">calculateArea</span>()); <span class="hljs-comment">//300</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
308

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#308-What-are-default-parameters

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
