==================== Question ====================  

### What is an anonymous function  

==================== Answer ====================  

An anonymous function is a function without a name! Anonymous functions are commonly assigned to a variable name or used as a callback function. The syntax would be as below,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">function</span> (<span class="hljs-params">optionalParameters</span>) {
  <span class="hljs-comment">//do something</span>
}
<span class="hljs-keyword">const</span> myFunction = <span class="hljs-keyword">function</span>(<span class="hljs-params"></span>){ <span class="hljs-comment">//Anonymous function assigned to a variable</span>
  <span class="hljs-comment">//do something</span>
};
[<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>].<span class="hljs-title function_">map</span>(<span class="hljs-keyword">function</span>(<span class="hljs-params">element</span>){ <span class="hljs-comment">//Anonymous function used as a callback function</span>
  <span class="hljs-comment">//do something</span>
});
</code></pre>
<!-- codeblock-end -->

Let's see the above anonymous function in an example,

<!-- codeblock-start -->
<pre><code class="hljs language-javascript"><span class="hljs-keyword">var</span> x = <span class="hljs-keyword">function</span> (<span class="hljs-params">a, b</span>) {
  <span class="hljs-keyword">return</span> a * b;
};
<span class="hljs-keyword">var</span> z = <span class="hljs-title function_">x</span>(<span class="hljs-number">5</span>, <span class="hljs-number">10</span>);
<span class="hljs-variable language_">console</span>.<span class="hljs-title function_">log</span>(z); <span class="hljs-comment">// 50</span>
</code></pre>
<!-- codeblock-end -->

==================== Id ====================  
214

---

DECK INFO

TARGET DECK: Javascript::Interview::SJIQ - Javascript interview questions - sudheer jonna::Part I - Introduction::Chapter 1 - Interview Questions

FILE TAGS: #Javascript::#Interview::#SJIQ-Javascript-interview-questions-sudheer-jonna::#Part-I-Introduction::#Chapter-1-Interview-Questions::#214-What-is-an-anonymous-function

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
